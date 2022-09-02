# Introducing Cloud Architecture

## Well-Architected Framework

![](attachments/Pasted%20image%2020220902083341.png)  
.  

A guide that is designed to help you build the most secure, high-performing, resilient, and efficient infrastructure possible for your cloud applications and workloads.

- **Security**: the ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies. The implementation: strong identity foundation, enable traceability, security at all layers, automate security best practices,and protect data in transit and at rest.

- **Operational Excellence**: the ability to run systems and gain insight into their operations to deliver business value. It also addresses the ability to continuously improve supporting processes and procedures. 
	- Aware how it will be deployed, updated, and operated.
	- Implementing engineering practices to reduce defect and do quick safe fixes.
	- Enable observation through logging, instrumentation, and business technical metrics.
 
- **Reliability**: the ability of a system to recover from infrastructure or service disruptions and dynamically acquire computing resources to meet demand. It also addresses the ability of a system to mitigate disruptions such as misconfigurations or transient network issues.
  
- **Performance Efficiency**: o maximize your performance by using computation resources efficiently. You also want to maintain that efficiency as the demand changes.
	- Consider using a vendor to any technology that difficult to implement yourself.
	- Mechanical sympathy: use a tool or system with an understanding of how it operates best. Use the technology approach that aligns best to what you are trying to achieve. i.e. consider data access patterns when you select database or storage approaches.
  
- **Cost Optimization**: ongoing requirement of any good architectural design. The process is iterative, and it should be refined and improved throughout your production lifetime.
	- Measure efficiency
	- Eliminate unneeded expense
	- Consider using managed services

## Best Practices for Building Solution
Design tradeoffs:
- Trade consistency, durability, and space for time and latency to deliver higher performance, prioritize speed to market of new features over cost.
- Benchmarking to achieve cost-optimal workload.
- Must be based on design decisions on empiricaal data.

Scalability: ensure that your architecture can handle changes in demand.
- Bad design (anti-pattern): Administrator manually launches new server after users can not access application.
- EC2 Auto Scaling react based on alarm after EC2 reach its threshold, so new server is ready before capacity is reached.
- For monitoring solution there is Amazon CloudWatch. Example usage: the threshold is when CPU utilization stayed above 60% for longer than 5 minutes.
- When alarm is triggered, Amazon EC2 Auto Scaling immediately launches a new instance.
- You should  also design system to scale in when demand drops off.

Automate: where is possible, automate the provisioning, termination, and configuration of resources.
- Anti-pattern: When application server crashes, users manually notify administrator and administrator manually launches and configures new server.
- When application server crashes, Amazon CloudWatch can automatically detect it, notifies administrator. Amazon EC2 Auto Scaling can automatically launches and configures identical server. It can also automatically logs action to a change management solution.

Treat resources as disposable: taking advantage of provisioned nature of cloud computing.
- Thinking infrastructure as software instead of hardware (flexible and easier to upgrade)
- Think that it is easy to migrate between instances or other resources, so you can quickly respond to changes.

Use loosely coupled components: Architecture with independent components.

Design services not servers

Choose the right database solution

Avoid single points of failure

Optimize for cost

Use caching

Secure your entire infrastructure
## References
- https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf
- [Security Pillar Whitepaper](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [Operational Excellence Pillar](https://d1.awsstatic.com/whitepapers/architecture/AWS-Operational-Excellence-Pillar.pdf)
- https://d1.awsstatic.com/whitepapers/architecture/AWS-Reliability-Pillar.pdf
- https://d1.awsstatic.com/whitepapers/architecture/AWS-Performance-Efficiency-Pillar.pdf
