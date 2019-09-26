# Utility function to Clear Partitioned Region

This functions clear data from a Partitioned Region

Step 1: Build the maven project to create the jar

```
mvn clean package
```

Step 2: Deploy the jar on to Cloud Cache cluster using GFSH
Note: first you have to connect to the cluster where jar needs to be deployed

```
deploy --jar=target/geode-function-partitioned-region-clear-1.0.0.jar
```

Step 3: Delete the data in a region using following command

```
execute function --id=ClearPartitionRegion --region=[region_name]
```
