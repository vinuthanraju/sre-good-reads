# Monitoring vs Observability: 

Let’s understand the difference

Say you’re releasing a new microservice in production.

You already know a list of things that can go wrong so you keep an eye on them. Eg- CPU or memory saturation, high latency or error rate, etc.
Your dashboard shows you these real-time metrics. You get alerted anytime any threshold is crossed, then you mitigate the issue. Good.

But life is more complicated 😐

The microservice you just launched is now intertwined with 100s of other services that talk to each-other to make your system work.

Let’s say this is a Payments System. What happens when your user clicks “Pay” and it doesn’t work?
Your existing metric dashboards are all green. It's impractical to guess the error or go through millions of logs from all services. So how do you debug where the fault lies? 😰

💡 You might use the request’s unique ID to trace it through all the services it passes and analyze the corresponding logs & metrics to spot the culprit.

Keeping the above example in mind, let’s define the two:


👉 Monitoring is keeping an eye on the system’s health, performance & availability and alerting on KNOWN issues. It is a reactive approach, ie, we react when a threshold is crossed and try to re-stabilize the system.

👉 Observability captures the entire state of a system so we can explore UNKNOWN unknowns. It correlates data from different sources like Logs, Metrics & Traces so we can find patterns and root causes in our system. This makes it a proactive approach.

❗ One is not better than the other, both work in tandem to make systems more reliable.