
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">

    <title>How to make a website accessible</title>
    <style>
  html, body {
  margin: 0;
  padding: 0;
}

html {
  font-size: 10px;
  background-color: #6B8787;
}

body {
  width: 70%;
  margin: 0 auto;
}

/*  typography */

h1, h2, h3, h4 {
  font-family: Calibri, Arial;
  color: #2a2a2a;
}

p, input, li {
  font-family: Calibri, Arial;
  color: #2a2a2a;
}

h1 {
  font-size: 4rem;
  text-align: center;
  color: white;
  text-shadow: 2px 2px 10px black;
}

h2 {
  font-size: 3rem;
  text-align: center;
}

h3 {
  font-size: 2.2rem;
}

h4 {
  font-size: 1.8rem;
}

p, li, br {
  font-size: 1.6rem;
  line-height: 1.5;
}

/* header layout */

header {
  margin-bottom: 10px;
}

nav, article, aside, footer {
  background-color: white;
  padding: 1%;
}

nav {
  height: 50px;
  background-color: ff80ff;
  display: flex;
}

nav ul {
  padding: 0;
  list-style-type: none;
  flex: 2;
  display: flex;
}

nav li {
  display: inline;
  text-align: center;
  flex: 1;
}

nav a {
  display: inline-block;
  font-size: 2rem;
  text-transform: uppercase;
  text-decoration: none;
  color: black;
}

nav form {
  flex: 1;
  display: flex;
  align-items: center;
  height: 100%;
  padding: 0 2em;
}

input {
  font-size: 1.6rem;
  height: 32px;
}

input[type="search"] {
  flex: 3;
} 

input[type="submit"] {
  flex: 1;
  margin-left: 1rem;
  background: #333;
  border: 0;
  color: white; 
} 


/*  main layout */

main {
  display: flex;
}

article {
  flex: 4;
}

aside {
  flex: 1;
  margin-left: 10px;
  background-color: #D6F4F4 ;
}

aside li {
  padding-bottom: 10px;
}

footer {
  margin-top: 10px;
}
</style>
</head>

  <body>
    <!-- Here is our main header that is used accross all the pages of our website -->

    <header>
      <h1>How to make a website accessible</h1>

      <!-- Even is it's not mandatory, it's common practice to put the main navigation menu within the main header -->

      <nav>
        <ul>
          <li><a href="#">Layout</a></li>
          <li><a href="#">Elements</a></li>
          <li><a href="#">Keyboard</a></li>
          <li><a href="#">ARIA</a></li>
        </ul>

        <!-- A Search form is another common non-linear way to navigate through a website. -->

        <form>
          <input type="search" name="q" placeholder="Search query">
          <input type="submit" value="Go!">
        </form>
      </nav>
    </header>

    <!-- Here is our page's main content -->
    <main>

      <!-- It contains an article -->
      <article>
        <h2>Accessible Page Layout </h2>

      <p>The easiest way to create an accessible website is to start with semantic HTML tags for landmarks. HTML by deafualt is accessible and semantic HTML tags will automatically populate the accessibility tree with the correct name, role, state and vaule without any additional work</p>
<p>Start with a simple layout with landmark elements, where the navigation bar is at the top, followed by a  content area and a footer on the botton. Navigation elements are used as shortcuts for assistive technology users, so they can quickly jump to a specific section fo the page. It is very similar to how visual users will look at visual cues on a pake like a navigation bar, headings, etc.</p>

        <h3>Navigation Bar</h3>

       <p> The best way to create a navigation bar is by using the NAV element with an unordered list. Screen reader users will hear "Navigation landmark, list of x items". They will know how long the list is and decide if they want to tab through the entire list. You can definitley style your navigation bar using CSS. </p>
        <p> Using aria-current to tell the screen reader that we are currently on this page. This can also be used for date pickers to show the current date. We can also use CSS for visual users. </p>
   
       <h3>Skip Link</h3>

<p> Add a skip link for keyboard users. It is simple and improves their experience. It should be the first thing when tabbing on a web page and it allows users to directly skip to the main content of a web page and bypass blocks of content such as navigation or ads. Add an ANCHOR elemet inside of the NAV tag</p>
      
<h3> Main Content</h3>
<p> xxxxx.</p>
        
        
        <h3> Footer</h3>
<p> User the FOOTER element for secondary information, such as copyright</p>

<h3>Headings</h3>
<p>Most of the screen reader users will first look at a page heading structure in order to get a feeling for the page. Similar to how people use the table of contents in a book rather than scanning the entire book.</p>
<p> It is important that we do not skip headings or use headings for aestethic reasons becuase the headings level describes the struction of the page.</p>
      
  <h4>Bad Example - need to style WIP</h4>
  <p>This is styled to look like a heading</p>
    <h4>Good Example</h4>
    <p>This is H4 heading and the screen reader will read</p>
    
<h3> Section</h3>
<p> add text here</p>

<h3> Secondary Content</h3>
    <p>Use the ASIDE tag for secondary content, anything that is not part of the  subject </p>
        
    <h2>Accessible Interactive Elements</h2>    
        
       <h3>Form</h3> 
  <p>The FORM tag creates a container for various input elements like text fields, checkboxes, radio buttons, and buttons. Each element shoudl have input and label </p>
  <form>
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

   <h4> Another Form - check on this</h4>
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
   
    <!--drop-down list-->
    <select name="food">
    <option value="chocolate">Chocolate</option>
    <option value="ice Cream">Ice Cream</option></select>
</form>

  <h3>Checkbox Input</h3> 
  <h4>Examples</h4>
  
  <h5>Bad Example</h5>

  <span>Fake Label</span>
  <input type="text">
  <p>This label is just a SPAN tag that isn't associated with the input. Check the accessibility tree and you will see that there is no name associated with the input. The screen reader will just read "edit blank" </p>
  
  <h5>Good Example</h5>
  <label for="text-input">Real Label</label>
  <input type="text" id="text-input">
  <p>This label is associated with the actual LABEL tag. The screen readed will read "Real label edit blank"</p>


  <H5>Need to check</H5>
  
     <!--Use value and name to send the info to the server. 
    Use label to add a label-->
 <label for="my-checkbox">My Checkbox</label>
  <input type="checkbox" id="my-checkbox">

    <label for ="username">Username:</label> <br>
    <input type="text" name ="username"> <br>
  
  <h3>Button</h3> 
  <h4>Examples</h4>
  
  <h5>Bad Example</h5>
 <div class="button">Not a Real Button</div>
 <p> This button is made from a DIV tag. Without additional programming, it would not be accessible for keyboard or screen readers users. It would not get focus when using keyboard and you also can't activate it with a space bar.A DIV does not have any semantic meaning because its purspose is to proved a block level generid container.</p>
 <h5>Good Example</h5>
  <button class="button">Real Button</button>
  <p></p>This is using BUTTON tag in HTML. This button gets all the functionality out of the box. It is operable by keyboard and the screen reader reads "Real Button button</p>
      
      <h3>Images</h3>
<figure><img src="https..." alt="This should be a clear alternative text">
  <figcaption>Photo by..</figcaption>
</figure>
    
<p> Alt text is important for non-visual readers, About 140 characters. Figure tag allows us to add additional tags, such as figcaption for giving credits.
  Decorative images that do not provide any additional information should receive empty alt text. THey will then not be added to the accessibility tree. If you do not define alt text, the screen reader will read the file name. Add a class to the image and then use CSS to style the image size.
</p>

<h3> Table </h3>
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
      
       <h2>Keyboard accessiblity</h2>
    <p> HTML has a built-in keyboard accessibility. When working wtih non-semantic elemtns, ARIA can help to provide missing semantics
    <h3>Keyboard focus</h3>
    <p>When tabbing, browser fucus should highlight interactive elements. The focus ring indicates to a visual keyboard user where they are on a web page. You can replace it with something more consistent with your branding using borders, text size and text decorations.<p>

    <h2>WAI-ARIA</h2>
    <p> WAI-ARIA stands for the Web Accessibility Initiative, Accessible, Rich Internet Applications.
It is a tool that gives a developer the power to directly modify the accessibility tree. Aria does not add any functionality or style to the element. It modifies the accessibility tree so the element's functionality is correctly described to an assistive technology user.</p>
      <p> Three main ARIA features:
  <ul>
          <li>Roles- define what the element is. any of these are landmark roles, duplicating the semantic elements. Example: role="navigation" (NAV), role="complementary (ASIDE), role="search", role="tablist", role="tabpanel"</li>
        <li>Properties - give properties to elements. Example: aria-required="true", aria-labelledby="label"</li>
    <li>States - define current conditions of elements. Example: aria-disabled="true" - tells to the screen reader that the form input is currently disabled</li>
        </ul> </p>
    <p> Below are the main arias where ARIA is very useful </p>

<h3> Landmarks</h3>
<p>The search button below is using FORM and input type "search". The screen reader will announce "Search query".</p>
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

<h3>ARIA DESCRIBED BY</h3>
<p>Aria described by  uses a text content of an element to describe anothe element on the page. For example, it can be used to describe a label of a button. When the screen reader describes a label, it will read a text input </p>

<button aria-describedby="trash-desc">Move to trash</button>
<p id="trash-desc">
  Items in the trash will be permanently removed after 30 days.
</p>

<h3>Dynamic Content - ARIA-LIVE</h3>
<P> When content updates dynamically without the entire page reloading, the screen reader will not usually read it. This is often used in chat rooms, games, shopping carts, etc. Aria-live property will help screen readers read the updated content. Updates can be announced only if the user is idle (aria-live="polite") or as soon as possible (aria-live="assertive")
  <p> Add example <p>
        
    
 <h3>Keyboard Accessibility - TABINDEX</h3>
    <p>Native HTML elements have a built-in keyboard accessibility for buttons, form controls, links, etc. When working with a code that uses non-semantic elements, you can use tabindex to make code focusable. 
      <br> tabindex="0" allows elements that are not normally tabbable to become tabbable. </br> </p>

<h3>Form Validation and Errors</h3>
<h4>ARIA-REQUIRED="true"</h4>
<P> This is used for screen readers to tell users that form inputs need to be filled in. The required attribut in HTML works with most screen readers and so there is no need to include both, required and aria-required.</p>
<h4>ROLE="ALERT"</h4>
<p>This automatically turns the element into a live region, so changes to it are read out</p>
<h4>ARIA-RELEVANT="ALL"<h4>
  <P>This tells the screen reader to read out the contents of the error list when any changes are made to it </p>
  <h4>ARIA-LABEL ARIA-LABELLEDBY and ARIA-DESCRIBEDBY</h4>
  <p>Always include a LABEL FOR element for every input. It is a preferred method but can be substituted with 
    <ul>
      <li> ARIA-LABEL - can be used when we do not want the label to be visible. Good example is a text input next to the Search button.</li>
      <li> ARIA-LABELLEDBY - you can designate another id attribute as a label. One element can label multiple form controls. </li>
      <li> ARIA-DESCRIBEDBY - you can associate other descriptive info with the form input. Screen readers will read the label and then the description.
      <br>
      <label for="resetpass">Reset Password:</label>
<input type="password" id="resetpass" aria-describedby="pwnote"><br>
        <span id="pwnote">New password must be 8-15 characters and include letters and numbers.</span> </br> </li>
      
      </p>

      <h3> Making Non-semantic Buttons Accessible </h3>
<p> Whenever possible, it is recommended to use native HTML button.  It is supported by assistive technology and provides keyboard and focus requirements by default.</p>
<p> Here is what you need to do if a non-semantic elements, such as DIV, was used to mark up a button </P>
<h4> Building keyboard focus back in </h4>
<p> Use tabindex="0" so the button is tabbable. </p>
<h4> Building keyboard accessibility back in </h4>
<p> Use JS to activate the button via the Enter/Return key. </p> 
<h4> Building button styling back in </h4>
<p> Use CSS to style the button so it looks like a button </p>
<h4> Building support for screen readers back in </h4>
<p> Use role="button" so screen reader users know they are interacting with button </p>
<h4> Building text labels back in </h4>
<p>

      </article>

      <!-- the aside content can also be nested within the main content -->
      <aside>
        <h2>References</h2>

        <ul>
          <li><a href="#">Reference</a></li>
          <li><a href="#">Reference</a></li>
          <li><a href="#">Reference</a></li>
          <li><a href="#">Reference</a></li>
          <li><a href="#">Reference</a></li>
        </ul>
      </aside>

    </main>

    <!-- And here is our main footer that is used across all the pages of our website -->

    <footer>
      <p>©Copyright 2050 by nobody. All rights reversed.</p>
    </footer>

  </body>
</html> 
      
