Reading:

Assorted bits of documentation:
Read this article on the Chart.js API.
Chart.js docs: You’ll be needing these!
Read the following articles on the Canvas API.
- Basic usage
- Drawing shapes with canvas
- Applying styles and colors
- Drawing text
- https://www.freecodecamp.org/news/how-to-make-your-first-javascript-chart/

Knowing how to present to your audience effectively is critical.  As humans we have certain natural behaviors such as how sensationalism may catch our attention and draw us in vs. a more relevant topic that may be of more importance and value.  For this reason, it’s better when expressing data to have it in a chart vs. a table when possible so that it’s easier to visualize the data as a whole.  

Chart.js is a powerful tool that allows developers to present stunning charts and transitions out of the box.  It is open source, meaning it’s free, and it also offers responsiveness.

You can create responsive charts with JSCharting through a couple simple steps:

Define a <div> tag in the HTML file with a unique id.
Provide this id, data, and any other options when calling JSC.Chart() in the JavaScript file.

Step 1 - Add a blank chart

- The first zip file contains a blank starting point you can fill in as we go. If you get lost or confused, or want to skip ahead, the zip file at the end or throughout each section will bring you up to speed. If you wish to download all the files at once, see all-steps.zip instead.
Index.html and js/index.js

Step 2 - Experiment with you chart and test different values.
 
Step 3 - Prepare the data with CSV data format

- The file contains rows (lines) and each row represents a record or entry. Normally the first row of values contains the names of each comma separated value (column). Subsequent rows contain the values themselves.

Step 4 - Assemble all your data together in the chart

- The data handling section was the most difficult step, but that alone will enable you to manipulate and extract data of interest from any CSV file. This is where it all comes together and where you will feel a sense of accomplishment.
Start by adding a renderChart() function to the end of the index.js file. You will pass the series data to this function as an argument.
