**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

#### Run `kubectl` command to show the running pods and services for the three components. Copy and paste the output or take a screenshot of the output and include it here to verify the installation

#### Successfully install Grafana, Prometheus, and Jaeger.

![alt text](https://github.com/fthiagomedeiros/CNAND_nd064_C4_Observability_Starter_Files/blob/master/Project_Starter_Files-Building_a_Metrics_Dashboard/images/01.%20ProjectAndClusterStaging/01.%20pods_prometheus_grafana_jaeger.png?raw=true "Successfully install Grafana, Prometheus, and Jaeger.")


#### Successfully access Grafana’s web UI.

![alt text](https://github.com/fthiagomedeiros/CNAND_nd064_C4_Observability_Starter_Files/blob/master/Project_Starter_Files-Building_a_Metrics_Dashboard/images/01.%20ProjectAndClusterStaging/02.%20grafana_login_home.png?raw=true "Successfully access Grafana’s web UI.")


#### Locate and share an observability dashboard.

![alt text](https://github.com/fthiagomedeiros/CNAND_nd064_C4_Observability_Starter_Files/blob/master/Project_Starter_Files-Building_a_Metrics_Dashboard/images/01.%20ProjectAndClusterStaging/03.%20grafanadashboard.png?raw=true "Locate and share an observability dashboard.")

_______________________

## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
_______________________


## Describe SLO/SLI
**_*TODO:* Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*._**

SLIs are indicators that garantee we have reached the SLO. For instance, __the SLO is__ **"the service has an monthly uptime of 99.99%."**. It means we expect that in the period of a month, our service will be available 99.99% of the time. To confirm that we have reached this objective, we must evaluate the error rates in order to know if the uptime in the last month was the expected. 

The same as said previously, can be used for request response time. For instance, __the SLO is__ **"the service has a request response time of 200ms monthly".** It means we expect each request response (in average) must be 200ms. The SLI indicates that we have reached the expected value from SLO.

## Creating SLI metrics.
**_*TODO:* It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs.**

A Service-Level Indicator (SLI) is a specific metric used to measure the performance of a service. These metrics are relevant and built around the Four Golden Signals (Latency, Error Rates, Traffic, Saturation)

* the SLO may be **latency**. The SLI will be the time a **request takes to complete**. We have to trace the time each request takes to complete and order to have an average for that.
* the SLO may be **uptime**. The SLI for that must be the how many **error messages** we are seeing in the periof of time. Tha value indicates if we reached the SLO.
* the SLO may be **saturation**. The SLI for that must be the **usage of memory** cannot go above 80% or measuring the **CPU saturation** on order to avoid the effects caused by CPU utilization. Both of these metrics are directly related to system performance.
* the SLO may be **traffic**. The SLI indicates that **the number of requests** processed successfully in a specifi period of time.





## Create a Dashboard to measure our SLIs
*TODO:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.

## Tracing our Flask App
*TODO:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here.

## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.

## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue.

TROUBLE TICKET

Name:

Date:

Subject:

Affected Area:

Severity:

Description:


## Creating SLIs and SLOs
*TODO:* We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name three SLIs that you would use to measure the success of this SLO.

## Building KPIs for our plan
*TODO*: Now that we have our SLIs and SLOs, create KPIs to accurately measure these metrics. We will make a dashboard for this, but first write them down here.

## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  
