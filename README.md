# learn_d3
Learning D3JS

D3 = Data Driven Documents

The "data" can be anything.

The "documents" is the DOM.


[https://davidwalsh.name/learning-d3](https://davidwalsh.name/learning-d3)


1. Based on SVGs
    a. Canvas
    b. Shapes
    c. (0,0) = top-left
    
2. Data Binding
    a. selection return arrays (maybe empty)
    b. selections are acted upon

3. Scales
    a. domain ~ inputs interval (min-max)
    b. range ~ outputs interval (min-max)
    c. linear, log, time, ordinal, band

4. Margins & Axes
    a. Axes are attached to whichever element they're called on
    b. Margins are necessary to view all data

5. General Update Pattern
    1. JOIN new data w/ existing data
    2. EXIT to remove missing data elements
    3. UPDATE old elements w/ new data
    4. ENTER to add new data elements

```
var viz = g.selectAll("whatever")
    .data(data);

viz.exit().remove()

viz
    .attr("somex", function(d){ return x(d.gpa0) })
    .attr("somey", function(d){ return y(d.gpa1) })

viz.enter()
    .append("whatever")
        .attr("somex", function(d){ return x(d.gpa0) })
        .attr("somey", function(d){ return y(d.gpa1) })
```

[https://www.d3indepth.com/introduction/](https://www.d3indepth.com/introduction/)
