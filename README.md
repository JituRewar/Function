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

✅ Example Output

For input:
[-2, 1, -3, 4, -1, 2, 1, -5, 4]

Output:
Maximum Subarray Sum: 6
⚡ Kadane’s Algorithm is a must-know for interviews as it teaches dynamic programming and greedy concepts in one go!
