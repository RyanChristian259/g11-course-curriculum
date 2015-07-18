# JavaScript and the DOM - a primer

Let's look at the basics of using *vanilla* JavaScript to manipulate the DOM...

## Set the stage

- Clear the stage (close all other terminal tabs, chrome tabs, email etc...)
- Figure out the "what" and "why" by...
   - reading through the objectives
   - reading through the activities below
- REMEMBER! It's about the process. There's no rush. Take risks, have fun! Don't be afraid to make mistakes and try things.

### Objectives:

By the end of this lesson you should be able to:

- ADD EVAN'S OBJECTIVES

### Key terms:

- ADD KEY TERMS

### Rationale:

- ADD RATIONALE

## Setup

1. Create a new local project directory called "js-dom-basics".
1. Add a local git repository.
1. Create a remote repository on Github.
1. Add a simple `console.log("sanity check!")` in the *main.js* to verify that it's included correctly.
1. In git, add/commit locally, and then push your changes to Github.

## Discussion


#### `getElementbyID`

Add the following code to your JavaScript file:

```javascript
var firstParagraph = document.getElementById('main');
console.log(firstParagraph);
```

Open the JavaScript console in Chrome. **What do you see?**

```javascript
<p id="main">Just a paragraph...</p>
```

**What does this give us?**

Since we are assigning the [DOM node](http://www.w3schools.com/jsref/dom_obj_all.asp) - `<p id="main">Just a paragraph...</p>` to a variable, we now have a reference to it. With the node in hand, we can now view its content (tags, attributes, inner text), manipulate/change any part of it (attributes, inner text, etc.), move it, or remove it altogether. JavaScript gives us this power!

Any node within the [document](http://www.w3schools.com/js/js_htmldom_document.asp), the root node, can be accessed via JavaScript. **What if we wanted to target (or access) the list?**

Without an `id` attribute, we need to use a different [method](http://www.w3schools.com/jsref/dom_obj_all.asp)...

#### `getElementsByTagName`

The 'getElementsByTagName' method returns a collection/array of nodes. These collections are "live", which means that if you add a new HTML element to the collection, it will also be added to the DOM. You can treat the collection just like you would a normal JavaScript array.

Add the following code to your JavaScript file:

```javascript
var getAllElements = document.getElementsByTagName('ul');
console.log(getAllElements)

var getSingleElement = document.getElementsByTagName('ul')[0];
console.log(getSingleElement)
```

Again, open your JS console. **What do you see?**

```javascript
[ul]

<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
  <li>item 4</li>
  <li>item 5</li>
</ul>
```

The first example outputs the *entire* collection while the second example outputs the *first* (and only) element in the collection.

**Can you guess what the following code will do?**

```javascript
allListItems = unorderedList.getElementsByTagName('li');
```

Test it out. Assign it to a variable called `allListItems`, and then log the variable to the console. If all went well, you should see a collection that contains *all* `li`s.

Finally, let's loop through the collection, outputting each *individual* element to the console:

```javascript
for (var i = 0; i < allListItems.length; i++) {
  console.log(allListItems[i]);
}
```

**What if we wanted to simply view the text within each list item, rather than the entire element?**

Simply update the loop like so:

for (var i = 0; i < allListItems.length; i++) {
  console.log(allListItems[i].innerText);
}

**What will this do?**


```javascript
for (var i = 0; i < allListItems.length; i++) {
  console.log(allListItems[i].innerText = i);
}
console.log(allListItems);
```

Test it out!

#### `innerText` vs `innerHTML`

Research this on your own. **How would you construct the Google query?**

#### `createElement`

## Activies