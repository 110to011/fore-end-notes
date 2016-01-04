### 如何实现两个数组的合并？

> 思路：同时对两个数组进行遍历，设置两个标志位i,j，用来记录遍历的位置  
将两个数组中较小的值插入到新数组中，然后将标志向前移动一个位置，重复比较，直到搜索值都插入到数组中。  

```js
function con(arrA,arrB){
   var i , j , k, lenA = arrA.length, lenB = arrB.length , allLen = lenA + lenB,result = [];
   for(i=0,j=0,k =0; k < allLen; k++ ){
       if(i < lenA &&(j >= lenB || arrA[i] < arrB[j])){
           result.push(arrA[i++]); 
       }else{
            result.push(arrB[j++]);
       }
   }
   return result;
}
var ar1 = [1,4,2],ar2 = [9,3,10];
console.log(con(ar1,ar2));
```

### 如何实现多个数组的合并？

> 思路：  
* 取得需要连接的数组的个数  
* 将第一个数组放入结果数组中  
* 从第二个数组元素开始循环，每次调用两个数组连接的方法  
* 将上一次合并的结果作为下一次合并时的第一个参数，重复进行，直至传入的参数遍历完
* 最后将合并完成后的结果进行排序

```js
function concatMore() {
	var len = arguments.length,result = arguments[0],i;

	for(i = 1;i < len;i++) {
		result = con(result,arguments[i]);
	}

	return result.sort(function(a,b) {return a-b;});
}
```
