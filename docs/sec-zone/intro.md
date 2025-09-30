## What is a Security Zone ?

A security zone consists of set of resources from one or more services. Here are a few examples of security zones:

#### Zone: `finance`
```yaml
 service: prod_hadoop; path=/finance/*, /taxes/*  
 service: prod_hive; database=finance  
 service: prod_kafka; topic=FIN_*  
 service: test_hadoop; path=/finance/*, /taxes/*  
```
#### Zone: `sales`
```yaml
 service: prod_hadoop; path=/sales/*  
 service: prod_hive; database=sales  
 service: prod_kafka; topic=SALES_*  
```

As can be seen above, the resources can be specified using wildcards - like `FIN_*`, `SALES_*`.

It is critical that a resource be not mappable to more than one zone. Ranger would not allow creation of zones that specify resources that match for resources of another zone. For example, attempt to update finance zone
above with HDFS path `/sales/finance/*` will not be permitted, as this
conflicts with HDFS path specified in sales zone - `/sales/*`.

## Administration 

A set of users and groups can be designated as administrators of a security
zone. These users can create/update/delete security policies for the
resources in the zone.  


## Audits
A set of users and groups can be authorized to view audit logs of access to
zone’s resources. Other users will not be allowed to view access-audit logs of
resources of the zone.  
