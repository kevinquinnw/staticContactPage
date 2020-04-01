# staticContactPage
A tutorial on how to create a functional contact page with google forms, and HTML.

# Task 
I have heard of so many ways to create a contact page with static websites and I have found that this is the easiest way. 

### Our steps are:
1. Create your html form
2. Create a google form
3. Snag some code from the form 
4. Make the redirect hidden with JavaScript.

# Create HTML Form 
#### Make it basic, we will go back to it later.

```html 
<form>

    <p>Name</p>
    <input placeholder="Name" type="text" required>

    <br>

    <p>Email</p>
    <input placeholder="Email" type="email" required>

    <br>
    
    <p>Message</p>
    <textarea placeholder="Comment"></textarea><br>
    
    <br>

    <button type="submit">Send</button>
  
</form>
```

# Create a Google Form 

#### Create a google form and add as many questions as you like.
![Questions](questions.png "Optional Title")

#### Get the prefilled link
![Pre-filled Link](pre-filled-link.png "Optional Title")


### We will extracting the entry values from the link and using it for our form. You will have to fill out the form, submit it, then copy the link.

```
https://docs.google.com/forms/d/e/1FAIpQLScOS65F0ZSyiyFeC2y4X1Y76YIg-HYgFgWhmeawIi-uFcauTQ/viewform?usp=pp_url&entry.1804520491=cskbotboi&entry.1428655783=cskbotboi@gmail.com&entry.877185975=Hello!
```

# Adding code. 
In the url, your entry will be equal to what you typed out on the survey. 

## Add the following to your <form> tag.

### Note: For the action part, erase up to "viewform?" piece of the URL and put formResponse?. 

```html 
<form name="gooform" id="gooform" enctype="text/plain" action ="https://docs.google.com/forms/d/e/1FAIpQLScOS65F0ZSyiyFeC2y4X1Y76YIg-HYgFgWhmeawIi-uFcauTQ/formResponse?" target ="hidden_iframe" onsubmit="submitted=true;">
```

## Name, Email, Message, Field's
```html
    <p>Name</p>
    <input id="entry.1804520491" name="entry.1804520491" placeholder="Name" type="text" required>

    <br>

    <p>Email</p>
    <input id="entry.1428655783" name="entry.1428655783" placeholder="Email" type="email" required>

    <br>
    
    <p>Message</p>
    <textarea id="entry.877185975" name="entry.877185975" placeholder="Comment"></textarea><br>
```


### It should all look like this. 
```html 
<form name="gform" id="gform" enctype="text/plain" action ="https://docs.google.com/forms/d/e/1FAIpQLScOS65F0ZSyiyFeC2y4X1Y76YIg-HYgFgWhmeawIi-uFcauTQ/formResponse?" target ="hidden_iframe" onsubmit="submitted=true;">

    <p>Name</p>
    <input id="entry.1804520491" name="entry.1804520491" placeholder="Name" type="text" required>

    <br>

    <p>Email</p>
    <input id="entry.1428655783" name="entry.1428655783" placeholder="Email" type="email" required>

    <br>
    
    <p>Message</p>
    <textarea id="entry.877185975" name="entry.877185975" placeholder="Comment"></textarea><br>
    
    <br>

    <button class="" type="submit">Send</button>
  
</form>
```


