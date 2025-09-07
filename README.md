DSA DAY 3


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




🚀 DSA Series – Day 8
📌 Topic: Maximum Subarray Sum (Kadane’s Algorithm)

✨ Key Learnings:
🔹 The problem is to find the contiguous subarray (within a one-dimensional array) that has the largest sum.
🔹 Brute force approach has O(n²) or O(n³) time complexity.
🔹 Kadane’s Algorithm optimizes it to O(n) by keeping track of the maximum subarray ending at each index.

💡 Approach (Kadane’s Algorithm)

Initialize two variables:

max_so_far = -∞

current_sum = 0

Traverse the array:

Add the current element to current_sum.

Update max_so_far if current_sum is greater.

If current_sum becomes negative, reset it to 0.

Return max_so_far as the result.

// CODE 
#include<iostream>
#include<vector>
#include<climits>
using namespace std;

// optimised solution o(n*2)

// int main(){
//     int arr[] = {1,2,3,4,5};
//     int n = 5;
//     int maxsum = INT_MIN;
//     for(int st=0;st<n;st++){
//         int currSUM = 0;
//         for(int end = st;end<n;end++){
//            currSUM+=arr[end];
//             maxsum = max(currSUM,maxsum);
           
//         }
        
//     }
//     cout<<"max subarray sum :"<<maxsum;
//     return 0;
// }


// MOST OPTIMISED O(N);
// kadane's algorithim

int main(){
    int arr[] = {3,-4,4,5,7,8,-9,8};
    int n = sizeof(arr)/sizeof(arr[0]);
    int currentsum = 0 , maximumsum = INT_MIN;
    for(int i=0;i<n;i++){
        currentsum = currentsum + arr[i];
        maximumsum = max(maximumsum,currentsum);
        if(currentsum < 0){
            currentsum = 0;
        }
    }
    cout<<maximumsum;

    return 0;
}

✅ Example Output

For input:
[-2, 1, -3, 4, -1, 2, 1, -5, 4]

Output:
Maximum Subarray Sum: 6
⚡ Kadane’s Algorithm is a must-know for interviews as it teaches dynamic programming and greedy concepts in one go!
