#使用说明

1. 调用局域网发现的方法，获得局域网设备

```objc
/** 
 * 局域网发现设备
 * @param timeout  超时时间
 * @param callback 返回的设备列表
 */
+ (void)findDeviceTimeout:(NSInteger )timeout
                 callback:(void(^)(NSArray * localDeviceList))callback;
 
```  
         

2. 获取指定设备（获取那些设备的，放到数组作为参数传入）的wifi信号强度接口

```objc

/**
 * 获取局域网设备与WiFi连接质量
 * @param devices 需要查询设备连接WiFi强度的设备列表
 * @param timeout 超时时间
 * @param callback 回调查询结果,通过ACLocalDevice的linkQuality属性获取
 */
+ (void)fetchConnectedWifiRssiWithLocalDevice:(NSArray <ACLocalDevice *>*)devices
                                      timeout:(NSTimeInterval)timeout
                                     callback:(void (^)(NSArray <ACLocalDevice *> *devices,
                                                        NSError *error))callback;

/**
 * 停止获取设备与WiFi连接的信号强度
 */
+ (void)stopFetchWifiRssi;

```

