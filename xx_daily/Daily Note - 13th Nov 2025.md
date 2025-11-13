---
date: 2025-11-13
tags:
  - daily
banner: "![[media/calendar.jpeg]]"
banner-height: 150
banner-x: 5
banner-y: 42
icon: 📆
banner-display: cover
content-start: 151
---
## Tasks

### Blockers
```tasks
is blocking
```

### All Tasks
```tasks
not done
```

## General Notes

- **Task1**: For Stack name: Enter VPCStack
- **Task2**: For DB subnet group: Name: Enter AuroraSubnetGroup, For database: DB cluster identifier: Enter MyDBCluster, For Master username: Enter admin. Database options: Initial database name: Enter WPDatabase
- **Task3**: For file system: Name - optional: Enter myWPEFS, For Tag key: Enter Name, Tag value – optional: Enter myWPEFS
- **Task4**: For Target group name: Enter myWPTargetGroup, For Load balancer name: Enter myWPAppALB.
- **Task5**: For Stack name, WPLaunchConfigStack, For WordPress admin username: wpadmin
- **Task6**: For Auto Scaling group name: Enter WP-ASG, For Tags: Key: Enter Name, Value - optional: Enter WP-App  
writer endpoint: mydbcluster.cluster-chkyufnkoby0.us-west-2.rds.amazonaws.com
fs id [fs-09cd89c71373f5699](https://us-west-2.console.aws.amazon.com/efs/home?region=us-west-2#/file-systems/fs-09cd89c71373f5699)


myWPAppALB-2063265306.us-west-2.elb.amazonaws.com/wp-login.php