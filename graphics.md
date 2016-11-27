Graphics
===

Plan 9 has built-in graphics capabilities. There are system commands that are capable of rendering and manipulating raster graphics. The raster graphics are easily converted to popular formats such as GIF, PNG and JPG using tools. Finally, you can use certain simple text formats to draw. 

For example, let's assume that you have a document with a series of data in it. There is a tool called graph(1) that will take a series of x/y points and graph them as a line using a series of drawing commands. There is another tool called plot(1) that will take a series of drawing commands and render it in a window. The two can be piped together to  Select the data series with your left mouse button and then click and drag using the middle mouse button the command to run the command on the selected input. If you want to customize the output check out the various command line options for the two commands to change colours, add labels for the axes, etc.

    1	10.13
    2	4.8
    3	16.0011

    > graph > /tmp/graph.plot && window plot /tmp/graph.plot

Let's try doing some raw drawing commands to print a red unit circle with x and y axis lines. Details about the commands can be found in plot(6).

    o
    ra  -1.0  -1.0  1.0  1.0
    e
    co  r
    cf  r
    di  0.0  0.0  1.01
    co  k
    li  0.0  -1.0  0.0  1.0
    li  -1.0  0.0  1.0  0.0
    cl

    > cat > /tmp/pic.plot && window plot /tmp/pic.plot

This next example involves a two step process. Let's first generate a set of x and y coordinates for a sine wave within this document. Once we have the table, we can use graph and plot to draw it. Click on the line below this command and then middle-click select the command. The math tool bc(1) is used to calculate the sine values. The output is generated where you put the cursor. The special '<' character at the beginning of the command does that.

    < for (i in `{seq 0 0.1 6.28}) { echo '    '^$i^'	'^`{ echo 'print s('^$i^')' | bc -l -s} }



Now, select the table and middle-click select this command to plot it.

    > graph -g 1 > /tmp/graph.plot && window plot /tmp/graph.plot

In this tutorial, you have seen how to use selected text as input to commands using the special '>' character at the beginning of the command. Tabular data can be sent to the graph command, which outputs plot commands to the plot command to render the graph. If you like, you can even write your own drawing commands directly to plot. There is also a special command prefix '<' that can insert the output from the command directly in your document where the cursor is located. To read more about these special prefixes in acme(1).
