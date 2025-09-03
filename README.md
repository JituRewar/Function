# Function
FACTORIAL CODE BY HELP OF FUNCTION


#include<iostream>
using namespace std;
//function deffination
int fact(int a){
    int s =1;
    for(int i=1;i<=a;i++){
        s = s*i;
    }
    return s;

    }
int main(){
    // function call
   

    cout<<fact(6)<<endl;
    return 0;
}
