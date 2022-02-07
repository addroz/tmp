
def cal_diff(x):
    x['DiffHeartRate'] = np.where(x['MonthEnd'].shift().dt.month.eq(
        x['MonthStart'].dt.month), x['HeartRate'].diff(), x['HeartRate'])
    return x


df = df.groupby(['Disease', 'State']).apply(cal_diff)
