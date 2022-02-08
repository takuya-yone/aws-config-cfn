# aws-config-cfn

## For Organizations Integration

### enable org integration
```Bash
aws organizations enable-aws-service-access --service-principal config.amazonaws.com
aws organizations enable-aws-service-access --service-principal config-multiaccountsetup.amazonaws.com
```
### delegate administrator to account
```Bash
aws organizations register-delegated-administrator --account-id [Account Id] --service-principal config.amazonaws.com
aws organizations register-delegated-administrator --account-id [Account Id]  --service-principal config-multiaccountsetup.amazonaws.com
```

### check delegated account
```Bash
aws organizations list-delegated-services-for-account --account-id [Account Id] --output text
```

### creagte aggregator on [Account Id] 

### 

# Ref
- https://docs.aws.amazon.com/ja_jp/config/latest/developerguide/aggregate-data.html
- https://fu3ak1.hatenablog.com/entry/2021/01/05/110810
- https://dev.classmethod.jp/articles/config-aggregator-in-organization-member-account/
- https://dev.classmethod.jp/articles/deploy-config-rules-in-organization-member-account/
- https://dev.classmethod.jp/articles/config-aggregator-in-organization-member-account/