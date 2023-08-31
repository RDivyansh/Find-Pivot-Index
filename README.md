# Find-Pivot-Index

class Solution {
public:
    int pivotIndex(vector<int>& nums) {
        int lsum = 0,rsum= 0;
        int sum = 0;
        for(int i=0;i<nums.size();i++){
            sum += nums[i];
        }
        rsum = sum;
        for(int i=0;i<nums.size();i++){
        rsum -= nums[i];
        if(lsum == rsum){
                return i;
        }
        lsum+=nums[i];
        }
return -1;
    }
};
