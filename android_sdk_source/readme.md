# 目录说明  

  * -apidoc      是javadoc的文档，从index.html进入主页  
  * -demo        是示例的代码工程  
  * -jar_core    是使用此工程需要主要的引用包,此文件下会放置迭代的各个版本的jar包  
  * -jar_base    是使用此工程需要的基础包    
  * -sdkdoc      包含了此工程一些必要的说明  
# 示例APK  

## [vpsdk_1.2.1.apk](https://github.com/HBandSDK/Android_Ble_SDK/blob/master/android_sdk_source/Demo/vpsdk_1.2.1.apk)  

# 更新日志
## [vpprotocol_2.1.1.15.jar](https://github.com/HBandSDK/Android_Ble_SDK/blob/master/android_sdk_source/jar_core/vpprotocol_2.1.1.15.jar) 

vpprotocol_2.0.4.3.jar
>*添加了呼吸率检测功能

vpprotocol_2.0.2.3.jar
>*修改了读取血氧的bug

vpprotocol_2.0.1.3.jar
>*添加代码混淆

## 注意：由1.x.x.x升级到2.x.x.x，需要修改以下内容


因SDK前期设计的不合理，为了保证内部的枚举类不被混淆，且保持类名的统一，
此次更新将在com.veepoo.protocol.operate包下的所有的内部枚举类全部转移到com.veepoo.protocol.model.enums包下。
如果您使用到以下枚举，那么您将需要修改类名且重新导包


| 涉及的功能| 修改前<br>com.veepoo.protocol.operate.*| 修改后<br>com.veepoo.protocol.model.enums.* |
| :------| :------:  | :------: |
| 01.闹钟 | AlarmOperater.AOStatus | EAalarmStatus |
| 02.血压模式 | BPModelOprate.BPStatus | EBPStatus |
| 03.血压检测 | BPOperater.BPDetectStatus| EBPDetectStatus |
| 04.拍照 | CameraOperater.COStatus | ECameraStatus |
| 05.倒计时 | CountDownOprate.DCStatus | ECustomStatus |
| 06.疲劳度 | FatigueOperate.FatigueStatus | EFatigueStatus |
| 07.查找设备 | FindDeviceOperater.FDStatus | EFindDeviceStatus |
| 08.心率 | HeartOperater.HeartStatus| EHeartStatus |
| 09.心率异常 | HeartWarningOperate.HWStatus | EHeartWaringStatus |
| 10.久坐 | LongSeatOperater.LSStatus| ELongSeatStatus |
| 11.夜间转腕 | NightTurnWristOperate.NTStatus | ENightTurnWristeStatus |
| 12.血氧检测 | Spo2hDetectOperate.SPO2HStatus | ESPO2HStatus |
| 13.女性 | WomenOperater.OperateStatus  | EWomenOprateStatus |

vpprotocol_1.2.7.1.jar
>*更新了多国语言设置功能  


vpprotocol_1.2.6.0.jar
>*修改了读取运动模式仅读取一次的bug  
>*修改了部分Api的doc描述  
