<!DOCTYPE html>
<html lang="en-us">
<head>
<style>
:root {
  --header-height: 75px;
  --main: #2d2a2e;
  --yellow: #ffd866;
  --black: #111111;
  --white: #fcfcfa;
  --sans-serif: 'Open Sans', sans-serif;
  --monospace: 'Hack', monospace;
}

body {
  font-family: var(--sans-serif);
  background: var(--white);
  min-height: 100vh;
  display: grid;
  grid-template-rows: minmax(min-content, var(--header-height)) auto minmax(min-content, var(--header-height));
  justify-content: center;
}

h1,
h2,
h3,
h4,
h5,
h6,
label {
  font-family: var(--monospace);
}

nav {
  background: var(--main);
  font-size: 1.15rem;
  color: var(--yellow);
  display: flex;
  padding: 1.5rem 0;
  align-items: center;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  gap: 2rem;
}

nav a {
  text-decoration: none;
}

nav a,
footer a {
  color: var(--yellow);
}

footer {
  background: var(--black);
  color: var(--white);
  padding: 3rem 0;
}

form,
form .input-container {
  display: flex;
  flex-direction: column;
}

label {
  margin-bottom: 0.5rem;
}

input {
  max-width: 25rem;
  border: 2px solid var(--main);
  border-radius: 4px;
  line-height: 2rem;
}

input[type='submit'] {
  width: min-content;
  padding: 6px;
  background: var(--yellow);
  font-family: var(--monospace);
  color: var(--main);
  font-weight: bold;
  text-transform: uppercase;
}

/* main {
  display: grid;
  grid-template-columns: minmax(410px, 2fr) 3fr;
  grid-template-rows: 50px 1fr;
  gap: 2rem;
}

main h1 {
  grid-column: 1 / -1;
} */

aside p {
  max-width: 30rem;
}

#terms-content p {
  max-width: 25rem;
}

/* *** Wrapper Styles *** */

.content {
  padding: 0 3rem;
  max-width: 75em;
}

nav .content {
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 100%;
}

/* *** Informative vs Decorative Images *** */
.pawprint {
  width: 30px;
  height: 30px;
}

.pug {
  border-radius: 50%;
  height: 125px;
}

/*  *** Browser Focus ***  */

.skip-link {
  position: absolute;
  left: 50%;
  transform: translateY(-200px);

  /* Fancy Styles   */
  padding: 8px;
  background: var(--black);
  transition: transform 0.3s;
}

.skip-link:focus {
  transform: translateY(0);
}

/*  *** Styling for current tab, using aria-current attribute ***  */
nav a[aria-current='true'] {
  color: white;
  text-decoration: underline;
}

/* *** Focus and hover style of the navigation *** */
nav a:focus,
nav a:hover {
  color: lightgrey;
  text-decoration: underline;
}

/* *** Cursor pointer for checkbox and submit *** */
input[type='checkbox'],
input[type='submit'] {
  cursor: pointer;
}

/* *** Custom Component *** */
#terms-content {
  display: none;
}

#terms-button {
  margin: 0;
  padding: 0;
  margin-top: 1em;
  font-weight: bold;
  border: thin solid transparent;
  background-color: transparent;
  padding-left: 0.125em;
  text-align: left;
  cursor: pointer;
}

#terms-button:focus,
#terms-button:hover {
  background-color: #eee;
  text-decoration: underline;
}

#terms-button:active {
  background-color: #bbb;
  border: 1px dashed #bbb;
}

#terms-button h2 {
  display: inline;
}

#terms-button[aria-expanded='false']::before {
  display: inline-block;
  position: relative;
  content: '🦴';
  transform: rotate(135deg);
}

#terms-button[aria-expanded='true']::before {
  display: inline-block;
  position: relative;
  content: '🦴';
  transform: rotate(45deg);
}

</style>
<title>How to make a website accessible</title>
    
    </head>

      <h2> Navigation Bar test 4 </h2>
    <p> Best way to create a navigation bar is by using the NAV element with an unordered list. Screen reader users will hear "Navigation landmark, list of 3 items". They will know how long the list is and decide if they want to tab through the entire list. You can definitley style your navigation bar using CSS. </p>
    <nav>
      <a class="skip-link" href="#main">Skip to Main Content</a>
  <!-- <div class="content"> -->
    
    
    <ul>
    <li><a href="#home" aria-current="true">Home</a></li>
    <li><a href="">About</a></li>
    <li><a href="">Contact</a></li>
    </ul>
   <!-- </div> -->
    </nav>
<h2>Skip Link</h2>
<p> Using aria-current to tell the screen reader that we are currently on this page. This can also be used for date pickers to show the current date. We can also use CSS for visual users. </p>
    <p> Add a skip link for keyboard users. It is simple and improves their experience! It should be the first thing when tabbing on a web page and it allows users to directly skip to the main content of a web page and bypass blocks of content such as navigation or ads. Add an ANCHOR elemet inside of the NAV tag</p>
    
  <!-- <main id="main" class="content"> -->
      <main id="main">
    <h1>Accessible Landmarks</h1>
   
  
    
<h2> Body of the page</h2>
<p> The  tag tells screen readers where the  tag of the web page begins.</p>

<h2> Footer</h2>
<p> User the FOOTER element for secondary information, such as copyright</p>

<h2>Heading</h2>
<p>Most of the screen reader users will first look at a page heading structure in order to get a feeling for the page. Similar to how people use the table of contents in a book rather than scanning the entire book.</p>
<br> It is important that we do not skip headings or use headings for aestethic reasons becuase the headings level describes the struction of the page.
<h3>Examples</h3>
  
  <bold>Bad Example</bold>
  <p>This is styled to look like a heading</p>
    <h4>Good Example</h4>
    <p>This is H4 heading and the screen reader will read</p>
<h2> Section</h2>
<p> add text here</p>

    <h2> Secondary Content</h2>
    <p>Use the ASIDE tag for secondary content, anything that is not part of the  subject </p>

<h1>Accessible Elements</h1>
<p>The easiest way to create an accessible website is to start with semantic HTML tags. HTML by deafualt is accessible and semantic HTML tags will automatically populate the accessibility tree with the correct name, role, state and vaule without any additional work</p>
<p>Start with a simple layout with landmark elements, where the navigation bar is at the top, followed by a  content area and a footer on the botton. Navigation elements are used as shortcuts for assistive technology users, so they can quickly jump to a specific section fo the page. It is very similar to how visual users will look at visual cues on a pake like a navigation bar, headings, etc.</p>

<section>
  <h2>Form</h2> 
  <p>The FORM tag creates a container for various input elements like text fields, checkboxes, radio buttons, and buttons. Each element shoudl have input and label </p>
  <form action="">
<label for="name">Name</label>
<input type="text" id="name" required>
<p>for and id establishes the programatic relationship. User can click either direclty in the field or on the label and both will focus the input. You can also give it a required attribute and the browser will incude a built in warning when you try to submit </p>

<label for="email">Email</label>
<input type="email" id="email" required>
<p> When using the email type, browser will validat that the value is email. It also allows auto-completion which is very helpful, especially for people that have motor impairments. </p>

      <label>
          <input type="checkbox">
          I accept all the <a href="#terms">terms and conditions</a>
        </label>

        <input type="submit" value="Sign Up">
      </form>
    </section>
    <section id="terms">
      <button id="terms-button" aria-expanded="false" aria-controls="terms-content">
        <h2>Terms and Conditions</h2>
      </button>
      <div id="terms-content">
        <p>Clouds are free they come and go as they please. Let's build some happy little clouds up here. The first step
          to doing anything is to believe you can do it. See it finished in your mind before you ever start. Let's put
          some happy little clouds in our world. Even trees need a friend. We all need friends. There comes a nice
          little fluffer.</p>
        <p>We tell people sometimes: we're like drug dealers, come into town and get everybody absolutely addicted to
          painting. It doesn't take much to get you addicted. We have all at one time or another mixed some mud. This is
          your world, whatever makes you happy you can put in it. Go crazy. Let's put some highlights on these little
          trees. The sun wouldn't forget them. Nice little clouds playing around in the sky.</p>
        <p>If you've been in Alaska less than a year you're a Cheechako. Every day I learn. We can fix anything. We have
          no limits to our world. We're only limited by our imagination.</p>
      </div>
   
  </section>
  <h2>Checkbox Input</h2> 
  <h3>Examples</h3>
  
  <h4>Bad Example</h4>

  <span>Fake Label</span>
  <input type="text">
  <p>This label is just a SPAN tag that isn't associated with the input. Check the accessibility tree and you will see that there is no name associated with the input. The screen reader will just read "edit blank" </p>
  
  <h4>Good Example</h4>
  <label for="text-input">Real Label</label>
  <input type="text" id="text-input">
  <p>This label is associated with the actual LABEL tag. The screen readed will read "Real label edit blank"</p>
  
  <h2>Button</h2> 
  <h3>Examples</h3>
  
  <h4>Bad Example</h4>
 <div class="button">Not a Real Button</div>
 <p> This button is made from a DIV tag. Without additional programming, it would not be accessible for keyboard or screen readers users. It would not get focus when using keyboard and you also can't activate it with a space bar.A DIV does not have any semantic meaning because its purspose is to proved a block level generid container.</p>
 <h4>Good Example</h4>
  <button class="button">Real Button</button>
  <p></p>This is using BUTTON tag in HTML. This button gets all the functionality out of the box. It is operable by keyboard and the screen reader reads "Real Button button</p>

    
<h2>Checkbox Input</h2>
     <!--Use value and name to send the info to the server. 
    Use label to add a label-->
 <label for="my-checkbox">My Checkbox</label>
  <input type="checkbox" id="my-checkbox">

    <label for ="username">Username:</label> <br>
    <input type="text" name ="username"> <br>

<h2>Images</h2>
<figure><img src="https..." alt="This should be a clear alternative text">
  <figcaption>Photo by..</figcaption>
</figure>
    
<p> Alt text is important for non-visual readers, About 140 characters. Figure tag allows us to add additional tags, such as figcaption for giving credits.
  Decorative images that do not provide any additional information should receive empty alt text. THey will then not be added to the accessibility tree. If you do not define alt text, the screen reader will read the file name. Add a class to the image and then use CSS to style the image size.
</p>

    <h1>Keyboard focus</h1>
    <p>When tabbing, browser fucus should highlight interactive elements. The focus ring indicates to a visual keyboard user where they are on a web page. You can replace it with something more consistent with your branding using borders, text size and text decorations.<p>

    <h1>WAI-ARIA</h1>
    <p> WAI-ARIA stands for the Web Accessibility Initiative, Accessible, Rich Internet Applications.
It is a tool that gives a developer the power to directly modify the accessibility tree. Aria does not add any functionality or style to the element. It modifies the accessibility tree so the element's functionality is correctly described to an assistive technology user.</p>

<h2> ROLE and ARIA-LABEL on Search button</h2>
<p></p>The search button below is using FROM and input type "search". The screen reader will announce "Search query".</p>
  <form>
          <input type="search" name="q" placeholder="Search query">
          <input type="submit" value="Go!">
        </form>

<p>The search form is a very important feature but it is not listed under the screenreader landmars. Here is how you can improve it using ARIA features. I have added role="search". The search form will now be called out as a separate item, when browsing thru the page and when browsing by landmarks. Remember that screen reader users will often navigate via landmarks. </p>
  <form role="search">
          <input type="search" name="q" placeholder="Search query">
          <input type="submit" value="Go!">
        </form>

<p> I have also added aria-label attribute aria-label="Search through my page" that will be read out when the form input is highlighted</p>
 <form role="search">
          <input type="search" name="q" placeholder="Search query" aria-label="Search through my page">
          <input type="submit" value="Go!">
        </form>

<h2>ARIA DESCRIBED BY</h2>
Aria described by  uses a text content of an element to describe anothe element on the page. For example, it can be used to describe a label of a button. When the screen reader describes a label, it will read a text input </p>

<button aria-describedby="trash-desc">Move to trash</button>
<p id="trash-desc">
  Items in the trash will be permanently removed after 30 days.
</p>

<h2>Dynamic Content - ARIA-LIVE</h2>
<P> when content updates dynamically without the entire page reloading, the screen reader will not usually read it. This is often used in chat rooms, games, shopping carts, etc. Aria-live will help screen readers read the updated content. Updates can be announced only if the user is idle (polite) or as soon as possible (assertive)
  <p> here is an example from Mozilla <p>
        <section aria-live="assertive" aria-atomic="true">
      <h1>Random quote</h1>
      <blockquote>
        <p></p>
      </blockquote>
    </section>
    <script>
    const quotePara = document.querySelector('section p');

    let quoteJson;

    getQuotes('quotes.json', populateJson);

    let intervalID = window.setInterval(showQuote, 10000);

    function getQuotes(url, callback) {
      let request = new XMLHttpRequest();
      request.open('GET', url);
      request.responseType = 'json';
      request.send();

      request.onreadystatechange = function() {
        if (request.readyState === 4 && request.status === 200) {
          callback(request.response);
        }
      };
    }

    function populateJson(response) {
      quoteJson = response;
    }

    function showQuote() {
      let random = Math.floor((Math.random()*25));
      quotePara.textContent = quoteJson[random].quote + ' -- ' + quoteJson[random].author;
    }
    </script>

    <h2>Keyboard accessiblity</h2>
    <p> HTML has a built-in keyboard accessibility. When working wtih non-semantic elemtns, ARIA can help to provide missing semantics
---
<p>chickpeas</p>
<h2>Pasta Salad</h2>
<p>mozarella</p>
<a href ="location.html">Our Location</a>
<br><br>
<img src ="falafel.jpg" width = "240" height = "135" alt = "falafel">
</body>
<style>
    table, th, td {
        border: 1px solid black;
        border-collapse: collapse;
    }
</style>
<table>
    <tr>
        <th>Dish</th>
        <th>Price</th>
    </tr>
    <tr>
        <td>Falafel</td>
        <td>$10</td>
    </tr>
    <tr>
        <td> Pasta Salad</td>
        <td>$12</td>
    </tr>
</table>

<form action ="/registration" method = "POST">
    <!--Use value and name to send the info to the server. 
    Use label to add a label-->
    <label for ="username">Username:</label> <br>
    <input type="text" name ="username"> <br>

    <label for ="password">Password:</label> <br>
    <input type="password" /><br>

    <input type="checkbox" name="dog" value ="Dog" />
    <label for ="dog"> I own a dog</label> <br>
    <input type="checkbox" name="cat" value ="Cat" />
    <label for ="cat"> I own a cat</label> <br>
    <!--Radio buttons - like checkboxes but only one from the group can be checked-->
    <input type="radio" name="right" value="Right" />
    <label for ="right">I am right-handed</label>  <br>
     <input type ="radio"  name ="left" value = "Left"  />
     <label for="left"> I am left-handed</label> <br>
    <input type="submit" />

    <input type="number" name="age" />
    <input type ="email" name = "email" />
    <input type ="file" name = "file" />
    <!--This may not be correct-->
    <textareaname="multiline" rows="5" ></textareaname> <br>
    <!--drop-down list-->
    <select name="food">
    <option value="chocolate">Chocolate</option>
    <option value="ice Cream">Ice Cream</option></select>
</form>
</main>

</html>
