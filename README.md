<p align="center" >
  <img src="https://github.com/klarm/KMCard/blob/master/logo.png" width="139" height="90" alt="RVCard" title="RVCard">
</p>

# Introduction
**RVCard** is a lightweight, high-performance solution for creating dynamic UI components. It supports building reusable UI components by writing XML layouts and supports flexible combinations between UI components. There are various forms of embedding RVCard in your existing implementation. See the **Demo** and **How to Start** for more detail.

# Main Features
- Supports the description of UI components by writing XML layouts with standard flex syntax.
- layout and combine UI components asynchronously，high-performance.
- Supports custom tags and attributes in XML layouts.
- Supports adaptation protocol-standard data structure and structured non-standard data.

# Demo
 <img src="https://github.com/klarm/KMCard/blob/master/demos.png"/>

# How to Use

- adoption as a whole page
	- step 0:
	- step 1:
	- step 2:
done!

- adoption as independent UI component or combination of them
	- step 0:
	- step 1:
	- step 2:
done!

- adoption for structured non-standard data
	- step 0:
	- step 1:
	- step 2:
done!
   
# License
[MIT]

---
# 简介
**RVCard** 是一个轻量级高性能动态UI组件的方案，它支持通过编写XML布局构建可复用的UI组件，并且支持UI组件之间的各种灵活组合。使用方式上，可以通过各种形式灵活嵌入你的现有实现。具体案例请参见demo。

# 主要特性
- 支持通过编写XML布局描述UI组件，支持标准flex排版
- 支持布局之间的各种灵活组合
- 布局排版和组合支持异步执行，提高UI流畅性
- 支持自定义tag及属性，方便业务方灵活扩展并隔离代码
- 支持适配协议标准数据结构和结构化非标准数据

# 样例
 <img src="https://github.com/klarm/KMCard/blob/master/demos.png"/>
 具体细节请参见Demo工程

# 怎样使用
有三种使用方式：
- 整页使用RVCard
  + Step 0：将RVCardView嵌入页面
  + Step 1：设置RVCardView的PageData
  + Step 2：触发RVCardView的reload
  
- 直接使用UI组件或其组合 
  + Step 0：若直接使用UI组件，调用RVSkinParser的下列方法：
	```obj-c
	+ (UIView *)buildRVView:(NSString *)xmlFile rootRect:(CGRect)frame data:(id)data refresher:(SkinBinderBlock)refresher;

	+ (UIView *)buildRVView:(NSString *)xmlFile rootRect:(CGRect)frame data:(id)data refresher:(SkinBinderBlock)refresher 	completionBlock:(layoutCompletionBlock)completionBlock;

	+ (UIView *)buildRVView:(NSString *)xmlFile rootRect:(CGRect)frame data:(id)data refresher:(SkinBinderBlock)refresher 		completionBlock:(layoutCompletionBlock)completionBlock config:(RVSkinConfig*)config;  
 	```

  + Step 1：若使用UI组件的组合，调用RVSkinAssembler的下列方法：
	```obj-c
	+ (UIView *)buildAssembledRVSkins:(NSArray *)skinItems rootRect:(CGRect)frame pattern:(NSDictionary *)pattern dataArray:(NSArray *)skinDatas;
	
	+ (UIView *)buildAssembledRVSkins:(NSArray *)skinItems rootRect:(CGRect)frame pattern:(NSDictionary *)pattern dataArray:(NSArray *)skinDatas refreshers:(NSArray *)refreshers;
 	```
	
  + Step 2：像普通View一样使用上述方法的返回的View
  
- 适配结构化任意结构数据列表
  + Step 0：业务方使用系列四个delegate：
    ```obj-c
	typedef NSString*(^getSkin)(NSInteger idx);
	typedef NSDictionary*(^getPattern)();
	typedef id(^getItemData)(NSInteger idx);
	typedef NSInteger(^getItemCount)();
     ```
  + Step 1：业务方实现并注入binder：
  	```obj-c
  	typedef void(^SkinBinderBlock)(RVSkinBinderData *data, badgeAttacher attacher);
  	```
	
整体如下图所示： 
       <img src="https://github.com/klarm/KMCard/blob/master/dataBinder.png" width ="40%"/>
       
详细细节请参考demo
