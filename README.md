# algorithm

## Bài giải
### Tìm dãy con tăng liên tiếp có độ dài lớn nhất
&nbsp;
```c
 1. #include<iostream>
 2. using namespace std;
 3. int main(){
 4.    int n,arr[100];
 5.        cin>>n;
 6.    for(int i  =0;i<n;i++)
 7.        cin>>arr[i];
 8.    int nonContain = 1,contain=1,index=0;
 9.    for(int i =0;i<n;i++){
10.        if(arr[i]>arr[i-1]) contain++;
11.        else contain = 1;
12.        if(contain>nonContain){
13.            index = i;
14.            nonContain = contain;
15.        }
16.    }
17.    for(int i = index-nonContain+1;i<index+1;i++)
18.        cout<<arr[i]<<" ";
19.    return 0;
20. }
```

#### Độ phức tạp:O(n)
