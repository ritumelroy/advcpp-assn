# C++ course projects summary

For my C++ course we had 2 main projects. Due to school and course policy I cannot upload the full folders that I submitted. So below is some writeup and screenshots.

1. filtered string view

Write a more complex version of the string_view described above - the filtered_string_view.
A filtered_string_view is like a string_view, however it presents a filtered view of the underlying data. This means that readers of the filtered_string_view may only see part of the underlying data.
The filter is optionally provided by the caller as a predicate (a function which returns a boolean) which returns true if the data is to be kept. If not provided, the filter will default to the "true" predicate, i.e., a function which always returns true. In this case, no data would be filtered.

To do this, I also created my own iterator.
![alt text](ss1.png)

I achieved this using simple functions. Below is screenshots from the .h file to demonstrate.
![alt text](ss2.png)

Here are some tests I wrote as part of the project
![alt text](test1.png)
![alt text](test2.png)

2. This project got us to write a generic directed weighted graph (GDWG) with value-semantics in C++. Both the data stored at a node and the weight stored at an edge will be parameterised types. The types may be different. For example, a graph with nodes storing std::string and edges weighted by int.

For this assignment, memory management using C++ pointers were crucial. They were quite a headache but once I sorted out my internal representation I got it under control.

I had to use abstract class for Edge of the graph.

![alt text](a2-ss1.png)

We also had to work almost always with templates for this assignment.

The other main thing I learnt from this assignment was using my custom struct to define how to compare the std::set. Here are some of it's screenshots

![alt text](a2-ss2.png)

Here is how I defined my custom iterator.

![alt text](a2-ss3.png)

Here is how I defined my graph DS.

![alt text](a2-ss4.png)

Here are some examples of my tests using Catch2 test suit:

![alt text](a2-ss5.png)

![alt text](a2-ss6.png)
