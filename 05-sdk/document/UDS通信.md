# UDS通信 

Matrix-SDK中通过`ACServiceManager`这个类完成对UDS的请求；

#### 1. API

```objc
/**
 发送请求到UDS服务

 @param infoDictionary 请求内容（字典类型）
 @param methodName 方法名
 @param serviceName UDS服务名称（控制台可查询）
 @param serviceVersion UDS的版本号（控制台可查询）
 @param callback UDS回调信息
 */
+ (void)sendInfoToServiceWithInfoDictionary:(NSDictionary *)infoDictionary
                                 methodName:(NSString *)methodName
                                serviceName:(NSString *)serviceName
                             serviceVersion:(NSInteger)serviceVersion
                                   callback:(void(^)(NSDictionary *response, NSError *error))callback;
```

UDS有的接口，开发者均可在通过该接口发送请求。
参数：

- infoDictionary：请求参数
- methodName：UDS方法名称
- serviceName：UDS服务名
- serviceVersion：UDS服务版本
- callback：请求回调
