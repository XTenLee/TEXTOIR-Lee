# The working directory of TEXTOIR

```
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
```

# Data Format 

## Model Test
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

![image](https://user-images.githubusercontent.com/37832030/109410824-b3b7dc00-79d8-11eb-94a1-e82f6656de8f.png)

**Naming Scheme of json**：Detection_ Influence.json

**Naming Scheme of Key Words**：KIR_DatasetName_KIR_Metric
  
**Example**
```
 {"KIR_banking_0.1_F1":{
    "MSP":[72, 72, 71, 73, 70, 73, 72,73,74,74],
    "DOC":[82, 82, 81, 84, 89, 90, 93,92,93,93],
    "OpenMax":[75, 82, 81, 87, 83, 83, 84,84,85,83],
    "DeepUnk":[80,73, 81, 83, 89, 87, 90,89,91,92],
    "ADB":[82, 93, 91, 93, 90, 91, 90,91,94,95]
},
      "LR_banking_0.3_F1":{
    "MSP":[72, 72, 71, 73, 70, 73, 72,73,74,74],
    "DOC":[82, 82, 81, 84, 89, 90, 93,92,93,93],
    "OpenMax":[75, 82, 81, 87, 83, 83, 84,84,85,83],
    "DeepUnk":[80,73, 81, 83, 89, 87, 90,89,91,92],
    "ADB":[82, 93, 91, 93, 90, 91, 90,91,94,95]
}
}

```
![image](https://user-images.githubusercontent.com/37832030/109410871-14471900-79d9-11eb-8e64-ba36a26179f7.png)

**Naming Scheme of json**：Detection_Model_Analysis.json

**Naming Scheme of Key Words**：ADB_Example
  
**Example**
```
 "ADB_Example2_circle_r": //决策边界方法中边界圆的半径设置
{
    "r1": 30,
    "r2": 40,
    "r3": 50,
    "r4": 60
 },
    "ADB_Example2_circle_xy"://决策边界方法中边界圆心设置
{
    "Boundary#1": [[1.5,5.7,30]],
    "Boundary#2": [[2.5,1.5,40]],
    "Boundary#3": [[4.1,4.1,50]],
    "Boundary#4": [[6,6.5,60]]
 },
    "ADB_Example2_cluster":{//样例的2维坐标点
    "Cluster#1" : [
        [1.275154, 5.957587,30],
        [1.441611, 5.444826,30],
        [1.17768, 5.387793,30],
        [1.855808, 5.483301,30],
        [1.650821, 5.407572,30],  
        [1.513623, 5.841029,30]
    ],
    "Cluster#2":[
        [2.606999, 1.510312,10],
        [2.121904, 1.173988,10],
        [2.376754, 1.863579,10],
        [2.797787, 1.518662,10],
        [2.327224, 1.358778,10]
    ],
    "Cluster#3":[
        [3.919901, 4.439368,10],
        [3.598143, 5.07597,10],
        [3.914654, 4.559303,10],
        [4.148946, 3.345138,10],
        [4.629062, 3.535831,10]
    ],
    "Cluster#4":[
        [5.919901, 6.439368,5],
        [5.598143, 6.97597,5],
        [5.914654, 6.559303,5],
        [6.148946, 6.345138,5],
        [5.629062, 6.535831,5]
    ]
}

```

![image](https://user-images.githubusercontent.com/37832030/109410862-0abdb100-79d9-11eb-88ec-f5e5bf7942bd.png)

**Naming Scheme of json**：Detection_Model_Analysis.json

**Naming Scheme of Key Words**：MethodName_Example
  
**Example**

```
"DeepUnk_Example2_bar":  {//每个意图类别中，每个样例属于此类的概率，下表中展示了6个样例。中括号中第几个数据代表第几个样例属于此类别的概率。
    "Play Music":[0.1, 0.12, 0.17, 0.1, 0.1, 0.03], 
    "Book Resturant":[0.1, 0.11, 0.1, 0.16, 0.16, 0.75],
    "Book Ticket":[0.15, 0.7, 0.12, 0.21, 0.1, 0.1],
    "RateBook":[0.1,  0.01, 0.1, 0.7, 0.1, 0.15],
    "GetWeather":[0.8, 0.12, 0.21, 0.16, 0.21, 0.21],
    "AddToPlaylist":[0.1,  0.21, 0.7, 0.1, 0.1, 0.14],
    "UnKnown Intent":[0.1,  0.01, 0.12, 0.1, 0.9, 0.01]  
},
  "DeepUnk_Example2threshold":   {//每个类别的概率阈值，有几个样例需要重复设置几次。
    "Threshold-Play Music":[0.55, 0.55,0.55,0.55,0.55,0.55],
    "Threshold-Book Resturant":[0.43, 0.43,0.43,0.43,0.43,0.43],
    "Threshold-Book Ticket":[0.5, 0.5,0.5,0.5,0.5,0.5],
    "Threshold-RateBook":[0.6, 0.6,0.6,0.6,0.6,0.6],
    "Threshold-AddToPlaylist":[0.4, 0.4,0.4,0.4,0.4,0.4],
    "Threshold-GetWeather":[0.5, 0.5,0.5,0.5,0.5,0.5],
    "Threshold-UnKnown Intent":[0.47, 0.47,0.47,0.47,0.47,0.47]
}

```
