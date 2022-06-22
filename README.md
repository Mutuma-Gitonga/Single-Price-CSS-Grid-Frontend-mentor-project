# Simple CSS Grid Component Challenge - Frontend Mentor
# Introduction
After watching [Brad Traversy's CSS Grid tutorial](https://www.youtube.com/watch?v=0xMQfnTU6oo), I sought a worthwhile development challenge on the question. In light of that, I found one on [Frontend Mentor](frontendmentor.io). I found it quite simple and I describe the development process briefly. 

# Challenge Instructions
Producing an optimal layout for different screen sizes as rendered in [this design](https://www.frontendmentor.io/challenges/single-price-grid-component-5ce41129d0ff452fec5abbbc) from the Frontend mentor website. In addition, the challenge requires applying any desdired hover state change on the Sign Up button for the desktop view.

## Tools and Resources
**Frontend mentor resources:** Here, I found the vital project style guide (that includes color codes, design widths, font size, and font family) and the README template (with extra instructions and ofcourse the template documentation).

**Google:** Searching online resources to resolve any pitfalls I run into.

**VS Code Editor:** Shifted to VS Code after a month's stint of using the Sublime Text Code editor. I have frankly found VS Code more versatile than the latter code editor. In particular, VS Code has a convenient inbuilt command line for running git bash commands. Besides, the inbuilt [Emmet toolkit](https://code.visualstudio.com/docs/editor/emmet) has significantly increased my productivity especially when penning html markdown.

**Chrome or Mozilla:** Any of these browsers will do to visualize the layout grids in the developer tools section. Such visualization is critical as explained in Traversy's tutorial, especially in specifying the column and row spans in the stylesheet.

## My Solution Screenshots and hosted URLs
I took these screenshots using Mozilla Firefox's screenshot tool, available in its context sensitive menu.

**Desktop view screenshot**
![Desktop view screenshot](https://github.com/Mutuma-Gitonga/Single-Price-CSS-Grid-Frontend-mentor-project/blob/main/Solution%20Screenshots/Desktop%20view%20screenshot.png)

**Mid screen view screenshot**
![Midscreen view screenshot](https://github.com/Mutuma-Gitonga/Single-Price-CSS-Grid-Frontend-mentor-project/blob/main/Solution%20Screenshots/mid%20screen%20screenshot.png?raw=true)

**Mobile view screenshot**

![Mobile view screenshot](https://github.com/Mutuma-Gitonga/Single-Price-CSS-Grid-Frontend-mentor-project/blob/main/Solution%20Screenshots/mobile%20view%20screenshot.png)


**Static site URL:**

**Live site URL:**

## My Development Process
### Web Technologies and Principles Employed
- Non-semantic HTML5 markup. 
- CSS3 Custom properties.
- [CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout).
- Mobile-first responsive design (using media query).

### Step 1: Project HTML Skeleton and Class Naming (Grid Container and Grid Items)
The skeleton consists of a grid container that's a div element having "price-card" as its custom class name. In this container, I created three grid items/elements, all div elements with appropriate names, that is, "card--bg-white", "card--bg-darkcyan", and "card--bg-lightcyan"

As seen in the previous paragraph, the grid items class names assume a uniform naming convention that includes the object in question (in this case the cards) and their background colors. Developer circles call this CSS class selector name convention the block, element, modifier (BEM). BEM's primary purpose is improving code maintainability, which means greater developer productivity. I read a concise BEM article over at [freeCodeCamp](https://www.freecodecamp.org/news/css-naming-conventions-that-will-save-you-hours-of-debugging-35cea737d849/).

See below for the HTML skeleton code snippet:

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Single Price Grid Component Project</title>
</head>
<body>
  
  <div class="price-card">
    <div class="card--bg-white">
    </div>

    <div class="card--bg-darkcyan">
    </div>

    <div class="card--bg-lightcyan">
    </div>
  </div>
  
</body>
</html>
```

### Step 2: Populating "card--bg-white" CSS grid item with code
The design mockup portrays a grid item where the first two text lines have special styling. Therefore, I chose a heading 3 for the headliner, then used a paragraph with a class name "card_title" to style the second line.

The remaining text is added within a paragraph element.

Below is the code snippet for this grid item:

```HTML
<div class="card--bg-white">
      <h3>Join our community</h3>
      <p class="card__title">30-day, hassle-free money back guarantee.</p>
      <p>Gain access to our full library of tutorials along with expert code reviews. <br> Perfect for any developers who are       serious about honing their skills.</p>
</div>
```

### Step 3: Coding the "card--bg-darkcyan" CSS grid element
In this grid item, the headliner was equally set using a heading 3. On its part, the text was wrapped within paragraph elements, with a line break separating the two text parts. An span inline element wrapped the monthly charge amount for styling it with a larger font-size. 

The sign up button was wrapped within a div element and style added to center the button in the container thanks to [this JavaTPoint resource](https://www.javatpoint.com/how-to-center-a-button-in-css). Also, I added an anchor element to make sign up a link.

The code snippet below demos these html markdown choices:

```HTML
<div class="card--bg-darkcyan">
      <h3>Monthly Subscription</h3>
      <p><span>$29</span> per month <br> Full access for less than $1 a day</p>
      <div style="text-align: center;">
      <button class="signup_button"><a href="#signup">Sign Up</a></button>
      </div>
</div>
```

### Step 4: Adding HTML markdown to "card--bg-lightcyan" CSS grid item
I used heading 3 as the headliner for the main text line. I then wrapped the rest of the text within a paragraph element having requisite break elements within it. 

Below is the code snippet:

```HTML
<div class="card--bg-lightcyan">
      <h3>Why Us</h3>
      <p>
        Tutorials by industry experts <br>
        Peer & Expert code review <br>
        Coding exercises <br>
        Access to our GitHub repos <br>
        Community forum <br>
        Flashcard decks <br>
        New videos every week
      </p>
</div>
```

### Step 5: Coding the Stylesheet
With the HTML markdown done, I created a stylesheet file "style.css" on the git bash command line. Next, I linked the stylesheet to the html file using a link element in the head section, as in the code snippet below:
```HTML
<link rel="stylesheet" href="style.css">
```
