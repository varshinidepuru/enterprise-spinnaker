# Instructions

Please follow these instructions to get the logs all ISD Services and Number of Users logged in ISD, Number of Applications,Pipelines,Cloud Targets and Number of Pipelines executed per day.

Create secrets mentioned below if spinnakerStorage is sql.**NOTE**: Do not change the name of the Secret
   - `kubectl -n opsmx-isd create secret generic mysqlcredentials --from-literal host=PUT_YOUR_MYSQL_HOST_NAME --from-literal username=PUT_YOUR_MYSQL_USER_NAME --from-literal password=PUT_YOUR_MYSQL_PASSWORD`

Read the comments in the yaml file and Execute below commands, by repalcing the namespace

- `kubectl -n opsmx-isd apply -f job.yaml` # Change the namespace accordingly default is "opsmx-isd"

    - Once pod will completed so please check the pod logs to verify the logs are publised to opsmx-jfrog or not.

      `kubectl -n opsmx-isd logs isd-info-xxx` #Replacing the name of the pod name correctly
