---
title: "Array Operations"
date: 2021-01-18T17:16:56+05:30
draft: false
tags: ["ds-algo", "programming", "competitive-programming"]
categories: [dsa, arrays]
sources: []
---

<!--

::Annotation Guide::
~~~~~~~~~~~~~~~~~~~~

* `em` is the modifier

1. em (_text_) - blue underline
2. strong (**text**) - yelow highlight
3. del (~~text~~) - red strike-through

4. em > em (_*text*_) - blue circle
5. em > strong (_**text**_) - lawngreen box
6. em > del (_~~text~~_) - red cross-off
-->

> Insert element in an array

```java
static int insert(int arr[], int n, int x, int capacity, int position) {
    if(n == capacity) return n;
    int idx = position - 1;
    for(int i = n - 1; i >= idx; i--){
    	arr[i + 1] = arr[i];
    }
    arr[idx] = x;
    return n + 1;
    }
```

> Search for an element in an array

```java
static int search(int arr[], int n, int x) {
    for(int i = 0; i < n; i++){
    	if(arr[i] == x)
    		return i;
	}
    return -1;
}
```

> Delete an element in an array

```java
static int delete(int arr[], int n, int x){
   	int i = 0;
   	for(i = 0; i < n; i++) {
   		if(arr[i] == x)
   			break;
   	}
   	if(i == n) return n;
   	for(int j = i; j < n - 1; j++){
   		arr[j] = arr[j + 1];
   	}
   	return n-1;
}
```

> Check if an array is sorted

```java
static boolean isSorted(int[] arr, int n){
	for(int i = 1; i <n; i++){
		if(arr[i] > arr[i-1]) return false;
	}
	return true;
}
```
