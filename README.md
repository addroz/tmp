df.sort(['ticker', 'date'], inplace=True)

# for this example, with diff, I think this syntax is a bit clunky
# but for more general examples, this should be good.  But can we do better?
df['diffs'] = df.groupby(['ticker'])['value'].transform(lambda x: x.diff()) 

df.sort_index(inplace=True)
