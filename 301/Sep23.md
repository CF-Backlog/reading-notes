# Form Data 

MDN: [Forms and Data](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data)       
Reference: [HTML Forms](https://htmlreference.io/forms/)   
YouTube: [HTML 5 Form Styling Video](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK)  

## MDN Sending Data page

When a user *submits* a form - where does the data go? How do we handle the data when it gets to where it's going? 

> A client (like browser) sends a request to a server using the HTTP protocol, the server answers with the same protocol
 HTML `form` is user-friendly way to configure HTTP request to *send data* to a server
 The `<form>` element defines **how** the data is sent w/its `action` and `method` attributes

`action` attribute defines **where** data is sent via a: 
   *relative URL* `<form action="/somewhere_else">`
   *absolute URL* `<form action="https://example.com>`

> Note: If your form is hosted on HTTPS but you specify data to be sent to HTTP (insecure) you will get a security warning as a user because data will not be encrypted.

> The server responds by handling data and loading the URL, often causing a page reload if pointed to the same page. 
`method` attribute defines **how** data is sent

> HTML form data is transmitted most commonly as `GET` or `POST` method

> HTTP request consists of 2 things: **header** that contains set of global metadata about browser capabilities and **body** with necessary info for the server to process

`GET` basically asks the server to send back a specific resource

> You'll see that resource appear in the address bar when you submit the form: 
   `www.foo.com/?say=Hi&to=Mom` appears with this code in the html: 
   <image src="../images/read13-1.png" style="width: 400px">
   Data in the URL is series of key/value pairs tied with `&`
 `POST` basically says "Hey server, look at this data and send me back an appropriate result" and the data is appended to the **body** of the HTTP request.

> Note: The POST method does NOT append data in the URL. A `POST` HTTP request looks like this: 
   <image src="../images/read13-2.png" style="width: 300px">
   `Content-Length` header indicates size of body
   `Content-Type` header is type of resource sent to server

> HTTP requests are never displayed to the user, if you want to see them use Chrome Dev tools in the Network section

### Only thing the users sees is the URL called (when using GET) and with POST the user sees nothing. Ex: To send a *password* NEVER use GET because you don't want this to show up in the URL

## On the Server Side | When it receives Data
 It takes a string and parses to get the key/value pair data
 It is accessed depending on the **development platform** and **framework** you use 
 While there are many server-side technologies for form handling, it is more common to use a 

**high-quality framework** : 
   Django for Python
   Express for Node.js
   Laravel for PHP
   Ruby on Rails for Ruby
> Frameworks make it easier than trying to do this from scratch

## Sending Files
> There are 3 special requirements to consider when sending files
   Set `method` to `POST` so it's not in the URL
   Set the value of `enctype` to `multipart/form-data`
   Include one or more `<input type="file">` controls to allow users to select the file(s) that will be uploaded
  > ### Set size limit to prevent abuse

## Security 
> Never trust your users or yourself!
> Attacks most commonly happen in the part that dictates **how** the server handles data

> **All data** checked 
  Escape dangerous characters like char sequences that look like executable code links JS or SQL
  Limit incoming amount of data to what's necessary
  Sandbox uploaded files (store them in a different server and allow access via a subdomain)
