<!DOCTYPE html>
<html lang="en-us">
<head>
<style>
body {
  height: 100%;
  width: 100%;
}
section {
  padding: 24px;
  min-height: 80vh;
  border-bottom: 5px solid grey;
}

.button {
  display: inline-block;
  background: tomato;
  color: white;
  padding: 18px;
  font-size: 18px;
  font-family: sans-serif;
  font-weight: bold;
  border-radius: 8px;
  cursor: pointer;
  border: none;
}

.button:active {
  background: rebeccapurple;
}
</style>
<title>How to make a website accessible</title>
    
    </head>
    <body>
    <h1>Accessible Landmarks</h1>
   
    <h2> Navigation Bar </h2>
    <p> Best way to create a navigation bar is by using the NAV element with an unordered list. Screen reader users will hear "Navigation landmark, list of 3 items". They will know how long the list is and decide if they want to tab through the entire list. </p>
    <nav>
    <ul>
    <li><a href="">Home</a></li>
    <li><a href="">About</a></li>
    <li><a href="">Contact</a></li>
    </ul>
    </nav>
<h2>Main Body of the page</h2>
<p> The MAIN tag tells screen readers where the main tag of the web page begins.</p>

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
    <p>Use the ASIDE tag for secondary content, anything that is not part of the main subject </p>

<h1>Accessible Elements</h1>
<p>The easiest way to create an accessible website is to start with semantic HTML tags. HTML by deafualt is accessible and semantic HTML tags will automatically populate the accessibility tree with the correct name, role, state and vaule without any additional work</p>
<p>Start with a simple layout with landmark elements, where the navigation bar is at the top, followed by a main content area and a footer on the botton. Navigation elements are used as shortcuts for assistive technology users, so they can quickly jump to a specific section fo the page. It is very similar to how visual users will look at visual cues on a pake like a navigation bar, headings, etc.</p>

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
    <h2>Terms and Conditions</h2>
    <p> Here are my tertns</p>
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
</html>
