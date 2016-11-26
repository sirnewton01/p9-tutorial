Graphics
===

Plan 9 has built-in graphics capabilities. There are system commands that are capable of rendering and manipulating raster graphics. The raster graphics are easily converted to popular formats such as GIF, PNG and JPG using tools. Finally, you can use certain simple text formats to draw. 

For example, let's assume that you have a document with a series of data in it. There is a tool called graph(1) that will take a series of x/y points and graph them as a line using a series of drawing commands. There is another tool called plot(1) that will take a series of drawing commands and render it in a window. The two can be piped together to  Select the data series and then click and drag using the middle mouse button the command to run the command on the selected input. If you want to customize the output check out the various command line options for the two commands to change colours, add labels for the axes, etc.

    1	10.13
    2	4.8
    3	16.0011

    > graph > /tmp/graph.plot; window plot /tmp/graph.plot

