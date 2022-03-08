# 10322
StrataScratch 10322
select DISTINCT a.user_id from amazon_transactions a JOIN amazon_transactions b 
ON a.user_id=b.user_id AND a.id != b.id AND 
b.created_at >= a.created_at AND 
b.created_at <= a.created_at + INTERVAL '7 day'
