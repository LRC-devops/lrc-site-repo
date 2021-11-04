# lrc-compiled-site

To make changes to the site, make sure to read through the basic formatting section so that you understand how to edit the underlying code.
After reading, navigate to the section that explains how to make the edit you need.

NEVER ALTER THE FIRST TWO CONTENT BLOCKS ON ANY PAGE OF THE WEBSITE. These two elements are shared blocks and contain the CSS stylesheet and Navigation menu. If a change is made in these elements and something is broken, it will break all pages on the site as well.

For permanent changes, the alterations need to be done inside of a local environment. You will need to download VSCode, clone this repository, make the changes in a branch, commit that branch, and upload the new code to Sitefinity. Instructions on how to do this can be found below.

Basic HTML formatting explanation

---

    HTML is formatted with a specific structure. Each element begins with an opening tag and a closing tag. The type of tag changes depending on the element, but every element is opened and closed in the same way. The basic structure looks like this:
      <div> //this opens the element. You start with <, name the element (this is a div element), then close the element with the same tag, but adding a slash so the environment knows the element is closed. Like this:
      </div>

    When an element is styled, other components are added to the opening tag, but the close tag remains the same.
      <div class=”inPerson-session” title=”This is a test” href=”uuu.url-test.com”> //Styled elements may look like this, but always close with the same simple tag:
      </div>

    Comments are elements that the computer skips over and only for documentation to help keep the programmer organized and let others know how things work. In HTML, comments open with this tag:
    <!—-
    And close with this tag
    -->
    Anything between these tags will be greyed out and ignored by the computer.


    CSS comments look like this:
    /* opening comments
    */ closing comment.


    SCSS comments look like this:
    //each line will have these two slashes and will be ignored by the computer

    //They
    //can
    //be
    //multiline
    //comments
    //like
    //this

    Classes are used to style HTML elements and are styled in a completely different way. There should be no need to edit a CSS element, only add one to an HTML element. CSS IS CASE SENSITIVE so be sure to watch out for that.
    HTML elements are styled by added a CSS class to the element that tells it to look a certain way.

    HTML tags set the structure, and anything after the > of the opening tag will appear as text on the website. ex:
    <div class="test">THIS TEXT WILL BE VISIBLE AND STYLED HOWEVER THE test CLASS SPECIFIES</div>

HOW SESSIONS ARE FORMATTED

---

    <!--
    <tr class="inPerson-session"> //This is where the color of the row is added. use class="inPerson-session" for gold, class="zoom-session" for green, and class="cancel-session" for red cancellations.
      <td>Computer Science</td> //This is the title of the session. For cancellations: use this HTML code &times; to insert an 'X', state that the session is canceled then add <br> for a breakpoint. The title of the session should break to a new line, so the students know what session is canceled.
      <td>Tu 2:30-4pm</td> //This row is super simple and only states the day and time of the session
      <td>* In Person</td> //This row is simple for in-person sessions, but a little different for zoom sessions. The * directs the viewer down to the bottom of the popup for additional information.
    </tr> //This tag simply closes the row.

    <tr class="inPerson-session">
      <td>Computer Science</td>
      <td>Th 11-12:30pm</td>
      <td>* In Person</td>
    </tr>
    -->

TO ADD AN IN-PERSON SESSION

---

    For adding a session, simply find the correct slot in between the days/times that the new session should sit. Copy the session above and edit the information to reflect the new session.
    Begin by locating the correct course popup with the schedule you are attempting to alter

    Find a space for the new session. Pay attention to how the sessions are organized by course, then by day of the week and time

TO ADD A ZOOM SESSION

---

        Follow the same steps above for duplicating then altering the new session. The format for zoom-sessions is explained below.

       <!--
         <tr class="zoom-session"> //This is where the zoom-session styling is added to the row.
          <td>Computer Science</td> //This is the title of the session
          <td>F 12-1:30pm</td> //This is the day/time of the session
          <td><a href="https://ucdenver.zoom.us/j/92310857800" title="Manharsh Zoom Link" class="popup__table--courses--link">** Online - Zoom Session</a></td> //This is where this row differs from the inPerson session. The <td> tag opens, and another tag opens directly after it, the <a> tag. This is where the link goes. The link to the zoom session goes in the href, href="place-link-here", the style goes in the class tag, and the title is the name of academic guide, title="Academic-Guide's Zoom Link". This title exists for accessibility and organizational purposes.
        </tr>
       -->

TO CANCEL A SESSION

---

      Canceling a session means you will need to replace the <tr> class with a cancel class. After that you will add something like this to the title of the session:
      <!--
      <tr class="cancel-session"> //You will replace the inPerson-session or zoom-session class with the cancel-class
        <td>&times; Session canceled DATE<br>Computer Science</td> //add the &times; elements, specify the cancellation and date, add a <br> to break the line, then leave the title of the session.
      -->
      This process should be the same for inPerson and zoom sessions.

USING VSCODE TO MAKE CHANGES

---

    Begin inside of GitHub desktop. You will use the tabs at the top to fetch the most updated version of the code. Click "Fetch Origin" to update the code in your local environment.
    Next, you will create a new branch to make your edits. Use the tab next to "fetch Origin" to do so. Click on "Current Branch", then click on the button on the upper-right side of the popup window that says "New Branch".
      Title the new branch with the name of the update(s) you are making. Ex.
        If you are updating Question Session schedules, title the branch something like ag-qs-sched-update
          You will use a description later to explain your edits more in-depth.
    Once you have created a new branch, you are ready to make changes to the code! Click the button on the main window that says "open in Visual Studio Code".
    Make your edits.
    Once you are done editing the code, return to GitHub desktop.
    Use the window in the lower left-hand corner to create a message attached to your update. Title the message, and describe the changes you made.
    Use the blue button below that message window to commit the changes.
    Next, the tab at the top which previously read "fetch origin" new says something like "publish branch". Click this button to finalize the edits. Once you have published the branch, I can review our edits and okay the changes to be added to the master branch origin.
