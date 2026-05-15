Сколько всего строк в логе: 
iisus.rodilsiagmail.com@MacBookPro task9 % wc -l nginx_logs
   51462

Сколько запросов получили статус 200:
iisus.rodilsiagmail.com@MacBookPro task9 % grep "200" nginx_logs | wc -l
    4413

Сколько запросов с ошибками 4xx или 5xx:
iisus.rodilsiagmail.com@MacBookPro task9 % grep -E "[4-5][0-9]{2}" nginx_logs | wc -l
   36874

Топ-5 самых частых IP-адресов в логе:
iisus.rodilsiagmail.com@MacBookPro task9 % awk '{print $1}' nginx_logs | sort | uniq -c | sort -rn |head -n 5
2350 216.46.173.126
1720 180.179.174.219
1439 204.77.168.241
1365 65.39.197.164
1202 80.91.33.133
