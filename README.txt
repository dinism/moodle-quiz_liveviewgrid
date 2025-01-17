# moodle-quiz_liveviewgrid
Dynamic quiz spreadsheet. <br />
This version v1.2.0 (2019032000) is compatible for Moodle 3.2+.<br />
This quiz report module allows teachers to see, in real time, 
the responses from students as they are completing questions in a quiz.
 As students change their answers or submit more answers, the spreadsheet is refreshed. 
 If desired, the grades that each response would be given can be shown as the background color in the cells of the spreadsheet, 
 but this action is unrelated to the grading of the quiz.
The top row in this spreadsheet/table has the names of the questions in the quiz. 
The teacher can click on any of these question names to obtain an overview of that question.
For multichoice, truefalse, and calculatedmulti question types, a histogram is displayed.
For all other question types, the response from each student is given in one line on the page. 
The teacher can choose to show or hide the student's name associated with each response.<br />
To install this module, place the liveviewgrid directory as a sub-directory in the <your moodle site>/mod/quiz/report/ directory, 
creating the <your moodle site>/mod/quiz/report/liveviewgrid/ directory.
After installing this quiz report module,
 teachers can click on the "Live Report" option in the "Report" drop-down menu to access this spreadsheet.
Changes for version 1.1.3. Spreadsheet handles Cloze questions, has better formatting for tooltips,
  the students can be sorted by last or first name, results can be shown by group or all responses.
  Added "....' to long (truncated) answers to let the teacher know that the tooltip would show more of the answer.
Changes for version 1.2.0. Handles groups properly, including limiting teacher view unless accessallgroups is enabled.
Changes for version 1.2.1. Tooltips now work for touchscreen laptops using Firefos browser.
Changes for version 1.2.4. Shows groups in dropdown menu, only shows groups to teachers that they are allowed to see,
  changed settings links to buttons, and made all information and help strings into tooltips.
  Also, now supports a compact view of the table. In this view the question texts that are truncated have tooltips.
  The page for essay questions now displays in a table, one row per student.
Changes for version 1.2.5. The question names are now buttons with tooltips. 
  If a teacher clicks on a button, the single question page is displayed with the buttons from the standard page.
Changes for version 1.2.6. The teacher now has the option to show/hide student names and show/hide correct answers.
Changes for version 1.2.7. The question tooltip now has both question name and questiontext. Truncate splits on entire symbols. 
Changes for version 1.2.8. If evaluate is set, the histogram bars are now colored according to how correct they are.
   To do this I created a revised version of the lib/graphlib.php file, liveviewgrid/classes/quiz_liveviewgrid_graphlib.php.
Changes for version 1.2.9. If a teacher attempts the quiz (preview) their resonses no longer show up.
   Percentages of students vs class enrollment are displayed on the bars. If show names is set in single question view,
   the student name shown on the bars. Dropdown menus submit on change of value. Current value not shown.
   Tooltips show complete choice options on the x-axis legend. These changes required displaying image in iframe.
Changes for version 1.2.10. Removed bug in tooltip_histogram.php.
Changes for eersion 1.2.11. Removed hardcoded URL bug.
Changes for version 1.2.12. Made navigations workgin clearer, iframe a little wider and align left, and truncate=1 for compact view.
Changes for version 1.2.13. Made a new file, liveviewpopout.php to provide a static page for comaprison and printing.
Changes for version 1.2.14. Removed links to other pages from liveviewpopout.php, added a print button.
Changes for version 1.2.24. Changed the options so that they are radio buttons that can be hidden and displayed.
Changes for version 1.2.25. Changed some of the language srings to make things clearer.
Changes for version 1.2.26. Moved options to a table that could be hidden or shown.
Changes for version 1.2.27. Removed bug (group added in to option form) and changed color to colour in strings.
Changes for version 1.2.30. Changed the "Refresh Page" text to a button,
     added session values so that the options would follow the user, 
     and added || $qattemptstep->state == 'todo' in locallib to handle preferredbehaviour=immediatefeedback.
Changes for version 1.2.32. Added a feature so that teachers could see the progress students were making in a quiz.
Changes for version 1.2.33. Don't carry singleqid to the next quiz.
Changes for version 1.2.38. Checked against Moodle coding guidelines and remove all reference to lesson module.
Changes for version 1.2.40. Put back in reference to lesson and checked against Moodle coding guidelines.
Changes for version 1.2.41. Added in the "Back to all qustions" button.
Changes for version 1.2.42. Added in the option for teachers to select the refresh time and to see progress in lessons.
Changes for version 1.2.43. Changed code so that the group is not carried as a session value.
Versions in-between here: Added back button, added checks to be sure answer exists.
Changes for version 1.3.0  Added page for all responses (allresponse.php, singleq_histogram.php, qidhash.php, javascript_teach_refreshG3.js.
This version will refresh the individual iframes without refreshing the entire page. Changed the default for $refresht to 3.
Changes for version 1.3.2 Corrected bug that carried values of the $response array from one user to the other. $response = array(); in locallib.php, line 295.
Changes for version 1.3.3 Changed default values for rag, evaluate, showkey, and compact = 1