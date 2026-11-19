# Group Sold Products By The Date

Problem Number: 1484

Difficulty: Easy

Language:     lists = activities.groupby(['sell_date'], as_index = False)['product'].unique()
    lists['product'] = lists['product'].apply(lambda x: sorted(x))
    counts = activities.groupby(['sell_date'], as_index = False)['product'].nunique()
    return pd.DataFrame({"sell_date": counts['sell_date'], 'num_sold':counts['product'], 'products':lists['product']})```


Problem URL:
https://leetcode.com/problems/group-sold-products-by-the-date/

Submission Date:
2026-11-19 05:12:44

Generated automatically by LeetSync.
