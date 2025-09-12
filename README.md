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
 CODE 
 MOST OPTIMISED O(N);
 kadane's algorithim


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




🚀 DSA Series – Day 9
📌 Topics Covered

Moore’s Voting Algorithm for finding the Majority Element

LeetCode #168 – Excel Sheet Column Title problem-solving

✨ Key Learnings

Understood how Moore’s Voting Algorithm maintains a candidate and count to efficiently identify the majority element.

Learned why the algorithm runs in O(n) time and uses only O(1) space, making it optimal.

Practiced edge cases where the array might not contain a majority element.

Explored how to convert numbers into Excel column titles (e.g., 1 → A, 28 → AB).

💻 Code

Check out my implementation 

 vector<int> nums = {1,21,4,21,21};

int freq = 0,ans = 0;

int n = nums.size();
for(int i=0;i<n;i++){
    if(freq==0){
        ans = nums[i];
    }
    if(ans==nums[i]){
        freq++;
    }
    else freq--;
}  
cout<<ans;
return 0;



🔥 Slowly building consistency, one day at a time.
#DSA #C++ #MooreVoting #LeetCode #CodingJourney #IIITKota



🚀 DSA Series – Day 10
📌 Topic: Time and Space Complexity

✨ Key Learnings:
🔹 Understood how to analyze the efficiency of algorithms.
🔹 Learned about Big-O, Big-Theta, and Big-Omega notations.
🔹 Differentiated between time complexity (execution speed) and space complexity (memory usage).
🔹 Explored examples like constant O(1), linear O(n), logarithmic O(log n), and quadratic O(n²) complexities.

💡 Takeaway:
Efficient coding = balancing both time ⏱️ and space 💾.



🚀 DSA Series – Day 11
📌 Topic: Best Time to Buy and Sell Stock (Max Profit Problem)

✨ Key Learnings:
🔹 Understood how to track the minimum price while iterating through the array.
🔹 Learned how to calculate maximum profit by comparing with the current price.
🔹 Time Complexity: O(n) | Space Complexity: O(1)

💻 Practice Problem:
LeetCode #121 – Best Time to Buy and Sell Stock

    int maxProfit(vector<int>& prices) {
        int bestbuy = prices[0],maxProfit=0;
        for(int i=0;i<prices.size();i++){
            if(prices[i]>bestbuy){
                maxProfit = max(maxProfit,prices[i]-bestbuy);
            }
            bestbuy = min(bestbuy,prices[i]);
        }
        return maxProfit;
        
    }

