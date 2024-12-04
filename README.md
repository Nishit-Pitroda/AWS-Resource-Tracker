# AWS-Resource-Tracker
This Bash Script is used to track AWS Resource Usage


!#/bin/bash

########################
#Author: Nishit
#Version: v1

#This Script Track AWS Resource Usage
########################

set -x

#AWS list buckets
aws s3 ls

#AWS List instances
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'

#AWS List Functions
aws lambda list-functions

#AWS List Users
aws iam list-users
