<style>
p { zoom:0.5 }
h4 { zoom:0.7 }
span { color:#6362A1; }
</style>

A basic read file function as we learned

<span>fs.readFile(file, function(err, file) {
if (err) console.error(err);
// writeHead(file)
});</span>

---

#### How to read a file using the stream method

<span>------------------------------------------</span>
</h1>

```js=
const fs = require('fs');
const path = require('path');

const file = path.join(__dirname, ".", "reallybigfile.txt");

var readStream = fs.createReadStream(file);
//set up a read stream on a target file and store it in a variable

var fileContent = '';
//create an empty string we will use to store the contents of the read file.

readStream.on('data', function (chunk) {
  fileContent += chunk;
  console.log(fileContent);
});
//every time a new chunk of the read file becomes available we append it to our fileContent variable

readStream.on('end', function() {
  console.log("reading ended");

});
//once the stream has finished fileContent will contain all the content of the read file and we can
//do something with it.
```



---


# Streams and Buffers in Node.js


---



* A Buffer is an area of memory that stores data, usually binary, that is received faster than it can be processed.
* Node Stream Buffers store data from simple Readable and Writable Streams before sending them out.


---


![](https://i.ytimg.com/vi/GlybFFMXXmQ/maxresdefault.jpg)


---




## Writable and Readable Streams


---


## Writable Streams
* Have a *write* method that passes a string or Buffer object to write to the stream.
* *end* method closes the stream and takes an optional value to write to the stream.
* *write* and *stream* both can take an optional callback




---


## Readable Streams
* Both the 'request' and 'response' are readable streams.
* Reading from a stream is done using event handlers rather than methods.
* Readable streams have *data* and *end* events. *data* is fired when data comes in, *end* is fired when the stream ends.
* This approach is good for data that can be processed immediately, without waiting for the whole document.
* *createReadStream* from *fs* allows a file to be read as a readable stream

___


## .on
* Objects that emit events in Node have a method called *on*, similar to addEventListener.
* *.on* gets an event name and function


---


# Buffers

* The "chunk" value passed to the data handler above may be a binary Buffer. This can be converted so a string by decoding it to UTF-8 using *toString()*.


---



```js=
const http = require('http');

createServer((request, response) => {
  response.writeHead(200, {"Content-Type": "text/plain"});
  request.on("data", chunk =>
  response.write(chunk.toString()));
  request.on("end", () => response.end());
}).listen(8000);

request({
  hostname: "localhost",
  port:"8000",
  method:"POST",
} response => {
  response.on("data", chunk =>
  process.stdout.write(chunk.toString()));
}).end("Hello Server");
```

---
