## This are D3-interactive-charts lesson (from Code Institute Full-Stack Diploma course). Transcription from lessons, included in comments sections in the code. 

# D3 Interactive Charts.

1. What is it?

D3 Interactive Chart.

2. What does it do?

Visually updates based on the variation of data bound to the SVG elements.

3. How do you use it?

Filter the data based on click events and text based input from HTML buttons and a textfield.


LESSON:
Now let's play with an example where the data set changes dynamically. In this
example we have created two buttons and a text field that allow us
to filter and modify the data the data by the way is generated randomly between
a value of 1 and 500 we can also filter in the data based on values entered into
the text field so how does this work so you can see here on line 16 17 and 18
we've got our two buttons and our inputs and the on click events are wired up for
two of the buttons let's have a look so before we get to that we can see that
this our familiar set up is in place our heights and our our weights and so on
now the very first thing that's called before we click the buttons is to change
data that generates our data first time and how that data is
generator well it generates a random set of data and sets it as the bar chart
it's called on page load and then each time the bottom is clicked here's our
random data it's built up using a random data set and pushed to an array that
array then is returned to any code that invokes it
let's have a look at the filter data so it filters the data before plotting into
the bar chart and it removes any bars less than the value in the filter input
box you can see there anything greater than or equal to the filter value gets
returned anything less than doesn't make it
now let's have a look at plot data so in order to plot the data it takes in a
parameter of data itself and it binds our rectangles to the data set passed in
once it does that it cleans out any previous or unneeded rectangles and
labels if the data has less items in the existing chart on line 72 and 73 you can
see exit and remove it's the opposite of enter it's a way of removing the
bindings between the data and the corresponding rectangles are
corresponding SVG objects we then invoke create bars and create labels these are
custom functions we create ourselves there's a create bars bars enter and
append to the rectangle again these bars are passed in as parameters create
labels takes in labels parameter and it binds the the text similar to what we
were doing in earlier units when we're creating a text object
let's have a look resize bars and position labels so the resize bars it
has a transition and a duration of 500 milliseconds see that's what gives you
the nice fluid transitioning between the bar rendering so it takes 500
milliseconds to bind the data and render the the bars with their newly bound data
okay let's look at what we have an overview again and it's all bound to a
div nothing new here so we have our two buttons in input we have on click event
handlers and our custom event handler is our change data and filter data and they
kick off the process
