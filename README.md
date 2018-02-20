# D3.js-Notes
--------------
Selectors 
-----------
d3.select command is used to perform a single-element selection in D3.This method accepts a string that represents a valid CSS# selector or an element object if you already have a reference to the element you want to select. The d3.select command returns a D3 selection object on which you can chain modifer functions to manipulate the attribute, content, or inner HTML element.
[NOTE] more than one element can be selected using the selector, provided only the first element is returned in the selection.
selection.attr: 
  //set foo attribute to goo on p element
  d3.select("p").attr("foo", "goo");
  // get foo attribute on p element 
  d3.select("p").attr("foo");
  
  selection.classed : allows to add or remove CSS classes on the selected element(s)
  selection.style : add or remove style based on specefic name to the specefic value on the selected element(s).
  selection.html : this function let you modify the innerhtml of html element(s)
  
  SELECTING MULTIPLE ELEMENTS
  ---------------------------
  d3.selectAll
  eg: d3.selectAll("div").attr("class","first");
  
  ITERATING THROGH SELECTION
  ---------------------------
  de.selectAll("div").each(function(d, i) { console.log("Data: " + d + ", Index : " +i); d3.select(this).append("h1").text(i); });
  
  CHAPTER 3 :: DEALING WITH DATA
  ===============================
  Binding an array as data
  ------------------------
  [TIP] D3 injects a property to the DOM element named __data__ to make data sticky with visual elements so when selections are made using a modified dataset, D3 can compute the difference and intersection correctly. You can see this property easily if you inspect the DOM element either visually using a debugger or programmatically.
  
  
