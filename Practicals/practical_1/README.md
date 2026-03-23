# URL Shortening Service — System Design Notes

## 1. Problem Statement Analysis

The problem on which this study is focused is the design of a URL shortening service, similar to TinyURL, where an elongated URL is shortened to a compact, abbreviated version, which is then redirectable to the original URL when requested to access it. While this problem may initially appear to be a simple transformation problem, the real challenge in this problem is the handling of large volumes of data and traffic. The system has to support 100 million new URLs each day, with a read-heavy workload where redirection is much higher in volume compared to creation. The problem, therefore, is an example of a problem in designing a distributed system, which is not just a programming problem.

## 2. Analysis of the Solutions Proposed by the Author

The author uses a systematic approach in solving the problem. First, understanding the problem and defining the requirements are done. Then, an estimate of the scope of the problem is provided. This gives an idea of the scope of the problem. The high-level design is proposed using RESTful APIs to create shortened URLs and redirects. This is a very popular approach in modern software systems. The usage of HTTP 301 and 302 redirects is discussed. This gives an idea of the design trade-offs involved in solving the problem. The database schema is discussed. The author begins with an ideal hash table solution and then moves to a relational database due to memory constraints. Two approaches are discussed for creating short URLs. Hashing with collision resolution and base 62 are discussed. However, base 62 is recommended because it is collision-free. Further enhancements are proposed in the form of caching to optimize reads, load balancing to optimize the system, and a distributed ID generator. These are some of the enhancements proposed in the solution.

## 3. Understanding

As discussed in this chapter, system design is not only about solving a problem but also involves breaking down a system into its constituent parts and designing those parts to ensure scalability. This chapter also demonstrates that system performance can be optimized based on usage patterns. In this case, systems with more reads are discussed. The chapter also demonstrates that an efficient way to create short URLs is by using base 62. It also demonstrates that basic concepts like caching and load balancing are important in maintaining system performance.

## 4. Areas of Confusion and Uncertainty

Throughout this chapter, various issues have been clarified; however, some concepts still remain unclear. Firstly, the concept of a distributed unique identifier generator has not been sufficiently discussed in terms of how it ensures uniqueness across all servers without any conflicts. Secondly, Bloom filters were mentioned in the system design; however, their functionality and potential sources of confusion were not sufficiently discussed. Thirdly, database sharding was mentioned in the system design; however, the process was not sufficiently discussed. Lastly, the concept of cache coherence was mentioned; however, it was not sufficiently discussed in terms of how it is enforced in the system.

## 5. Additional Topics for Inquiry

In order to gain a deeper and more comprehensive knowledge about this system, some topics that are related to it will also be explored. These topics include the concepts of distributed systems, the CAP theorem, cache systems such as Redis, load balancing techniques, distributed unique identifier generation techniques such as Snowflake, database sharding techniques, and database replication techniques. Exploring database replication techniques would also be beneficial in gaining a deeper and more comprehensive knowledge about the system.

## 6. Brief Assessment of Critical Analysis

The chapter offers a clear and systematic approach to the design of a URL shortener system, covering not only basic concepts of system design but also significant implementation aspects. The author succeeds in effectively presenting critical system design considerations that are fundamental to principled system engineering. The use of base-62 encoding instead of hashing is a significant case study that offers practical relevance to critical decision-making. However, there are some aspects that are touched on lightly, indicating that an in-depth analysis of the subject will be necessary to attain a comprehensive understanding. The chapter offers a great foundation for learning system design concepts, while at the same time recognizing that an extensive study of the subject, especially distributed systems, will be necessary to attain a deeper understanding.

