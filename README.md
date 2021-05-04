# 202001604 강현구 정렬 알고리즘 성능 비교

## 1. 버블 정렬, 선택 정렬, 삽입 정렬, 쉘 정렬 코드

![버블 정렬](C:\Users\82104\Desktop\버블정렬.PNG)

![선택 정렬](C:\Users\82104\Desktop\선택정렬.PNG)

![삽입 정렬](C:\Users\82104\Desktop\삽입정렬.PNG)

![쉘 정렬](C:\Users\82104\Desktop\쉘정렬.PNG)

## 2. 성능 비교 방법

정렬 알고리즘의 성능은 **걸리는 시간**이므로 currentTimeMillis를 사용했습니다. 정렬 시작 전과 후의 시간을 체크하여 (후-전)을하여 걸린 시간을 (ms)단위로 표시하였습니다.

![](C:\Users\82104\Desktop\성능비교 방법.PNG)

![n=1,000일 때 정렬된 배열의 일부와 걸린 시간](C:\Users\82104\Desktop\결과라라라랑.PNG)

## 3. 성능 비교

성능 비교는 각각의 정렬을 n=1,000, n=10,000, n=100,000으로 측정하였고, 각각 10번씩 측정해 평균을 내었습니다.

**1. 버블 정렬**

|           |  1   |  2   |  3   |  4   |  5   |  6   |  7   |  8   |  9   |  10  | 평균 |
| :-------: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
|  n=1,000  |  7   |  8   |  5   |  6   |  8   |  5   |  6   |  6   |  4   |  4   |      |
| n=10,000  | 139  | 108  | 110  | 102  | 101  | 110  | 111  | 105  | 101  | 111  |      |
| n=100,000 |      |      |      |      |      |      |      |      |      |      |      |

