# The working directory of TEXTOIR

.

├── thedataset 			//Dataset Management

├── detection			//Open Intent Detection

├── discovery			//Open Intent Discovery

├── annotation			//Data Annotaion

├── static				//Static Resource

│   ├── test_data		//Test Data

│   ├── img			//image

│   ├── lib				//Front Style

│   ├── log				//Run Logd

│   └── models			//Intention Recognition Models

│       ├── result		//json

│       ├── data			//Datasets

│       ├── open_intent_detection	//Intent Detection Models

│       ├── open_intent_discovery	//Intent Discovery Models

│       ├── run_detect.py			//Entry of Run Intent Detection

│       └── run_discover.py		//Entry of Run Intent Discovery

├── textoir				//Setting

└── templates			//Front Page

# Data Format 

### Model Test
![image](https://user-images.githubusercontent.com/37832030/109410374-21fa9f80-79d5-11eb-8c93-6ce543f56059.png)

**Naming Scheme of json**：Detection_Overall_Performance_Error_Analyze.json

  **Naming Scheme of Key Words**：DatasetNmae_Klr_LR_ModelName_ overall_performance
  
  **Example**
  
  ```
  {"snips_1.0_1.0_overall_performance":{
    
        "intent_class": ["AddToPlayList", "GetWeather", "ReatBook", "Book Ticket", "Book Resutrant", "Play Music"],
        
        "left":[-120, -132, -101, -134, -190, -230],
        
        "right":[320, 302, 341, 374, 390, 450]
        
    },
    
    " snips_1.0_1.0_error_analysis":{
    
    "AddToPlayList":[0, -21, -12, -14, -10, -10],
    
    "GetWeather":[-8, 0, -12, -14, -10, -10],
    
    "ReatBook":[-15, -21, 0, -14, -19, -30],
    
    "Book Ticket":[-20, -12, -11, 0, -20, -30],
    
    "Book Resurant":[-20, -12, -11, -14,0, -30],
    
    "Play Music":[-32, -30, -30, -33, -39, 0]
    }}
    
 ```
 
 ```
.
├── thedataset 			//数据集管理模
├── detection			//意图检测模块
├── discovery			//意图发现模块
├── annotation			//数据标注模块
├── static				//静态资源
│   ├── test_data		//测试数据存放位置
│   ├── img			//图片
│   ├── lib				//前端样式
│   ├── log				//运行记录
│   └── models			//模型存放路径
│       ├── result		//json文件存放目录
│       ├── data			//存放数据集
│       ├── open_intent_detection	//意图检测算法
│       ├── open_intent_discovery	//意图发现算法
│       ├── run_detect.py			//意图检测运行文件
│       └── run_discover.py		//意图发线运行文件
├── textoir				//项目setting目录
└── templates			//前端页面

 ```
   sad
   
   
  
  
