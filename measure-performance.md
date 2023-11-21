# Measuring Performance

**ResponseTime** is the total time taken for a request to be serviced as seen by the requestor. It usually includes:
- Time taken (T1) to send the request (from the client to the server)
- Time (T2) that the request is waiting in queue to be processed.
- Time taken (T3) to actually service the request.
- Time taken (T4) to send the response (from the server to the client)

T1 and T4 are purely *network delays* where as T2 is the *queueing delay*. T3 is the actual *service time*. T1 + T2 + T4 is actually the request *latency*.

**Throughput** is the number of requests processed in a given amount of time. How to measure throughput of a service?
- Run the request *n* times. Add all the response times and divide by *n* to get the *mean response time*. Or it can be said that 50% of the request will complete in less than the *mean response time*.
- The above metric does not work well with outliers and better answers are expected. One common approach is to use *percentiles*. *n-percentile time* is the time in which n% of requests will complete. The *mean response time* could be looked at as 50-percentile. If 95-percentile time of a service is 500 millisecond, it means 95% of the requests will complete in 500 milliseconds.
