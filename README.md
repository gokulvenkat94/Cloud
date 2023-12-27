# Cloud



This code is used to remove snapshots with no active ec2 / volume id we can even change some values at the if condition syntax  to get the output of ec2 which is older
(ex : iterate through instace_response which will give you all the ec2 instances running in the account now give the if condition as instance id which is older and filter them with  your default 


instance_response = ec2.describe_instances(Filters=[
			{
				'Name': 'instnace-state-name',
				'Values': [
					'running',
				]
			},
		],

	activeinstance_id = set()
  for reservation in instance_response['Reservations']:
		for instance in reservation['Instances']:
			activeinstance_id.add(instance[InstanceId])




   
