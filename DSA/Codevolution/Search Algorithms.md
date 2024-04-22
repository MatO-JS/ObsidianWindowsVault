
## Linear Search

#### Problem : Given an array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.


```javascript

function linearSearch(arr,target){

	for(let i =0;i<arr.length;i++){
	
		if(arr[i]===target){
			return i
					}
				}
		return -1;

		}

console.log(linearSearch([45,89,10,0,11,22],22));
console.log(linearSearch([88,23,55],1));

```

```java

public class Main {

	public static int linearSearch(int[] array,int target){
		for(int i =0;i<array.length;i++){
			if(array[i]==target){
				return i;
			}

		}
			return -1;
	}

	public static void main(String[] args) {
	int[] array = {45,22,55,22};
	int target = 0;

	System.out.println(linearSearch(array,target));
	
	
	}
}
```

## Binary Search

##### Given a sorted array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.

> BINARY SEARCH ONLY WORKS ON A SORTED ARRAY


## Pseudo code for binary search of a sorted array



![[Screenshot 2024-04-10 191205.png]]