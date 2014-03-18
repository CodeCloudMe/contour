#### **formatter** : { function }

<% if(defaultValue !== "[object Object]") { %>*default: <%= defaultValue %>* <% }%>

A function that formats each value. The function should return a string which is a valid [format](#config_config.yAxis.labels.format). (The returned string can vary based on each value.)

The general form of a specifier is `[​[fill]align][sign][symbol][0][width][,][.precision][type]`. The exact definitions are identical to those [used in D3](https://github.com/mbostock/d3/wiki/Formatting#wiki-d3_format).

**Example:**

    new Contour({
        el: '.myLineChart',
        yAxis: { 
            labels : 
                { formatter: 
                    function (datum) { return datum + '%' }
                }
        }
      })
    .cartesian()
    .line(data)
    .tooltip()
    .render()

*[Try it.](<%= jsFiddleLink %>)*

<% if(notes) { %><%= notes %><% } %>

