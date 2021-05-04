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

|           |   1   |   2   |   3   |   4   |   5   |   6   |   7   |   8   |   9   |  10   |  평균   |
| :-------: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :-----: |
|  n=1,000  |   7   |   8   |   5   |   6   |   8   |   5   |   6   |   6   |   4   |   4   |   5.9   |
| n=10,000  |  139  |  108  |  110  |  102  |  101  |  110  |  111  |  105  |  101  |  111  |  109.8  |
| n=100,000 | 13016 | 12931 | 12808 | 12812 | 13078 | 12697 | 13037 | 12727 | 12598 | 12853 | 12855.7 |

  ![버블 정렬 그래프](file:///C:\Users\82104\AppData\Local\Temp\DRW00001d3455ab.gif)  



**2. 선택 정렬**

|           |  1   |  2   |  3   |  4   |  5   |  6   |  7   |  8   |  9   |  10  |  평균  |
| :-------: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :----: |
|  n=1,000  |  5   |  2   |  4   |  3   |  6   |  3   |  4   |  3   |  4   |  3   |  3.7   |
| n=10,000  |  45  |  51  |  48  |  45  |  40  |  46  |  39  |  45  |  39  |  47  |  44.5  |
| n=100,000 | 3604 | 3645 | 3710 | 3602 | 3526 | 3609 | 3658 | 3673 | 3976 | 3825 | 3682.8 |

  ![img](file:///C:\Users\82104\AppData\Local\Temp\DRW00001d3455b1.gif)  



**3. 삽입 정렬**

|           |  1   |  2   |  3   |  4   |  5   |  6   |  7   |  8   |  9   |  10  | 평균  |
| :-------: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :---: |
|  n=1,000  |  4   |  2   |  3   |  3   |  3   |  2   |  2   |  3   |  2   |  2   |  2.6  |
| n=10,000  |  14  |  15  |  17  |  21  |  21  |  20  |  17  |  13  |  22  |  18  | 17.8  |
| n=100,000 | 825  | 851  | 862  | 853  | 846  | 845  | 889  | 902  | 862  | 847  | 858.2 |

  ![img](file:///C:\Users\82104\AppData\Local\Temp\DRW00001d3455c6.gif)      



**4. 쉘 정렬**

|           |  1   |  2   |  3   |  4   |  5   |  6   |  7   |  8   |  9   |  10  | 평균 |
| :-------: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
|  n=1,000  |  0   |  1   |  1   |  1   |  0   |  0   |  1   |  1   |  1   |  1   | 0.7  |
| n=10,000  |  5   |  5   |  5   |  4   |  5   |  3   |  4   |  4   |  4   |  4   | 4.3  |
| n=100,000 |  20  |  17  |  19  |  21  |  19  |  17  |  22  |  16  |  17  |  17  | 18.5 |

  ![img](file:///C:\Users\82104\AppData\Local\Temp\DRW00001d3455cc.gif)  



## 결과

n=1,000개 일 때, 버블, 선택, 삽입 순으로 각각 5.9ms, 3.7ms, 2.6ms

n=10,000개 일 때, 각각 109.8ms, 44.5ms, 17.8

n=100,000개 일 때, 각각 12855.7ms, 3682.8ms, 858.2ms

위 결과를 토대로 삽입>선택>버블 순으로 성능이 좋음을 알 수 있고, 이 차이는 n이 커지면 커질수록 심해집니다.

이제 쉘 정렬을 보면

n=1,000개 일 때, 0.7ms

n=10,000개 일 때, 4.3ms

n=100,000개 일 때, 18.5ms

으로 위 3개의 정렬보다 월등히 좋은 성능을 나타내는 걸 알 수 있습니다.

결국 이 실험을 통해 정렬 알고리즘의 성능은 쉘>>>>>>>>>삽입>선택>버블 순으로 좋다는걸 알 수 있습니다.

## 전체 코드

```
import java.util.Random;

public class sort {

    public static int[] bubble_sort(int[] list){
        int temp;
        for(int pass = 1; pass < list.length; pass++){
            for(int i = 1; i < list.length - pass + 1; i++){
                if(list[i-1] > list[i]){
                    temp = list[i-1];
                    list[i-1] = list[i];
                    list[i] = temp;
                }
            }
        }
        return list;
    }

    public static int[] selection_sort(int[] list){
        int min, temp;
        for (int i = 0; i < list.length - 1; i++) {
            min = i;
            for (int j = i + 1; j < list.length; j++){
                if (list[j] < list[min])
                    min = j;
            }
            temp = list[i];
            list[i] = list[min];
            list[min] = temp;
        }
        return list;
    }

    public static int[] insertion_sort(int[] list){
        int CurrentElement;
        for(int i = 1; i < list.length; i++){
            CurrentElement = list[i];
            int j = i-1;
            while(j>=0 && list[j] > CurrentElement){
                list[j+1] = list[j];
                j--;
            }
            list[j+1] = CurrentElement;
        }
        return list;
    }


    public static int[] shell_sort(int[] list){
        int gap, temp;
        gap = list.length/2;

        while(gap != 0){
            for(int i=0; i<gap; i++){
                for(int p=i+gap; p<list.length; p+=gap){
                    int key = list[p];
                    int j= p-gap;
                    while(j>=0){
                        if(key<list[j]){
                            list[j+gap] = list[j];
                        }
                        else
                            break;
                        j -= gap;
                    }
                    list[j+gap] = key;
                }
            }
            gap /= 2;
        }
        return list;
    }

    public static void main(String args[]){
        int n = 1000;
        int[] list = new int[n];

        Random random = new Random();
        for(int i=0; i<n; i++){
            list[i] = random.nextInt(100000);     //괄호 안 숫자까지의 난수 생성
        }

        long beforetime = System.currentTimeMillis();   //정렬 실행 전 시간체크
        shell_sort(list);                               //정렬 바꾸면서 실험
        long aftertime = System.currentTimeMillis();    //정렬 실행 후 시간체크

        long time = (aftertime - beforetime);           //후-전으로 걸린 시간찾기

        for(int i=0; i<n; i++){
            System.out.println(list[i]);
        }
        System.out.print("걸린 시간 : " + time + "ms");
    }
}
```