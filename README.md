## 中译英

地址：http://live.langziphp.com/v1/translator

方式：GET

返回类型：json

| 参数     | 类型   | 描述     | 是否必填 |
| -------- | ------ | -------- | -------- |
| sentence | string | 中文句子 | 是       |

使用案例：翻译“好好学习”

http://live.langziphp.com/v1/translator?sentence=好好学习

返回的数据：

```json
{
    "from":"zh",
    "to":"en",
    "trans_result":[
        {
            "src":"好好学习",
            "dst":"Study hard"
        }
    ]
}
```



## 历史上的今天

地址：http://live.langziphp.com/v1/history

方式：GET

返回类型：json

| 参数  | 类型   | 描述    | 是否必填 |
| ----- | ------ | ------- | -------- |
| day   | int    | 日期/号 | 是       |
| month | string | 月份    | 是       |

使用案例：查9月4号的历史事件

http://live.langziphp.com/v1/history?month=9&day=4

返回的数据：

```json
{
    "result":[
        {
            "_id":"17630904",
            "title":"法国作家夏多勃里昂出生",
            "pic":"",
            "year":1763,
            "month":9,
            "day":4,
            "des":"在256年前的今天，1763年9月4日 (农历七月廿七)，法国作家夏多勃里昂出生。",
            "lunar":"癸未年七月廿七"
        },
        {
            "_id":"17810904",
            "title":"洛杉矶建城",
            "pic":"http://juheimg.oss-cn-hangzhou.aliyuncs.com/toh/201109/4/1D10616727.jpg",
            "year":1781,
            "month":9,
            "day":4,
            "des":"在238年前的今天，1781年9月4日 (农历七月十七)，洛杉矶建城。",
            "lunar":"辛丑年七月十七"
        }
    ],
    "reason":"请求成功！",
    "error_code":0
}
```



## 手机归属地查询

地址：http://live.langziphp.com/v1/phone

方式：GET

返回类型：json

| 参数  | 类型   | 描述   | 是否必填 |
| ----- | ------ | ------ | -------- |
| phone | string | 手机号 | 是       |

使用案例：查13526735467的归属地

http://live.langziphp.com/v1/phone?phone=13526735467

返回的数据：

```json
{
    "resultcode":"200",
    "reason":"Return Successd!",
    "result":{
        "province":"河南",
        "city":"郑州",
        "areacode":"0371",
        "zip":"450000",
        "company":"移动",
        "card":""
    },
    "error_code":0
}
```



## 成语字典

地址：http://live.langziphp.com/v1/idiom

方式：GET

返回类型：json

| 参数 | 类型   | 描述 | 是否必填 |
| ---- | ------ | ---- | -------- |
| word | string | 成语 | 是       |

使用案例：查一览无余的成语解释

http://live.langziphp.com/v1/idiom?word=一览无余

返回的数据：

```json
{
    "reason":"success",
    "result":{
        "bushou":"一",
        "head":"一",
        "pinyin":"yī lǎi wú yú",
        "chengyujs":" 览：看；余：剩余。一眼看去，所有的景物全看见了。形容建筑物的结构没有曲折变化，或诗文内容平淡，没有回味。",
        "from_":" 南朝宋·刘义庆《世说新语·言语》：“江左地促，不如中国，若使阡陌条畅，则一览而尽，故纡余委曲，若不可测。”",
        "example":" 水中岸上都光光的；亏得湖里有五个洲子点缀着，不然便～了。 朱自清《南京》",
        "yufa":" 紧缩式；作谓语、状语；形容视野开阔",
        "ciyujs":null,
        "yinzhengjs":"南朝 宋 刘义庆 《世说新语·言语》：“ 江左 地促，不如中国，若使阡陌条畅，则一览而尽，故紆餘委曲，若不可测。”后以“一览无餘”谓一眼即可全见。《金瓶梅词话》第六一回：“风虚寒热之症候，一览无餘。” 朱自清 《南京》：“水中岸上都光光的，亏得湖里有五个洲子点缀着，不然便一览无余了。” 刘富道 《南湖月》：“ 黎露 站在厂门口，全厂一览无余。”",
        "tongyi":[
            "一目了然",
            "尽收眼底"
        ],
        "fanyi":[
            "管中窥豹",
            "一鳞半爪"
        ]
    },
    "error_code":0
}
```



## 新华字典

地址：http://live.langziphp.com/v1/xinhua

方式：GET

返回类型：json

| 参数 | 类型   | 描述 | 是否必填 |
| ---- | ------ | ---- | -------- |
| word | string | 字   | 是       |

使用案例：查学的解释

http://live.langziphp.com/v1/xinhua?word=学

返回数据类型：

```json
{
    "reason":"返回成功",
    "result":{
        "id":"319d6a87e8c8a42d",
        "zi":"学",
        "py":"xue",
        "wubi":"ipbf",
        "pinyin":"xué",
        "bushou":"子",
        "bihua":"8",
        "jijie":Array[12],
        "xiangjie":Array[246]
    },
    "error_code":0
}
```



## 天气查询

地址：http://live.langziphp.com/v1/weather

方式：GET

返回类型：json

| 参数 | 类型   | 描述 | 是否必填 |
| ---- | ------ | ---- | -------- |
| city | string | 城市 | 是       |

使用案例：查广州的天气

http://live.langziphp.com/v1/weather?city=广州

返回的数据：

```json
{
    "reason":"查询成功!",
    "result":{
        "data":{
            "realtime":Object{...},
            "life":Object{...},
            "weather":Array[5],
            "f3h":Object{...},
            "pm25":Object{...},
            "jingqu":"",
            "jingqutq":"",
            "date":"",
            "isForeign":"0",
            "partner":Object{...}
        }
    },
    "error_code":0
}
```



## 空气质量

地址：http://live.langziphp.com/v1/air

方式：GET

返回类型：json

| 参数 | 类型   | 描述 | 是否必填 |
| ---- | ------ | ---- | -------- |
| city | string | 城市 | 是       |

使用案例：查广州的空气质量

http://live.langziphp.com/v1/air?city=广州

返回的数据：

```json
{
    "resultcode":"200",
    "reason":"SUCCESSED!",
    "error_code":0,
    "result":[
        {
            "citynow":{
                "city":"广州",
                "AQI":"27",
                "quality":"优",
                "date":"2019-06-04 21:00"
            },
            "lastTwoWeeks":Object{...},
            "lastMoniData":Object{...}
        }
    ]
}
```



## 电影查询

地址：http://live.langziphp.com/v1/movie

方式：GET

返回类型：json

| 参数   | 类型   | 描述     | 是否必填 |
| ------ | ------ | -------- | -------- |
| ctitle | string | 电影名称 | 是       |

使用案例：查询复仇者联盟的电影信息

http://live.langziphp.com/v1/movie?title=复仇者联盟

```json
{
    "resultcode":"200",
    "reason":"成功的返回",
    "result":[
        {
            "movieid":"83336",
            "rating":"8.2",
            "genres":"动作/科幻/冒险",
            "runtime":"143 分钟",
            "language":"英语",
            "title":"复仇者联盟",
            "poster":"http://img21.mtime.cn/mt/2012/04/19/141408.39603781_270X405X4.jpg",
            "writers":"乔斯·韦登,扎克·佩恩",
            "film_locations":"美国",
            "directors":"乔斯·韦登",
            "rating_count":"25699",
            "actors":"小罗伯特·唐尼 Robert Downey Jr.,克里斯·埃文斯 Chris Evans,克里斯·海姆斯沃斯 Chris Hemsworth,斯嘉丽·约翰逊 Scarlett Johansson",
            "plot_simple":"美国队长在被冰封数年后，终于苏醒过来。这个世界已经不再是他过去所熟悉的样子，各类型的邪恶对手层出不穷。于是美国队长、钢铁侠、雷神、绿巨人等超级英雄聚集在一起，组成史上最强大的“复仇者”团队，共同惩恶扬善，为和平而战。",
            "year":"2012",
            "country":"美国",
            "type":null,
            "release_date":"20120505",
            "also_known_as":"复仇者"
        }
    ],
    "error_code":0
}
```



## 星座

地址：http://live.langziphp.com/v1/constellation

方式：GET

返回类型：json

| 参数          | 类型   | 描述                                         | 是否必填 |
| ------------- | ------ | -------------------------------------------- | -------- |
| constellation | string | 星座名称                                     | 是       |
| date          | string | 日期，值为today、tomorrow、week，month、year |          |

使用案例：查询查处女座一周内的运势

http://live.langziphp.com/v1/constellation?constellation=处女座&date=week

返回的数据：

```json
{
    "name":"处女座",
    "weekth":23,
    "date":"2019年06月02日-2019年06月08日",
    "health":"",
    "job":null,
    "love":"恋爱：本周的你虽然看起来目标明确，但其实也是存在有犹豫的，这份犹豫可能得保持一周。 ",
    "money":"财运：本周的你会为了身边的人破财，不过还好，应该问题不是很大。 ",
    "work":"工作：本周的你工作状态比较模糊，可能要面临临时出差的问题，相信你调整好状态会表现的不错。 ",
    "resultcode":"200",
    "error_code":0
}
```



## 二维码

地址：http://live.langziphp.com/v1/qr

方式：GET

返回类型：json

| 参数    | 类型   | 描述       | 是否必填 |
| ------- | ------ | ---------- | -------- |
| content | string | 二维码内容 | 是       |

使用案例：生成内容为“为人民服务”的二维码

http://live.langziphp.com/v1/qr?content=为人民服务







