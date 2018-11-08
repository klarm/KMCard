<p align="center" >
  <img src="https://github.com/klarm/KMCard/blob/master/logo.png" width="139" height="90" alt="RVCard" title="RVCard">
</p>

# Introduction
**RVCard** is a lightweight, high-performance solution for creating dynamic UI components. It supports building reusable UI components by writing XML layouts and flexible combinations of UI components. There are various forms of embedding RVCard in your existing implementation. See the **Demo** and **How to Start** for more detail.  

[中文文档](/README_CN.md)

# Main Features
- Supports describing UI components by writing XML layouts with standard flex syntax.
- layouts and combines UI components asynchronously，high-performance.
- Supports custom tags and attributes in XML layouts.
- Supports adaptation both protocol-standard data structure and structured non-standard data.

# Demo 
the demo app contains the following:
<img src="https://github.com/klarm/KMCard/blob/master/demos.png"/>

# How to Use
There are three ways to use RVCard in your project:
- adoption as a whole page
	- step 0: Add RVCardView to your page
	- step 1: Set page data for RVCardView
	- step 2: Call reload of RVCardView

- adoption as independent UI component or combination of them
	- step 0: Call buildRVView of RVSkinParser when you use independent UI component
	- step 1: Call buildAssembledRVSkins of RVSkinAssembler when you use combination of UI component
	- step 2: Then the method above returns a common view, use it as usual

- adoption for structured non-standard data
	- step 0: Implement four delegates
	- step 1: Implement a data binder method 
	- step 2: Register the binder for a certain layout
   
# License
Licensed under the [MIT](LICENSE.txt) License.
