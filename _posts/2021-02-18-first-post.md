---
title: "백준 2164번 c++ 풀이 "
date: 2021-02-18 05:24:00
categories: 백준 문제풀이
---

```cpp
#include<iostream>
#include<algorithm>
#include<cstring>
#include<vector>
#include<string>
#include<math.h>
#include<stack>
#include<queue>
using namespace std;

int main() {

	int n;
	cin >> n;

	queue<int> array;

	for (int i = 1; i <= n; ++i) {
		array.push(i);
	}
	while (array.size() != 1) {
		array.pop();
		array.push(array.front());
		array.pop();
	}

	cout << array.front() << '\n';
}
```
