# iotgateway
* 物联网网关mqtt输出，支持thingsboard
* 抛砖引玉，共同进步
* 可视化的配置方式实现数据采集(使用wtm开发)
* 基于.net5的开源物联网网关
* 内置ModbusTcp驱动(使用nmodbus4)
* 支持驱动二次开发（短期内会提供西门子三菱通讯）
* 数据通过mqtt推送，支持thingsboard
* 目前只支持遥测数据上传，后续支持属性的双向通信
# 运行
## windows运行：
1. [下载Releasev0.01](https://github.com/iioter/iotgateway/releases/download/v0.01/iotgateway-winx64-v0.01.zip)发布版本
2. [下载.net5](https://dotnet.microsoft.com/en-us/download/dotnet/5.0) sdk或runtime
3. 安装.net5 
4. 解压release包，运行IoTGateway.exe
5. 访问[iotgateway](http://localhost:518/)后台：http://localhost:518
## docker运行
1. docker push 15261671110/iotgateway
2. docker run -d -p 518:518 --name iotgateway --restart always 15261671110/iotgateway
## 登入系统
1. 用户名 admin,密码 000000
2. 打开发布文件路径下的ReadMe文件夹中的手摸手，按照顺序添加设备进行采集
# 采集配置
![1 登录](https://user-images.githubusercontent.com/29589505/145705166-d5818557-4ba1-4e7b-b8d8-8f5f4b28868f.png)
![2 首页](https://user-images.githubusercontent.com/29589505/145705168-94b3ff0c-2f5c-4a31-8e83-c2ed799320ce.png)
![3 网关配置](https://user-images.githubusercontent.com/29589505/145705172-2a10d11b-436d-4a2c-86bf-cf6aa5dade07.png)
![4 设备维护](https://user-images.githubusercontent.com/29589505/145705173-7c9ccc0e-e1ab-49ba-af28-0e5c654a57e3.png)
![5 设备参数配置](https://user-images.githubusercontent.com/29589505/145705174-95a14642-dd30-4e73-803d-5f998f297842.png)
![6 设备变量配置](https://user-images.githubusercontent.com/29589505/145705175-fb11013f-55f8-4123-b770-aaf41706a7aa.png)
![7 设备变量配置-新建](https://user-images.githubusercontent.com/29589505/145705178-52c7580f-1793-4c9a-935b-658d21946aa1.png)
# thingsboard接入教程
![0 准备一个modsim 或者modbus tcp设备](https://user-images.githubusercontent.com/29589505/145705255-18e8d649-6a08-4dc7-96b3-6bdf8fc23cb4.png)
![1 thingsboard  新建网关](https://user-images.githubusercontent.com/29589505/145705256-1e01030f-2ccb-464e-a3cc-784d5a7c1c91.png)
![2 gateway 修改网关传输配置](https://user-images.githubusercontent.com/29589505/145705260-3f9f36c9-c163-4853-9787-677926989af3.png)
![3 gateway 创建组](https://user-images.githubusercontent.com/29589505/145705261-c605c825-d463-491d-ad32-1a3c245e2ee3.png)
![4 gateway 创建设备](https://user-images.githubusercontent.com/29589505/145705263-d3ea2a6b-7ea3-491a-bcd1-20e8dc770922.png)
![5 gateway 配置设备参数](https://user-images.githubusercontent.com/29589505/145705264-6db386ba-e68e-4a7f-acff-44f55ce25e73.png)
![6 gateway 新建变量](https://user-images.githubusercontent.com/29589505/145705265-44a0da5d-6d16-4463-a755-626d93dc121c.png)
![6 gateway 修改设备为自启动](https://user-images.githubusercontent.com/29589505/145705269-c816789c-cd67-4c01-973f-ae4f10eb41d9.png)
![7 thingsboard 查看到设备和数据](https://user-images.githubusercontent.com/29589505/145705270-31d8884f-7f6f-4ff5-a6bb-1d57a97012f4.png)
![8 gateway 查看到数据](https://user-images.githubusercontent.com/29589505/145705271-cb80b80e-006e-4312-8843-6d0ae9457cb1.png)
