# React Js Data Tree
React Js Data Tree is a package that allows you to easily create a tree structure in your web application. With React Js Data Tree, you can pass your data object or array, and it will be displayed as a tree structure. This package is easy to use and customizable, allowing you to add additional HTML data and customize the styles of each box in the tree.

Installation
To use React Js Data Tree, you will need to install the package using npm. To install, open your terminal and type the following command:

### <a href="https://www.npmjs.com/package/react-js-data-tree-01" target="_blank"> npm install react-js-data-tree-01 </a>
![Screenshot from 2022-08-12 11-18-50](https://user-images.githubusercontent.com/87252360/184292625-7ed6e676-ad98-4894-b260-fa77de3dea3d.png)

### with extra html

<img width="1409" alt="Screenshot 2023-04-15 at 8 54 49 PM" src="https://user-images.githubusercontent.com/87252360/232234020-61179e19-14f6-4d1c-af2d-95f5d144c2a3.png">


Getting Started
To get started with React Js Data Tree, you will need to pass your data object or array to the Tree component. Here is an example of how to use the Tree component:

# Requirements

```
import React from 'react';
import { Tree } from 'react-js-data-tree-01';

```

```
let data = {
  "id": "0001",
  "type": "data tree",
  "name": "user",
  "child Data": {
    "array": [
      { "id": "1", "type": "new" },
      { "id": "2", "type": "new 1" },
      { "id": "3", "type": "new 2" },
      { "id": "4", "type": "new 3" }
    ]
  },
  "else arr": [
    { "id": "10001", "type": "None" },
    { "id": "10002", "type": "asdf" },
    { "id": "10005", "type": "adsfd" },
    { "id": "10007", "type": "ads" },
    { "id": "10006", "type": "d gdg " },
    { "id": "10003", "type": "d fdsf ds" },
    { "id": "10004", "type": "aaa" }
  ]
}
```



In this example, we import the Tree component from the react-js-data-tree-01 package and pass our data object to it using the data prop. This will render our data object as a tree structure in the browser.

## Props
The Tree component accepts several props that allow you to customize the tree structure and add additional functionality.

## data (required)
The data prop is the only required prop for the Tree component. This is the data object or array that you want to display as a tree structure. Here is an example of how to use the data prop:




```
<Tree data={data} />

```
## heading
The heading prop allows you to add a heading to the top of the tree structure. This prop is not required. Here is an example of how to use the heading prop:

```<Tree data={data} heading="Tree Heading" /> ```
 
 
 
 
 treeStyle
The treeStyle prop allows you to style the outer div of the tree structure. This prop is not required. Here is an example of how to use the treeStyle prop:

```
<Tree data={data} treeStyle={{ background: 'red' }} />
```

## boxStyle
The boxStyle prop allows you to style each box in the tree structure. This prop is not required. Here is an example of how to use the boxStyle prop:
 
 
 
------------------------

## properties :-

------------------
------------------

| name          | isRequired | type | example | about |  
| :---:          |  :---:     |      :---:|  :---:| :---:|  
| data | required | array or object | data= {['name', 'age']} or data = {{name:'user', age:30}} |  Data is the object or array that you want to show in the tree. 
| heading |not required | "string" | heading="string" |  Heading is the data that will be heading in the tree 
| treeStyle |not required | style object | treeStyle = {{background:'red'}} |   The outer div of the tree will be styled in TreeStyle. | 
| boxStyle |not required | style object | boxStyle = {{background:'red'}} | Each box in the tree will be styled with BoxStyle. | 
| extraHtml |not required | function | extraHtml = ```{(data)=>{ console.log(data) return(<div>yourHtml</div>)}}``` |   If any other HTML data is to be shown inside the box then it can be shown by extraHtml|
| branchExtraHtml |not required | function | branchExtraHtml = ```{(data)=>{ console.log(data) return(<div>yourHtml</div>)}}``` | Where a branch is being built and some extra data is to be shown on it, then it will be shown through branchExtraHtml.|
| onClick |not required | function | onClick = ```{(data)=>{ console.log(data)}}``` |If you want to do something on click of box then have to use onClick function it will return 2 parameters. 1st the data of that box and 2nd if getDataOnClick has been sent in it then that|
| onClickBranch |not required | function | onClickBranch = ```{(data)=>{ console.log(data) return(<div>yourHtml</div>)}}``` |Same as onclick but it will return 2nd param getDataOnClickBranch|
| getDataOnClick |not required | string | getDataOnClick = 'your key in data' | |
| getDataOnClickBranch |not required | string | getDataOnClickBranch = 'your key in data' || 
| showKey |not required | string | showKey = 'your key in data' |showKey is the key show that you want to show|
| showBranchKey |not required | string | showBranchKey = 'your key in data' |showBranchKey is the key show that you want to show in branch box.|
| hideKey |not required | string | hideKey = 'your key in data' | hideKey  is the key that you want to hide from box|
--------------------------------------



You can customize the tree by passing in additional props, such as a heading, styles, or event handlers. Here's an example:


```
<Tree
  data={data}
  heading="Tree Heading"
  treeStyle={{ background: 'red' }}
  boxStyle={{ background: 'blue' }}
  onClick={(data) => console.log(data)}
  extraHtml={(data) => <div>Extra HTML for {data.type}</div>}
/>
```
