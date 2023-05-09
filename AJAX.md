## Introduction

AJAX stands for **Asynchronous JavaScript and XML**. It is a set of web development techniques used to create asynchronous web applications. 

> [!NOTE] AJAX
> using AJAX, you can update a web page without reloading the entire page, which provides a smoother and more responsive user experience.

AJAX combines several technologies, including JavaScript, XML, CSS, and HTML, to create dynamic web pages that can be updated without requiring a full page refresh. Instead of loading a new page every time a user clicks a link or submits a form, AJAX enables the browser to communicate with the server in the background, retrieve data, and update parts of the page dynamically.

The XMLHttpRequest (XHR) object is the core of AJAX. It enables JavaScript to send HTTP requests to the server and receive responses asynchronously. AJAX is commonly used in modern web applications, such as social media sites, online marketplaces, and single-page applications.

Suppose you have a web page with a button and a paragraph element, and you want to fetch some data from a server and update the paragraph element when the button is clicked, without reloading the page. 

## AJAX request to django server (at a particular resource)

```javascript
async function makeRequest(url,method,body) {

let headers = {

'X-Requested-With': 'XMLHttpRequest',

'Content-Type': 'application/json'

}

if (method == 'post') {

const csrf = document.querySelector('[name=csrfmiddlewaretoken').value

headers['X-CSRFToken'] = csrf

}

let response = await fetch(url,{

method: method,

headers: headers,

body: body

})

return await response.json()

}
```
