# JumpSearch
#include&lt;iostream> using namespace std; #include&lt;cmath>   int jumpsearch(int arr[],int length,int key){     int left=0;     int right = sqrt(length);      while(key&lt;=arr[right] &amp;&amp; right&lt;length){   //if it is not right block         left=right;         right+=sqrt(length);         if(right>length-1){             right=length;         }     }  for(int i=left;i&lt;=right;i++){     if(arr[i]==key){         return i;     } } }  int main(){     int arr[15]={1,2,3,4,5,6,7,8,22,33,44,55,66,77,88};     int key=22;     int length=15;     // int length=sizeof(arr)/sizeof(arr[0]);     int x=jumpsearch(arr,length,key);     if(x==key){         cout&lt;&lt;"position of key is"&lt;&lt;x&lt;&lt;endl;     }     else      {      cout&lt;&lt;"key dose not exist";     }     return 0;
