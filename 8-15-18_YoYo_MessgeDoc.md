## 1、修改语言接口
- **接口说明**
    > 
        通过该消息接口切换服务语言  广电运通 -> YoYo
- **请求方式**
    >
        传输方式：Windows消息
        消息结构：JSON
        接收者HWND名称：人工智能客服系统

- **请求参数**
    >
    | 请求参数      |     参数类型 |   参数说明   |
    | :-------- | :--------| :------ |
    | intent|  string，必填|  本接口固定为 **change_lang**|
    | dest_lang|   string，必填|  可选为 **en_us \| zh_cn**|

- **消息示例**
    >
    ```json
    {
        "intent":"change_lang",
        "dest_lang":"zh_cn"
    }
    ```

## 2、业务回调接口(补票、无票、打发票、返回)
- **接口说明**
    > 
        通过该消息接口调起票务业务操作界面  YoYo -> 广电运通

- **请求方式**
    >
        传输方式：Windows消息
        消息结构：JSON
        接收者HWND名称：VoiceInteraction

- **意图表**
    >
    |意图名|意图|
    | :-------- | :--------|
    |tickey_repair|补票|
    |invoice_transaction|打发票|
    |page_back|返回|
    |pay_for_card|充值|
    |without_tickey|无票|
- **请求参数**
    >
    | 请求参数      |     参数类型 |   参数说明   |
    | :-------- | :--------| :------ |
    | intent|  string，必填|  可选为 **tickey_repair \| invoice_transaction \| page_back \| pay_for_card \| without_tickey**|

- **消息结构**
    >
    ```json
    {
        "intent":"page_back"
    }
    ```
