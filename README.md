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

```
https://docs.google.com/forms/d/e/1FAIpQLScOS65F0ZSyiyFeC2y4X1Y76YIg-HYgFgWhmeawIi-uFcauTQ/viewform?usp=pp_url&entry.1804520491=cskbotboi&entry.1428655783=cskbotboi@gmail.com&entry.877185975=Hello!
```

## Grabbing Entries 


