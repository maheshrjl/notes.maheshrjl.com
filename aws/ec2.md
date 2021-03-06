# 💻 EC2

### <mark style="color:blue;">Instance Types</mark>

* M : General Purpose i.e. app server
* T :  Micro instances - Low cost, general purpose, web servers
* C, D, I : CPU/IOPS Optimised, good for memory intensive compute
* R, X : Memory Optimised
* G, P : GPU
* F: FGPA - Field programmable gate array, for hardware accleration of code&#x20;

### <mark style="color:orange;">Instance Options</mark>

#### On Demand Instance:

* Pay a fixed rate per hour. Good for apps where compute needs scaling up/down

#### Spot Instance:

* Can be extremely cheap
* Can be terminated by AWS any time
* Best for jobs that can be terminated at any time eg: batch processing
* Not charged for partial hour if terminated by AWS but, charged for full hour if user terminated

<details>

<summary>Spot Instances &#x26; Spot Fleet</summary>

#### EC2 Spot Instance Request:

* Can get a discount of 90% compared to on-demand
* Define a max spot price & get the instance while current spot price  < max

</details>

#### Reserved instance:

* Fixed compute, resverved for a certain period of time. Cheaper than on-demand if used for predicatable long term. (1 or 3 years)

#### Dedicated Host:&#x20;

* Physical EC2 server are available only to customer. Used when regulatory requirements specify that you must not be using multi-tenant computing.

#### Dedicated instance:

* EC2 instances running on hardware dedicated to a single customer
* Hardware can be shared with other instances in the same account
* No control over instance placement

### <mark style="color:purple;">Security Group</mark>

* Control how traffic is allowed into or out of ec2 instances
* Security groups contain allow rules only
* Rules can be referenced by IP or by security group
* Can be attached to multiple instances
* Locked down to a single region/vpc
* All inbound traffic is blocked & outbound traffic is allowed by default
* They control:
  * Access to Ports
  * Authrozied IPv4 & IPv6 address ranges
  * Control of inbound network (from outside to the instance)
  * Control of outbound network (from the instance to outside)

{% hint style="info" %}
If a page is continously loading (timeout) it is most likely a security group issue.
{% endhint %}
