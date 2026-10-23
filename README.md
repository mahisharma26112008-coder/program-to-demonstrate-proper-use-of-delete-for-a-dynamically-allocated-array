# program-to-demonstrate-proper-use-of-delete-for-a-dynamically-allocated-array

#include<iostream>
 using namespace std;
int main(){
 int n;
    cout<<"enter size";
    cin>>n;

    int *p=new int[n];

    cout<<"enter"<<n<<"values"<<"\n";
    for(int i=0;i<n;i++){
        cin>>p[i];
    }

   for(int i=0;i<n-1;i++){
       for(int j=0;j<n-1-i;j++){
           if(p[j]>p[j+1]){
               int temp=p[j];
               p[j]=p[j+1];
               p[j+1]=temp;
           }
       }
   }
    cout<<"sorted array";
    for(int i=0;i<n;i++){
        cout<<p[i]<<" ";
    }

    delete[] p;

    return 0;
}
