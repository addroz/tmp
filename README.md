df['DiffHeartRate']=(df.groupby(['Disease', 'State', 
          (df.MonthStart.dt.month.ne(df.MonthStart.dt.month.shift()+1)).cumsum()])['HeartRate']
 .apply(lambda x: x.diff())).fillna(df.HeartRate)
