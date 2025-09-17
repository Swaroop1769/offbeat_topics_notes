APM - Application Performance Management
What APM collects -  metrics 
Why APM - Reason to collect metrics - to improve performance, user experience, Reduce issues and errors
With APM we can monitor - Frontend, Backend & Infrastructure
How APM monitoring performed: collects M E L T (metrics, events, Logs, Traces) - monitors key performance indicators such as:  response time, error rate, resource usage, throughput and latency
Golden Signals of Monitoring -> Latency(how fast things are), Traffic(how busy things are), Saturation(things are full), Errors(where things go wrong) - S E L T

 Top APM tools in market: Dynatrace (enterprise focused and complex), new relic '
Datadog - single unified dashboard - end to end observability


Datadog is modern monitoring and security tool.
    - Performance improvement and user experience
    - All types of monitoring in one place
    - 600 built in integrations (AWS, Azure etc.)
Datadog gives us functionality to test our projects

How does Datadog collects Data?
Multiple ways to send data to Datadog
    - From Datadog Agent
    - Using Datadog API
    - Integrations
How does it work?
works in 3 simple steps
    - Install and configure Datadog Agent in host(a server)
    - Server starts to send data (M E L T) to Datadog
    - Agents send this data to Datadog. With this data inside dashboards - alerts and queries
Important Benefit of Datadog : Everything is at one place
Able to monitor key aspects like Availability, Reliability, Scalability, Duration - S A R D

Datadog basic definitions:


-> Host: could be a server, VM, k8 Node. On server where Datadog is being installed.

-> Datadog Agent: is a software that runs on your hosts.
    - Datadog agent is heart of Datadog.
    - Agent acts like middle layer between app and Datadog website
    - Agent collects metrics, events from systems and apps.

-> Datadog Tags: way of adding dimensions to Datadog telemetries so they can be filtered, aggregated and compared in Datadog visualizations.
    - Example: have 2 hosts installed agents how to distinguish --> using Datadog tags: something like version: stage, version: prod
    - Datadog provides system tags but also gives us option to add custom tags.

Software Integration: combining two separate isolated software pieces to work together.

-> Right after installing the Datadog Agent on host, it starts collecting data(events and metrics) and sends to Datadog website where we can filter, aggregate and alert on information. F A A

2 Main components:
-> Collector: which collects data on your host for every 15 sec

-> Forwarder: sends data to Datadog over HTTPS

Main configuration file is datadog.yaml
Configuration files for integration - conf.d

Infrastructure Map --> where all the hosts will be listed!

Agent.metrics -> creates a dashboard with custom metrics focusing on the agent!

#After Datadog Agent is installed automatically it creates 5 Dashboards
    - Host Counts
    - Monitor Notifications Overview
    - System - Disk I/O
    - System - Metrics
    - System - Networking
Datadog Integration with Internet Information Server -  IIS - collects for active connections, bytes received, request count by HTTP method. Also sends service check for each site, letting you know whether it's up or down.

Metrics Explorer: for examining metrics in Datadog and present them in a graphic way.

Every submitted metrics against Datadog needs to have type (distributions, Counts, Gauge, Rate)

Metric Types effects how the metric values are displayed when queried as well as the associated graphing possibilities using 

##Metric Summary gives General Information whereas Metric explorer gives us the Graph.


Metrics Summary and Metric Types:
Metrics can be submitted in 3 ways:
    - Agent
    - DogStatsID (which comes with Agent)
    - Datadog HTTP's API
Datadog performs the following actions:
    1. Collects data in specific time interval
    2. Aggregate this data
    3. Send this data to Datadog and it will be presented as single point in graph.
Depending on how those aggregations are done we have different types of metrics:
    - Distributions (Distribution metric submission type represents the global statistical distribution of a set of values calculated across your entire distributed infrastructure in one time interval.)
    - Counts (host emits following values in a flush time interval: [1,1,1,2,2,2,3,3]. Agent will submit datapoint with 15 as a value)
    - Rates ([1,1,1,2,2,2,3,3]. Agent will submit single data point with 15 as a value)
    - Gauges ([71,71,71,71,71,71,71.5] Agent will submit data point with 71.5 as a value)

#every submitted metrics to Datadog needs to have a Type
Metric Type effects how the metric values are displayed when queried
Metric Summary gives more sort of General information whereas metric explorer gives graph.


Set up APM in host:
Suppose we developed an app and want Datadog to display data from application. Perform following steps:
    1. Datadog Agent installation
    2. APM Tracer client installation

In APM, a transaction trace gives detailed snapshot of single transaction in app. A transaction trace records the available function calls, database calls, and external calls. 
Application located in IIS will send data to Datadog.

APM mainly has:
    - Services
    - Service Map
    - Traces (APM -> Traces -> 1 Service (Individual row)-> Flame Graph)
    - Error Tracking
    - Profile Search (profile page where all the profile transactions are listed.)
    - Profile Aggregation (combining all the transactions)

In APM -> Services - > we get list of services, along with details like P50 Latency, P90 Latency, P99 Latency.
    
Service List in APM contains services (application, db server etc)
P50, P75,P90,P99 ---> these are nothing but P50 - 50% of all code inside our app are in this range of latency.

Insider service  we will have multiple components like latency - inside which contains APDEX(or application index), Requests and errors per second, etc.
 APDEX can be set per service - this is numerical measure of user satisfaction with performance of application.
Endpoints list all the request information inside our application.

Inside endpoint dashboard 
    - there's one important section - "Span Summary" - it gives info of all the inner calls, when main endpoint is executed.
    - Traces - is the places where we can see all the transactions inside the application. Every request placed is present in Traces tab(APM-> Traces). Traces are key part of APM. 
Inside Traces (clicking on an individual error/success one) - we get the Flame Graph

    - There's Traces Table - displays information of every single request in application.
    - On the left side pane - Facets - where we can filter the data - All the filtration options are called Facets.
    - If we click on single row in Traces table a new pop-up window is opened with more additional information. That graph is called - Flame Graph.
    - Flame Graph  = is a distributed Request trace, and it has information about each service code.
    - --> this is tracing to information 
    - Tags that we see inside Flame Graph are Datadog System Tags
Span List - contains information regarding the resources. 
Trace Map - something similar to service map - gives linkage, connection between different services and Data Flow.

Service Map:
    - Gives information on how different services communicate with each other.
    - Also gives general info regarding request, general latency and error rate.
Error Tracking:
    - Gives summary of errors of issues inside our application.
Datadog Profiling:
    - With profiling we can debug the code, it's like we can see method names, class names, line numbers and also all the Latency information associated with them.
    

    - With APM we get end to end application monitoring - end to end visibility to application architecture.

With APM we can collect and visualize front-end data along with full breakdown of backend and code-level activities.
Datadog tracing without limits is a unique no-sampling solution - no sampling every trace without limits.
For each request, we can easily pivot from traces to logs and metrics.
We can slice and dice app performance using any tags.
Datadog Continuous Profiler measures all production code all the time.
Correlate slow requests with code-hotspots.
APM works seamlessly with synthetic monitoring and Real User Monitoring
WatchDog automatically discovers unexpected issues.



