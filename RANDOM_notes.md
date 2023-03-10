RANDOM NOTES
===============

1. Create EC2 jumpbox
    - verify in the EC2's SG that the correct "My IP" was added
    - can use "google what's my IP" to verify

2. mysql -u <username> -p -h <cluster-hostname>
    - can use the Reachability Analyzer tool on the Network Interfaces page
    - may have to manually set password in the RDS

3. Verify that there is a SG for ECS from the RDS perspective
    - look on the overview tab for the RDS instance you are interested in