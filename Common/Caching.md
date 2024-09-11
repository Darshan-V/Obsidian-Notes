***Caching is one of the things that is key in improving the performance of any system. Doesn't matter if it is frontend, backend, CPUs or our day to day devices, you will find them using caching in one way or the other***

## What is Caching?

Caching is saving the data temporarily, that you frequently access, in a storage i.e. cache, so that you don't need to make a complete request again to get the same data.

* Cache storage are usually faster and available closer to the processing unit e.g. frontend, backend.
![[Pasted image 20240902115520.png]]

## Why we need Caching?

We can understand the need of caching if we understand the key points above.

Let's understand the problem:

- Our primary databases are usually slow and it takes time to retrieve data from them.
- Request for frequently accessed data adds unnecessary overhead to our server.
- In mission critical systems, loads on our server & database needs to be reduced.
- Some queries & API calls are expensive and computing them again and again is not optimal.

Therefore, to keep above points in check, we add a layer of caching.

**Advantages of caching**

- Faster access of data results in better user experience
- Reduces latency: No need to access main DB again for same data
- Reduces workload on main DB & server making it cost effective
- In many cases, because data is cached, it is available offline.
- Saves bandwidth & leads to low network traffic.