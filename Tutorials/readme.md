# websokect

http://www.runoob.com/html/html5-websocket.html


https://www.tutorialspoint.com/html5/html5_websocket.htm




====
====


# WebSocket

http://www.websocket.org/

http://www.iana.org/assignments/websocket/websocket.xml

子协议名称必须是 IANA 注册表中的某个注册子协议名称。
截止 2012 年 2 月，只有一个注册子协议名称 (soap)。

https://www.w3.org/TR/soap/
https://en.wikipedia.org/wiki/SOAP
https://www.tutorialspoint.com/soap/

https://www.tutorialspoint.com/index.htm


https://www.html5rocks.com/zh/tutorials/websockets/basics/

https://www.tutorialspoint.com/html5/html5_websocket.htm


http://www.runoob.com/html/html5-websocket.html


## demo

```js
var connection = new WebSocket('ws://html5rocks.websocket.org/echo', ['soap', 'xmpp']);

//请注意 ws:。这是 WebSocket 连接的新网址架构。
//对于安全 WebSocket 连接还有 wss:，就像 https: 用于安全 HTTP 连接一样。


``` 

title: 

Tutorials for Tex Commands, Agile Testing, Apache Tajo, C++ Library, MariaDB, SAP QM, SAP SOLMAN, SAP SCM, MS Access, KoaJS, OAuth2.0, Scrapy, SAP CCA, SAP PM, SAPUI5, Cognos, Internet of Things, Rural Marketing, Trampolining, Golf, CakePHP, SAP EWM, Web Dynpro, Angular2, Framework7, Arduino, CherryPy, Firebase,SAP C4C, SAP Dashboard, SAP PI, ExpressJS, Design Thinking, Internet Security, PyGTK, Apache Drill, Excel Charts, Elastic Search, Computer Security, Extreme Programming, Behavior Driven Development, Conversion Rate Optimization, SAP Basis, Business Law, Kanban, Erlang, SAP Payroll, ASP.Net WP, PouchDB, MFC, SAP HR, Yii, Clojure, Aurelia, CoffeeScript, CPanel, Laravel, SAP Webi, MS SQL Server, pinterest, Indian Polity, Teradata, Windows10



```js
// When the connection is open, send some data to the server
connection.onopen = function () {
  connection.send('Ping'); // Send the message 'Ping' to the server
};

// Log errors
connection.onerror = function (error) {
  console.log('WebSocket Error ' + error);
};

// Log messages from the server
connection.onmessage = function (e) {
  console.log('Server: ' + e.data);
};
``` 


```js
// Sending String
connection.send('your message');

// Sending canvas ImageData as ArrayBuffer
var img = canvas_context.getImageData(0, 0, 400, 320);
var binary = new Uint8Array(img.data.length);
for (var i = 0; i < img.data.length; i++) {
  binary[i] = img.data[i];
}
connection.send(binary.buffer);

// Sending file as Blob
var file = document.querySelector('input[type="file"]').files[0];
connection.send(file);
``` 



