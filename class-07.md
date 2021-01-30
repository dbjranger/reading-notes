Read
Domain Modeling
From the Duckett HTML book:

Chapter 6: “Tables” (pp.126-145)
From the Duckett JS Book:

Chapter 3: “Functions, Methods, and Objects” (pp.106-144)

- The <table> element is used to add tables to a web page.
- A table is drawn out row by row. Each row is created
with the <tr> element.
- Inside each row there are a number of cells represented by the <td> element (or <th> if it is a header).
- You can make cells of a table span more than one row or column using the rowspan and colspan attributes.
- For long tables you can split the table into a <thead>, <tbody>, and <tfoot>.
 
- Functions allow you to group a set of related statements together that represent a single task.
- Functions can take parameters (informatiorJ required to do their job) and may return a value.
- An object is a series of variables and functions that represent something from the world around you.
- In an object, variables are known as properties of the object; functions are known as methods of the object.
- Web browsers implement objects that represent both the browser window and the document loaded into the browser window.
- JavaScript also has several built-in objects such as
- String, Number, Math, and Date. Their properties and methods offer functionality that help you write scripts.
- Arrays and objects can be used to create complex data sets (and both can contain the other)

var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

EpicFailVideo.prototype.dailyLikes = function() {
  var viewers, percentage;

  viewers = this.generateRandom(10, 30) * this.epicRating;

  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }

  return Math.round(viewers * percentage);
}

EpicFailVideo.prototype.weeklyLikes = function() {
  var total = 0;

  for (var i = 0; i < 7; i++) {
    total += this.dailyLikes();
  }

  return total;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.weeklyLikes());
console.log(corgiFail.weeklyLikes());