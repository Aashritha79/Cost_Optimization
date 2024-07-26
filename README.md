<h2><b>Unused AWS Volume Snapshot Cleanup</b></h2>
<h5>About the project:</h5>
This project is designed to optimize storage costs by automatically managing and deleting stale Amazon Elastic Block Store (EBS) snapshots. The function scans all EBS snapshots owned by the account and identifies those not associated with any active EC2 instances. It then deletes these unneeded snapshots, freeing up storage space and reducing costs.<br>
<br>
<h3>Functionality</h3>
<b>1.	Retrieve EBS Snapshots:</b>
The Lambda function fetches a list of all EBS snapshots owned by the account.<br>
<b>2.	Identify Active EC2 Instances:</b>
	It also retrieves a list of all currently active EC2 instances.
<br><b>3.	Check Snapshot Associations:</b>
	For each snapshot, the function checks if the associated volume is attached to any active EC2 instance.
<br><b>4.	Delete Stale Snapshots:</b>
	If the volume associated with the snapshot is not attached to any active instance, or if the volume itself is missing, the function deletes the snapshot.
<h3>Benefits</h3>
	<b>Cost Optimization:</b> By deleting unneeded EBS snapshots, the function helps in reducing unnecessary storage costs.
<h3>Usage</h3>
<b>To deploy and use this Lambda function, follow these steps:</b><br>
<b>1.	Deploy the Lambda Function:</b>Use the AWS Management Console or AWS CLI.<br>
<b>2.	Configure Permissions:</b>Ensure that the Lambda function has the necessary IAM permissions to describe and delete EBS snapshots and to describe EC2 instances.<br>

