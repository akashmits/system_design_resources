
#1:Scatter And Gather Pattern

Let's say we have a process-heavy task like video compression.

We get a video and have to compress it into 5 different resolutions such as 240p, 360p, 480, 720p, and 1080p.

We have a single image compression service that takes in the video and processes each resolution sequentially. The problem here is that it's very slow.

The scatter-gather pattern advises us to run multiple of these processes simultaneously and gather all the results in one place.

So for our video process examples, this is how it will look:

Scatter – We will divide the task into multiple nodes, so one node will take care of compressing the video into 240p, another to 360p, and so on.
Process – Each node will compress its video individually and simultaneously.
Gather – Once all the nodes have finished compressing the videos, the videos will be stored on some server and we collect the links for all the different versions.
Instead of waiting for each of our videos to be compressed sequentially, now we can parallelize this whole process and increase performance significantly.

Pros
Parallel Processing – The scatter-gather pattern improves performance by enables parallel processing of subtasks. Tasks can execute concurrently across multiple nodes or processors.
Scalability – The scatter gather pattern allows us to scale horizontally, the higher our workload, the more nodes we provision.
Fault Tolerance – This pattern enhances fault tolerance by redistributing failed subtasks to other available nodes, ensuring the overall task can still be completed successfully.
Resource Utilization – The scatter-gather pattern optimizes resource utilization by efficiently leveraging available computational resources across multiple nodes or processors.
Cons
Communication Overhead – This pattern involves communication between nodes which introduce potential latency and network congestion that may impact overall performance, especially with large data volumes.
Load Balancing – Balancing the workload evenly across nodes can be challenging, leading to potential inefficiencies and performance bottlenecks if some nodes are idle while others are overloaded.
Complexity – This pattern is not easy to implement and adds an aditional layer of complexity to the system. It requires careful planning and synchronization mechanisms to coordinate subtasks.
Data Dependency – Handling dependencies among subtasks, where the output of one subtask is needed as input for another, can be more complex in the scatter-gather pattern compared to other patterns.
Use Cases
The scatter-gather pattern is useful in distributed systems and parallel computing scenarios where you can divide tasks into smaller subtasks that can be performed concurrently across multiple nodes and processors.

Here are some use cases where the scatter-gather pattern can be used:

Web Crawling – You can use the scatter gather pattern to fetch and crawl multiple web pages concurrently.
Data Analytics – Apply scatter-gather to divide large datasets into chunks for parallel processing in data analysis tasks, combining individual results for final insights.
Image/Video Processing – Utilize scatter-gather for distributed image/video processing, such as encoding frames in parallel and gathering results for the final output.
Distributed Search – Implement scatter-gather in distributed search systems to distribute search queries across nodes, gather and rank results for final search output.
Machine Learning – Apply scatter-gather in distributed machine learning for parallel model training on scattered data and combining models for final trained model.
MapReduce – Incorporate scatter-gather in the MapReduce model for big data processing, scattering input, parallel processing of intermediate results, and gathering for final output.
