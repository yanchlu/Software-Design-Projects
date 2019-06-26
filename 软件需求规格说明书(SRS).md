
# 软件需求规格说明书(SRS)


### 项目背景  
移动互联网发展迅速，越来越多的人乐于接受移动互联网给我们带来的便利，但是很多餐饮行业仍然采用传统人工点餐方法，既麻烦，又费时。通过调研，我们了解到许多参与者表明“自身有扫码点餐的意向，但是商家没有提供”，使得**扫码点餐**无法被人们广泛应用，因此我们希望可以解决这个困境的部分。

### 业务分析 
1 涉众人员分析（人）

点餐客户：希望能够快速自助点单，无需等待服务员。希望可以清楚地查看本店具体的菜品、及其库存和价格。希望能够清晰地看到本店的优惠信息。希望可以灵活的修改订单，添加菜品。希望可以通过点餐系统完成账单支付。

餐厅：希望能够便捷地指引未接触的客户进行扫码点餐。希望能够便捷的修改餐厅信息和菜单。希望能够快速准确的获取订单。

2 业务流程分析（事）

客户：

**1.** 点餐客户通过扫码成功进入主菜单，开始点餐。

**2.** 点餐客户通过上下拉浏览菜单，查看菜品。

**3.** 点餐客户选择各自想要的菜式，加入购物车。

点餐客户重复2-3步，直到选择完毕。

**4.** 点餐客户下单进入订单详情。

**5.** 点餐客户确定提交订单

**6.** 点餐客户可以查看订单详情，餐厅接收订单消息，开始准备菜品

### 限制条件（规）
1 运行环境约束

Android 7.0版本以上

2 质量要求

用户能简便，流畅点餐
餐厅能实时正确接收订单消息

### 产品分析

**功能性需求：**

两个系统： 用户点餐系统、商家管理系统


 ### 1 用例图
 
![case.png](https://github.com/ssad2019/pages/blob/master/doc/use_case/%E7%94%A8%E4%BE%8B%E5%9B%BE.png)

### 2 用例描述

### 扫码点餐用例

#### 1. Use case：扫描二维码

   Actors：客户
   
   Description：顾客打开程序，扫描二维码，进入小程序界面。

   主成功场景：扫描二维码进入主菜单界面
   
   交替场景：
   
   如果扫码失败，跳转到扫码界面并弹出提示，用户重新扫码

   如果重新扫码失败，需要呼叫服务员，人工点餐

   如果扫码后程序闪退或出现其他异常，呼叫服务员进行人工点餐，餐厅负责人联络点餐系统负责人；
   
#### 2. Use case：查看商店详情

   Actors：客户
   
   Description：顾客查看商店详情，包括商家图片，名称和简介。
   
   主成功场景：顾客进入商店详情界面查看商店详情
   
#### 3. Use case：菜单列表

   Actors：客户
   
   Description：顾客查看菜单列表，可以添加菜品或者从购物车中删除菜品，可以点击查看菜品详情，包括菜品名称，图片，价格和简介。
   
   主成功场景：顾客滑动查看菜单列表，点击菜品查看菜品详情，自由选择添加菜品或从购物车中删除菜品
   
   交替场景：
   
   如果点餐出现异常（图片无法加载，无法添加菜品等），呼叫服务员进行人工点餐，餐厅负责人联络点餐系统负责人；
   
#### 4. Use case：确认订单

   Actors：客户
   
   Description：顾客确认自己的订单，查看订单中所有菜品，添加订单备注，订单支付方式固定为线下支付。
   
   主成功场景：顾客进入确认订单界面查看订单
   
#### 5. Use case：提交订单

   Actors：客户
   
   Description：客户确认订单后提交订单，查看订单列表，订单时间和订单号。
   
   主成功场景：顾客提交订单，跳转到提交订单界面，查看订单信息
   
   交替场景：
   
   跳转失败，无法提交或者看不到订单时间与订单号，呼叫服务员查看商家管理系统订单界面，核实是否成功提交订单。
   
#### 6. Use case：用户操作

   Actors：商家
   
   Description：商家打开网页端管理系统，进行注册/登入/登出，之后可以修改商家信息，包括图片，名称和详情介绍。
   
   主成功场景：商家按照注册/登录流程进行注册/登录，登入后可选择登出更换账号
   
   交替场景：
   
   xxx
   
#### 7. Use case：生成二维码

   Actors：商家
   
   Description：商家生成与座位号绑定的二维码，用于客户扫码。
   
   主成功场景：商家输入座位号，生成与座位号绑定的二维码，之后自行下载打印
   
   交替场景：
   
   xxx
   
#### 8. Use case：订单查看

   Actors：商家
   
   Description：商家实时查看订单，当订单完成时，修改订单状态为已完成。
   
   主成功场景：顾客提交订单，商家实时查看订单界面刷新，可以看到新提交的订单以及订单详情（座位号，订单列表，备注）
   
   交替场景：
   
   xxx
   

**功能点：**


- 点餐
 
  ![order](https://raw.githubusercontent.com/E-Order/Dashboard/master/document/Requirement_Specification/系统顺序图/order_ssd.png)
        
- 管理购物车
![管理购物车15331209](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/15331209_%E7%AE%A1%E7%90%86%E8%B4%AD%E7%89%A9%E8%BD%A6.png)

- 提交订单
![提交订单15331236](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/post_order_ssd.png)
- 处理付款
![处理付款15331213](https://github.com/Evene/Dashboard/blob/master/img/pay_sequence.PNG)

- 添加商品
![添加商品15331217](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/15331217-%E6%B7%BB%E5%8A%A0%E5%95%86%E5%93%81.png)

- 更新商品
![更新商品15331217](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/15331217-%E6%9B%B4%E6%96%B0%E5%95%86%E5%93%81.png)

- 添加种类
![添加种类15331217](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/15331217-%E6%B7%BB%E5%8A%A0%E7%A7%8D%E7%B1%BB.png)

- 删除商品
![删除商品15331198](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/15331198_%E5%88%A0%E9%99%A4%E5%95%86%E5%93%81.PNG)

- 删除种类
![删除种类15331198](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/15331198_%E5%88%A0%E9%99%A4%E5%95%86%E5%93%81%E7%A7%8D%E7%B1%BB.PNG)

- 查看订单
![查看订单15331286](https://github.com/E-Order/Dashboard/blob/master/document/Requirement_Specification/%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE/%E6%9F%A5%E7%9C%8B%E8%AE%A2%E5%8D%95_15331286.png)

  以*查看订单*为例，绘制活动图

<img src = "https://raw.githubusercontent.com/E-Order/Dashboard/master/document/graph/activity.png">

**非功能性需求：**

1. 数据格式：
 价格精确到两位小数。（如12.00）


2. 性能：
 - 可接受至少50桌用户同时点餐
 - 商家实时接收订单消息，延迟不得超过10s

3. 安全性：
  需保障商家用户数据的安全，对账号密码进行保护。
 
4. 可靠性:
- 从远程服务失败中恢复，提供远程服务的本地实现，比如：本地产品信息数据库缓存最常用的一小部分产品信息。
- 限制服务器最大连接数，防止由于服务器负载过重而使用户掉线

5. 可适应性：
  针对第三方服务，创建一个实现了接口的资源适配器对象（主要针对支付功能）
 
 
