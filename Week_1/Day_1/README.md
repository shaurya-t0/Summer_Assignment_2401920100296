1.  Two SUM solution 


class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        vector<int> ans;
        for(int i = 0; i < nums.size() ; i++){
            for (int j = i+1; j< nums.size() ; j++){
                if(nums[i] + nums[j] == target){
                    ans.push_back(min(i,j));
                    ans.push_back(max(i,j));
                }
            }
        }
        return ans; 
    }
    
};



2.  Remove Duplicates from Sorted Array Solution 



class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        int k =0;
        for (int i= 0; i< nums.size(); i++){
            if(i==0 || nums[i]!=nums[i-1]){
                nums[k]=nums[i];
                k++;
            }
        }
        return k;
    }
};


3.  Best Time to Buy and Sell Stock Solution 



class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int minPrice = INT_MAX;
        int maxProfit = 0;
        for(int i=0; i < prices.size(); i++){
            int price=prices[i];
            minPrice=min(minPrice,price);
            int profit = price - minPrice;
            maxProfit = max(maxProfit , profit);
        }
        return maxProfit;
    }
};





