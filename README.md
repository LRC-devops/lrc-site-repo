# lrc-compiled-site

Basic HTML formatting explanation
____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

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

 

HOW SESSIONS ARE FORMATTED
____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

    <!--
    <tr class="inPerson-session"> //This is where the color of the row is added. use class="inPerson-session" for gold, class="zoom-session" for green, and class="cancel-session" for red cancelations. 
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
____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

    For adding a session, simply find the correct slot in between the days/times that the new session should sit. Copy the session above and edit the information to reflect the new session.
    Begin by locating the correct course popup with the schedule you are attempting to alter

    Find a space for the new session. Pay attention to how the sessions are organized by course, then by day of the week and time
  
TO ADD A ZOOM SESSION 
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

        Follow the same steps above for duplicating then altering the new session. The format for zoom-sessions is explained below. 

       <!--
         <tr class="zoom-session"> //This is where the zoom-session styling is added to the row. 
          <td>Computer Science</td> //This is the title of the session
          <td>F 12-1:30pm</td> //This is the day/time of the session
          <td><a href="https://ucdenver.zoom.us/j/92310857800" title="Manharsh Zoom Link" class="popup__table--courses--link">** Online - Zoom Session</a></td> //This is where this row differs from the inPerson session. The <td> tag opens, and another tag opens directly after it, the <a> tag. This is where the link goes. The link to the zoom session goes in the href, href="place-link-here", the style goes in the class tag, and the title is the name of academic guide, title="Academic-Guide's Zoom Link". This title exists for accessibility and organizational purposes.  
        </tr>
       -->

TO CANCEL A SESSION 
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

      Canceling a session means you will need to replace the <tr> class with a cancel class. After that you will add something like this to the title of the session: 
      <!--
      <tr class="cancel-session"> //You will replace the inPerson-session or zoom-session class with the cancel-class
        <td>&times; Session canceled DATE<br>Computer Science</td> //add the &times; elements, specify the cancelation and date, add a <br> to break the line, then leave the title of the session. 
      -->
      This process should be the same for inPerson and zoom sessions. 

