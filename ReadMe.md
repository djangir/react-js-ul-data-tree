# React Js Data Tree

use this to create your own tree in your browser.

### npm install react-js-data-tree-01
![Screenshot from 2022-08-12 11-18-50](https://user-images.githubusercontent.com/87252360/184292625-7ed6e676-ad98-4894-b260-fa77de3dea3d.png)

# Requirements

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

```
<Tree data={data} />

```
## extra props

```<Tree data={data} heading="Tree Heading" /> ```
 
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
