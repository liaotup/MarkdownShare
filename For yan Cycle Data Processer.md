* 处理代码
    ```JavaScript
    // 原始数据
    let originDataList = [{
            cycle: 1,
            month: '201701',
            value: -0.0001
        },
        {
            cycle: 2,
            month: '201702',
            value: -0.0001
        },
        {
            cycle: 1,
            month: '201703',
            value: -0.0001
        },
        {
            cycle: 3,
            month: '201703',
            value: -0.0001
        }
    ]

    // 推入数组
    function objectPusher(array, data, matchKey) {
        // 融合 
        function objectMerge(originObject, newObject) {
            let rs = null
            if (originObject)
                rs = Object.assign(originObject, newObject)
            else
                rs = newObject
            return rs
        }
        // 对象构造
        function reConstruct(originData) {
            let destData = new Object()
            destData['month'] = originData.month
            destData[originData.cycle + '月'] = originData.value
            return destData
        }
        //推入数组 （判断是否存在，不存在就直接推入，存在就融合）
        let index = month2ArrayIndexMap[matchKey]
        data = reConstruct(data)
        if (index) {
            let destObject = objectMerge(result[index], data)
            array[index] = destObject
        } else
            month2ArrayIndexMap[matchKey] = array.push(data) - 1
    }


    let month2ArrayIndexMap = new Object()
    let result = new Array()
    originDataList.forEach(item => {
        objectPusher(result, item, item.month)
    })
    console.log(result)
    ```

* 输出结果

```JavaScript
[{
        month: '201701',
        '1月': -0.0001
    },
    {
        month: '201702',
        '2月': -0.0001
    },
    {
        month: '201703',
        '1月': -0.0001,
        '3月': -0.0001
    }
]
```
