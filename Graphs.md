# How to read the ab gnuplot graphs

Have a look at the graphs used to present the test results:

![timeseries for requesting the root path with Node.JS](results/timeseriesNodeRoot.jpg)


The x-axis shows time. On the leftmost side we start our test and continue to move to the right over time. Once we reach the right boundary of the graph, the test is over.

Over the testing period numerous requests are sent to the server. These have a response time. Each request is depicted as a small plus sign on the chart. The y-axis shows how the it took the server to respond to a single request. If a plus is at the 250 line you know it took 250ms to respond to that request.

If there is a wide spread between pluses (from 50ms - 500ms for example) you know that requests are very much varying in response times. It is hard to predict a response time for a single request, we regard this as high variance. If there is almost a line or at least a small corridor we can tell there is little variance and high predictability for all requests.

If over time the response times become longer you know that the server gets distracted by requests and they somehow stack up. A gradually increasing response time is not desireable to sustain longer periods of high request numbers.
