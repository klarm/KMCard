<p align="center" >
  <img src="https://github.com/klarm/KMCard/blob/master/logo.png" width="139" height="90" alt="RVCard" title="RVCard">
</p>

# Introduction
**RVCard** is a lightweight, high-performance solution for creating dynamic UI components. It supports building reusable UI components by writing XML layoutsand you can aslo build flexible combinations of them. There are various forms of embedding RVCard in your existing code. See the **Demo** and **How to Start** for more details.  

[中文文档](/README_CN.md)

# Main Features
- It supports building UI components by writing XML layouts with standard Flex syntax.
- It layouts and combines UI components asynchronously for high performance.
- It supports custom tags and attributes in XML layouts.
- It supports the adaptation of both protocol-standard data and structured non-standard data.

# Demo 
The demo app contains the following examples:
<img src="https://github.com/klarm/KMCard/blob/master/demos.png"/>

# How to Use
There are three ways to use RVCard in your project:
- Use it as a whole page
	- step 0: Add RVCardView to your page
	- step 1: Set page data for RVCardView
	- step 2: Call reload of RVCardView

- Use it as an independent UI component or a combination of them
	- step 0: Call buildRVView of RVSkinParser when you use it as an independent UI component
	- step 1: Call buildAssembledRVSkins of RVSkinAssembler when you use it as a combination of UI components
	- step 2: Then the method above returns a common view, use it as usual

- Use it for structured non-standard data
	- step 0: Implement four delegates
	- step 1: Implement a data binder method 
	- step 2: Register the above binder for a certain layout
   
# License
Licensed under the [MIT](https://github.com/klarm/KMCard/blob/master/LICENSE) License.
