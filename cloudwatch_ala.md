# TASK

### AIM : I need to create one dashboard using cloudwatch and in that i want to create alert for any one ec2 and any one rds with 80% more CPU, storage and ram usage it will send alert mail 

* note: Dashboard have proper data visiulization on aws

#### Step 1: Set Up CloudWatch Metrics

1. Navigate to CloudWatch:

+ Go to the AWS Management Console and open the CloudWatch service.

2. Select Metrics:

+ In the CloudWatch console, navigate to Metrics and then select EC2 and RDS.

3. Choose Metrics: For both EC2 and RDS, select the instance(s) you want to monitor. Metrics to focus on include:

* CPU Utilization
* Disk Usage (Storage)
* Memory Utilization (RAM)



#### Step 2: Create CloudWatch Dashboards

1. Create a Dashboard:

+ In the CloudWatch console, go to Dashboards and click on Create dashboard.

2. Add Widgets:

+ Click on Add widget, then select the metrics you want to display 
+(e.g., CPU utilization, storage, memory).

+ Customize each widget to show data for the specific EC2 instances or RDS instances.

3. Arrange Widgets:

+ Arrange the widgets on the dashboard to create a visually appealing layout that makes it easy to monitor the metrics at a glance.


#### Step 3: Set Up CloudWatch Alarms

1. Create Alarms for EC2 Instances:

+ For each metric (CPU, storage, RAM):
Click on the metric graph in CloudWatch.
Click on Create Alarm.
Define the conditions (e.g., CPU usage > 80% for 5 minutes).
Set actions to Send notification to an Amazon SNS topic and choose or create an SNS topic for email notifications.

2. Create Alarms for RDS Instances:

+ Similarly, follow the steps above for RDS instances, selecting the appropriate metrics (CPU, storage, RAM).

#### Step 4: Configure Email Notifications

1. Set Up Amazon SNS Topic:

+ If you haven't already, create an Amazon SNS topic specifically for these alerts.
Subscribe to Email Notifications:

2. Subscribe your email address (or addresses) to the SNS topic you created.

+ This ensures you receive email notifications when alarms are triggered.

#### Step 5: Test and Validate
1. Test Alarms:

+ To ensure everything is set up correctly, you can intentionally trigger alarms (e.g., by increasing CPU load on an instance) and verify that you receive email notifications.