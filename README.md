# ArrayListRegisterService

Version(Latest)
----------------------
Last Release Version: v0.1.0
Last Release Date: September 5th, 2018 

Environment Required
----------------------
1.	Python 3.7+
2.	Linux/Unix Instance



Run Command of AaReyS Server on command prompt
---------------------------------------------------------
1.	Aareys_Main.py <ip_address> <port_no>  (In the ip_address creates the <port_no> & listens for clients)
2.	Aareys_Main.py (In the 127.0.0.1 ip creates the 2019 as default port & listens for clients)




GET API URLs List
--------------------
1.	http://127.0.0.1:2019/server/info/version/
2.	http://127.0.0.1:2019/list/create/listName/item
3.	http://127.0.0.1:2019/list/insertItem/listName/item
4.  http://127.0.0.1:2019/list/updateItem/listName/item
5.	http://127.0.0.1:2019/list/getAllItem/listName
6.	http://127.0.0.1:2019/list/findItem/listName/item
7.	http://127.0.0.1:2019/list/getAll/
8.	http://127.0.0.1:2019/list/deleteItem/listName/item
9.	http://127.0.0.1:2019/list/delete/listName/
10.	http://127.0.0.1:2019/list/deleteAll/
11.	http://127.0.0.1:2019/queue/create/queueName/item
12.	http://127.0.0.1:2019/queue/put/queueName/item
13.	http://127.0.0.1:2019/queue/get/queueName
14.	http://127.0.0.1:2019/queue/isEmpty/queueName
15.	http://127.0.0.1:2019/queue/getAll/
16. http://127.0.0.1:2019/queue/deleteItem/
17.	http://127.0.0.1:2019/queue/delete/queueName
18.	http://127.0.0.1:2019/queue/deleteAll/



Running py Script on command prompt to open URL
---------------------------------------------------
>>>import urllib2
>>>import json
>>>import os, time
>>>def callRequest(urlStr):
>>>		response = urllib2.urlopen(urlStr)
>>>		#print response.info()
>>>		jsonString = response.read()
>>>		response.close()
>>>		dictdump = json.loads(jsonString)
>>>		return dictdump['response']
>>>response = callRequest('http://127.0.0.1:2019/list/getAll')
>>>print response

Python Package References 
----------------------------
1.	socket
2.  threading
3.  socketserver 
4.  queue
