# RDS

## Pricing
<details>
  <summary>
RDS Pricing
  </summary>
RDS pricing depends on 3 things:

* *Instance hours*: type of RDS instance and # of hours it is active in a month
* *Storage*: Database size in GB.
* *IOPS*: Amount of provisioned IOPS (input/output operations per second)

There are two major type of instances that you can choose:
* *General Purpose (SSD)*: Most commonly used, ideal for broad range of workloads. You do not pay for IOPS, only for instance hours and storage. You get baseline IOPS proportional to storage (3 IOPS per GB). Additionally you get burstable performance at 3000 IOPS.
* *Provisioned IOPS*: Used for I/O intensive workloads. You explicitly specify provisioned IOPS & storage, pay for them separately.

</details>

## Cost optimization tips
<details>
  <summary>
Reserved Instances (RIs)
  </summary>

### Reserved Instances (RIs)
You can get RIs for RDS the [same way as EC2](ec2.md#use-reserved-instances-ris). All considerations and benefits of RIs apply.
</details>
<br>


<details>
  <summary>
Turn DB on/off with AWS Instance Scheduler
  </summary>

### Turn DB on/off with AWS Instance Scheduler
You can specify start and stop timing for RDS instances the [same way as EC2](ec2.md#turn-machines-onoff-with-aws-instance-scheduler). This is useful for non production databases.
</details>
<br>


<details>
  <summary>
Increase storage to get more IOPS
  </summary>

### Increase storage to get more IOPS
Sometimes it’s cheaper to pay for more storage than IOPS so you might consider increasing storage capacity. With increased storage burst capacity also replenishes faster.
</details>
<br>


<details>
  <summary>
Keep provisioned storage in check
  </summary>

### Keep provisioned storage in check
You can increase the storage with a click of a button. But decreasing RDS storage is not directly supported and the manual process is painful and will likely have some downtime.
</details>
<br>


<details>
  <summary>
Monitor the instance type
  </summary>

### Monitor the instance type
Periodically check CPU and memory utilization to see if the resources are getting utilized properly. If CPU or memory utilization is too low adjust the instance size and/or type.
</details>
<br>