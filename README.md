# Form.js
A javascript file which will give your forms the power of AJAX if the user allows it!
NOTE - JQUERY IS REQUIRED TOO!!!

##What you need to know...
Form.js will utilise AJAX when it can however if the user has javascript disabled or can't support AJAX, forms will be sent in the standard method which requires a page refresh...

Form.js will detect when forms with the class 'ajax' have been submitted and it will attempt to send the form data to the file declared as the action attribute on the form. Form.js will only send the fields with a name attribute declared also. For example...

```html
  <form class='ajax' action='send.php' method='POST'>
    <input type='text' name='fruit' placeholder='enter a fruit'>
    <input type='text' placeholder='This will not send!'>
    <input type='submit' value='Send'>
  </form>
```

This form is AJAX enabled due to the "class='ajax'" attribute. The AJAX call will use the method of POST declared by the attribute "method='POST'" to send the data to the file declared by "action='send.php'". The only data which will be sent is the 'fruit' field as it is the only field which has a name attribute (name='fruit'). The other fields will not be sent!

Finally, you need to create a function on the page called 'response' as the response from the other file will be passed as a parameter to this function. Here is an example of a response function...

``` javascript
  function response(data){
    alert(data);
  }
```

This isn't a great response function as it just alerts the response to the user, but you can craft this to your application and not have to worry about the underlying AJAX!

