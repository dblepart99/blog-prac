---
title: 정렬
date: 2021-09-01 16:37:47
categories: 알고리즘
tags:
  - 알고리즘
  - 정렬
  - 선택정렬
sitemap: true
---

## Selection Sort

As you can see the word "Selection". This algorithm always chooses the most minimum element in the array repeatedly from unsorted part and swap with the first element of unsorted part.

이름에서 볼 수 있듯 "선택"하는 정렬입니다. 이 알고리즘은 항상 배열이 정렬되지 않은 부분에서 최소의 원소를 정렬되지 않은 부분의 맨 앞으로 가져와 정렬합니다.

```
arr = [10, 20, 3, 7, 5]
설명을 위해 "|"를 기준으로 구분하겠습니다. unsorted part|sorted part
=> | 10 20 3 7 5
=> 3 | 10 20 7 5
=> 3 5 | 10 20 7
=> 3 5 7 | 10 20
=> 3 5 7 10 | 20
=> 3 5 7 10 20
```

```python
def selectsort(array):
    for i in range(len(array)):
        min_idx = i  #index of the minimum value
        for j in range(i + 1, len(array)):
            if array[min_idx] > array[j]:
                min_idx = j
        array[i], array[min_idx] = array[min_idx], array[i]

    return array
```

```python
arr = [10, 20, 3, 7, 5]
```

```python
selectsort(arr)
```

    [3, 5, 7, 10, 20]

선택 정렬은 N-1번 만큼 가장 작은수를 찾아서 맨 앞으로 보내야합니다. (N번이 아닌 이유는 선택받지 못한 가장 마지막 원소는 가장 큰 원소이기 때문입니다.) 시간복잡도로 따지면 반복문이 이중 중첩이므로 O(N^2)입니다.

## Insertion Sort

삽입 정렬도 이름에서 볼 수 있듯이 매우 직관적입니다. 삽입 정렬은 원소를 특정한 위치에 적절히 삽입합니다.
"적절히"라는 말이 참 애매할 수 있지만, 이 보다 더 정확한 표현도 없을 것 같습니다.

```python
def insertionsort(array):
    for i in range(1, len(array)):
        for j in range(i, 0, -1):
            if array[j] < array[j-1]:
                array[j], arr[j-1] = array[j-1], array[j]
            else:
                break
    return array
```

```python
arr = [10, 20, 3, 7, 5]
```

```python
insertionsort(arr)
```

    [3, 5, 7, 10, 20]

```python

```
