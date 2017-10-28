## Depth First Search ** Time O(n), Space O(h == height of tree)**
[Link](https://dev.to/vaidehijoshi/demystifying-depth-first-search)

![](./images/2017-10-26-22-25-50.png)
![](./images/2017-10-26-22-26-04.png)
![](./images/2017-10-26-22-28-06.png)
![](./images/2017-10-26-22-28-21.png)
![](./images/2017-10-26-22-36-50.png)
![](./images/2017-10-26-22-40-52.png)
![](./images/2017-10-26-22-46-38.png)


```js
node1 = {  
  data: 1,  
  left: referenceToLeftNode,  
  right: referenceToRightNode  
};

function preorderSearch(node) {  
  // Check that a node exists.  
  if (node === null) {  
    return;  
  }
  // Print the data of the node.  
  console.log(node.data);  

  // Pass in a reference to the left child node to preorderSearch.  
  // Then, pass reference to the right child node to preorderSearch.  
  preorderSearch(node.left);  
  preorderSearch(node.right);  
}

```