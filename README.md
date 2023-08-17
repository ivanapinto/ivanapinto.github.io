<!DOCTYPE html>
<html>
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
    <nav>
    <ul>
    <li><a href="">Home</a></li>
    <li><a href="">About</a></li>
    <li><a href="">Contact</a></li>
    </ul>
    </nav>
    <p> Best way to create a navigation bar is by using the NAV element with an unordered list. Screen reader users will hear that it is a lit with x items. The will know how long the list is and decide if they want to tab through the entire list.
<body>
<h1>Accessible Elements</h1>
<p>The easiest way to create an accessible website is to start with semantic HTML tags. HTML by deafualt is accessible and semantic HTML tags will automatically populate the accessibility tree with the correct name, role, state and vaule without any additional work</p>
<p>Start with a simple layout with landmark elements, where the navigation bar is at the top, followed by a main content area and a footer on the botton. Navigation elements are used as shortcuts for assistive technology users, so they can quickly jump to a specific section fo the page. It is very similar to how visual users will look at visual cues on a pake like a navigation bar, headings, etc.</p>

<section>

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
