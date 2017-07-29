# BVN Label API Document
## 新接口 （Swagger：<a href="http://bowkerbvnlabelportal.azurewebsites.net/wmsdemo/Swagger">/wmsdemo/Swagger</a>）
* /wmsdemo/FontAction/getPrinterList.action
    * 用于获取打印机配置信息
    * 使用 Get 方法获取
    * 示例反馈数据
        ```JSON
        {
        "code": 1,
        "message": "成功 ",
        "data": [
            {
            "id": 1,
            "name": "PrinterA",
            "address": "192.168.0.1",
            "port": 8080,
            "url": "/printit"
            }
        ]
        }
        ```
* /wmsdemo/FontAction/stockAction.action
    * 库存操作接口
    * 传参模形如下
        ```JSON
        {
            "moveInIdList": [
                3,
                4
            ],
            "moveOutIdList": [
                1,
                2
            ]
        }
        ```
    * 操作类型有两种
        * MOVE_IN
        * MOVE_OUT
