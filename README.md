# freedns
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

You can create your account:
https://www.noip.com/

You can login.

Create your hostname.

In order to manage dynamic DNS, run the following command.

$ pip install noipy

$ noipy -u username -p password -n xxx.ddns.net --provider noip
