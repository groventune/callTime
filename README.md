callTime
========
In online aural skills quizzes, I need to limit the number of times an audio file is played.
My solution is this:
Within each quiz question, I have a link which opens a pop-up window that auto-plays an embedded audio file (with no control bar) on launch and then closes the window using a javascript timer.
In the first window, there is also a javascript which counts the number of times the link has been clicked and disables it when the limit has been reached.

The problem is that if the page is refreshed, the counter gets reset as well.

However, the quiz itself has a clock.  There is another frame, separate from the main quiz content frame, which displays the elapsed time and the time left. 

I want to call this time-elapsed variable from within the quiz question when the page is launched.  If timeElapsed > 0, it means that this is a refresh and it will not reset the countdown timers.

Included are 2 files:
  CallTime is the source code for the frame that posts the elapsedTime.  The most relevant stuff starts at line 48.
  Quiz_question is a sample quiz question in the content frame in which I want to call the elapsedTime

callTime
