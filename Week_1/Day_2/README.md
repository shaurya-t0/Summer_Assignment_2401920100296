day2 solutions

1.  Maximum Subarray Solution 

class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int maxSum = INT_MIN;
        int sum=0;
        for(int i=0; i<nums.size(); i++){
            sum=sum+nums[i];
            maxSum= max(maxSum,sum);
            if(sum<0){
                sum=0;
            }
        }
        return maxSum;
    }
};


2.  Contains Duplicate Solution

class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        sort(nums.begin() , nums.end());
        for(int i=1 ; i < nums.size() ; i++){
            if(nums[i] == nums[i-1]){
                return true;
            }
        }
        return false;
    }
};


3.  Maximum Average Subarray Solution
