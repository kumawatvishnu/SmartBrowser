# SmartBrowser (using concept of cooperative caching)

Presently, web browsers don't contact with each other for sharing web cache. So when a miss occurs in local web cache, the request will be sent to web cache server and then to source server, despite the existence of 
the requested web resource in the same subnet. In this situation, each browser is separated and full resource utilization doesn't happen.

But if each browser cooperates with each other, a node will try to find web resource in the other node when hit in local web cache misses.

This project aims at implementing **"A Cooperative Browser-level Web Caching System Based on Chord"**.

Chord is a protocol and algorithm for a peer-to-peer distributed hash table. By implementing cooperative caching based on Chord, we intend to increase cache hit. Accordingly, decreasing the time required for loading the webpage's content.

In a close area, the chances that node needs the same resource is higher. If nodes are connected directly with peer-to-peer, the waiting time will be reduced. And we believe the problem will be solved to some extent.

#Features

* Connect different systems in a same subnet.
* Option to manually connect to a system by entering ip address and username of user or simply enter the broadcast address of the subnet and leave the connection part to smart browser.
* Option to set proxy for LAN.
* Fetch web content from web server by pressing ON button.
* Fetch web content from local cache & from Chord DHT cache by pressing OFF button.
* Option to view all cache present in the subnet, just press show all cache.
* Don't want to store cache ? just check incognito mode.
* Get stats of time taken to fetch the webpage & last update for cache files.

#screenshot

![shot_1](https://user-images.githubusercontent.com/20659938/29840572-1c6960a6-8d20-11e7-83e2-097b6df6db01.png)

![mysmartbrowser](https://user-images.githubusercontent.com/20659938/29840573-1c69f958-8d20-11e7-861e-be1872e9c5c3.png)


# Compilation and Execution

**Compiling the project :**

javac -classpath "path to ur jfxrt.jar file" *.java

Example : javac -classpath "/usr/lib/jvm/jdk1.8.0_121/jre/lib/ext/jfxrt.jar" *.java"

**Running the project :**

java -classpath "path to ur jfxrt.jar file:." NewBrowser

Example : javac -classpath "/usr/lib/jvm/jdk1.8.0_121/jre/lib/ext/jfxrt.jar:." NewBrowser"
