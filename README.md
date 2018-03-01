# usefulawsclicalls


# Intro

this list is a reminder for me and may help others. I will add to it 


### List all stopped instances in the london region.  print only thier Id, platform and machine type


    $ aws ec2 describe-instances --profile myprofile --region=eu-west-2 --query 'Reservations[*].Instances[*].[InstanceId,State.Name,Platform,InstanceType]' --filters "Name=instance-state-name,Values=stopped" --output text
