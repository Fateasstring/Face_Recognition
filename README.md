# Face_Recognition
人脸坐标识别模块。

### 1.业务场景：

​		公司某产品系统调用第三方接口进行人脸比对以确认客户真实身份。第三方要求上传用户身份证照片，用户手持身份证半身照进行比对。从出现的错误来看，当用户手持身份证半身照像素足够好，足够清晰时，第三方提供的接口会在一张图片中识别到两个人像，进而报错，也即是，一张照片只能检测出一个人像。

​		与第三方交流这个问题，对方坐地起价，宣称解决这个问题需要加5万元的修改费。

### 2.解决方法：

​		经过研究，发现可将用户手持身份证半身照进行切割，即开发一个模块，识别出用户人脸在图片中的位置坐标，身份证人脸在图片中的位置坐标，并加以标识区分，将数据坐标返回给前端进行切割，再用切割得来的照片按照新的比对逻辑，调用以前的业务接口进行比对，问题得以解决。