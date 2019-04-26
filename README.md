# freedns
This is a repository for updated source programs in the following books:
1. https://www.amazon.co.jp/AVR%E3%83%9E%E3%82%A4%E3%82%B3%E3%83%B3%E3%81%A8Python%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%88%E3%81%86-IoT%E3%83%87%E3%83%90%E3%82%A4%E3%82%B9%E8%A8%AD%E8%A8%88%E3%83%BB%E5%AE%9F%E8%A3%85-%E6%AD%A6%E8%97%A4-%E4%BD%B3%E6%81%AD/dp/4274217906/ref=sr_1_3?
2. https://www.amazon.cn/dp/B07M5XDTD2/ref=sr_1_1?__mk_zh_CN=%E4%BA%9A%E9%A9%AC%E9%80%8A%E7%BD%91%E7%AB%99&keywords=yoshiyasu+takefuji&qid=1556317403&s=gateway&sr=8-1
3. https://www.kingstone.com.tw/new/basic/2013120498099?kmcode=2013120498099&lid=book_new_flow&actid=book_flow

This shows how to setup dynamic DNS using freedns service.

Whenever your IP changed, you can access to the same machine using dynamic DNS. 

You can create your account on https://freedns.afraid.org/

freedns.py is a program to manage dynamic DNS for freedns service.

You can pick your favorite domain name from https://freedns.afraid.org/.

You should modify USERNAME, PASSWORD, and UPDATE_DOMAIN in freedns.py respectively.

Use crontab -e to activate crontab 

The following setting in crontab indicates every minute to maintain the dynamic DNS.

" * * * * * python xxx/freedns.py >/dev/null"

xxx is "path to the program of freedns.py"

----------------------------------------
The following dynamic DNS providers have the same scheme:
No-IP (3 free names) (expires in 30 days)
DuckDNS
DynDNS


You can create your account:
https://www.noip.com/

You can login.

Create your hostname.

In order to manage dynamic DNS, run the following command.

$ pip install noipy

$ noipy -u username -p password -n xxx.ddns.net --provider noip
