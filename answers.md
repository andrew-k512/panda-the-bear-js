
1.    Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
      PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

      var pandabear = document.querySelector('.profile-image');
      pandabear.src = "https://placebear.com/400/400"

2.    Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

      var skyPic = document.getElementById("left-image").children[0];
      skyPic.src = "https://placebear.com/325/225"


3.    Select the heading that says "Panda the Bear" and change it to your own name.

      var profName = document.querySelector('.bio-info-name');
      profName.innerHTML = "Andrew"

4.    Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

      var employ = document.querySelector("#employment h3");
      employ.innerHTML = "whatever"      

5.    Change the colour of the body.

      var bod = document.querySelector("body");
      bod.style.backgroundColor = "red";

6.    Change the colour of each element using the highlight class. Use a for loop to do this.

    var highlighted = document.querySelectorAll('.highlight');
    for (var i = 0; i < highlighted.length; i++) {highlighted[i].style.color = "red"};

7.    Change the font family of the h1 to 'monospace'.

    var theH1s = document.querySelectorAll('h1');
    for (var i = 0; i < theH1s.length; i++) {theH1s[i].style.fontFamily =
    "monospace"};

8.    Find a way to select the round icons in the sidebar and then change their colour.

    var iconCircles = document.querySelectorAll('a.action-icon-bg');
    for (var i = 0; i < iconCircles.length; i++) {iconCircles[i].style.backgroundColor =
    "blue"};

9.    Scroll down to the contact form. Change the placeholder attribute of the field where it says "Enter your name" to "identify yourself".

    var nameField = document.querySelector('input#name');
    nameField.placeholder = "Identify Yourself";

10.    Change the placeholder attribute of the message field to "state your business".

    var messageField = document.querySelector('#message');
    messageField.placeholder = "State your business";


11.    Give the name field a "value" attribute of "your nemesis".

      nameField.innerHTML = "Your nemesis"

12.    Change the value attribute of the email field to "koalathebear@gmail.com".

      var emailField = document.querySelectorAll('#email');
      emailField.innerHTML = "koalathebear@gmail.com";


13.    Change the value of the submit button on the contact form to "En garde!".

      var submitButton = document.querySelector("#submit");
      submitButton.value = "en Garde!";

14.    We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the
       disabled  attribute).

       submitButton.disabled = true

15.    We should help Panda protect their privacy by erasing their personal details from the sidebar.

      var pandaInfo = document.querySelector("ul.bio-info");
      pandaInfo.visibility = "hidden";
      // Does not work

------ Part 2 ----------------------------

1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)

  var timeTravelDiv = document.querySelector("#time-travel");
  var timeTravelParent = timeTravelDiv.parentElement;
  timeTravelParent.remove()

2. That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().

  var pikaDiv = document.querySelector("#right-image");
  var pikaImage = pikaDiv.children[0]
  var pikaClone = pikaImage.cloneNode(true);
  document.querySelector(".portfolio-container").appendChild(pikaClone);

3. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

for (var i = 0; i < 10; i++) {
 var pikaClone = pikaImage.cloneNode(true);
 document.querySelector(".portfolio-container").appendChild(pikaClone);
}

4. Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

var pandaInfo = document.querySelector("ul.bio-info");
var newLI = document.createElement("LI");
var textnode = document.createTextNode("Last updated today");
newLI.appendChild(textnode);
pandaInfo.appendChild(newLI);
