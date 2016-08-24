## 各浏览器Cookie大小、个数限制


网上查找出来的结果是：

 

一、浏览器允许每个域名所包含的cookie数：

　　Microsoft指出InternetExplorer8增加cookie限制为每个域名50个，但IE7似乎也允许每个域名50个cookie。

　　Firefox每个域名cookie限制为50个。

　　Opera每个域名cookie限制为30个。

　　Safari/WebKit貌似没有cookie限制。但是如果cookie很多，则会使header大小超过服务器的处理的限制，会导致错误发生。

　　`注：“每个域名cookie限制为20个”将不再正确！`

二、当很多的cookie被设置，浏览器如何去响应。

　　除Safari（可以设置全部cookie，不管数量多少），有两个方法：

* 最少最近使用（leastrecentlyused(LRU)）的方法：当Cookie已达到限额，自动踢除最老的Cookie，以使给最新的Cookie一些空间。Internet Explorer和Opera使用此方法。

* Firefox很独特：虽然最后的设置的Cookie始终保留，但似乎随机决定哪些cookie被保留。似乎没有任何计划（建议：在Firefox中不要超过Cookie限制）。

三、不同浏览器间cookie总大小也不同：

　　Firefox和Safari允许cookie多达4097个字节，包括名（name）、值（value）和等号。

　　Opera允许cookie多达4096个字节，包括：名（name）、值（value）和等号。

　　Internet Explorer允许cookie多达4095个字节，包括：名（name）、值（value）和等号。
     
   `注：多字节字符计算为两个字节。在所有浏览器中，任何cookie大小超过限制都被忽略，且永远不会被设置`