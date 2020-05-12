class Solution {
public:
    int singleNonDuplicate(vector<int>& nums) {
        if(nums.size() == 1) return nums[0];
        int l = 0;
        int h = nums.size()-1;
        while(l < h){
            int mid = l + (h-l)/2;
            bool isEven = (h-mid)%2==0;
            if(nums[mid] == nums[mid+1]){
                if(isEven)
                    l = mid+2;
                else
                    h = mid-1;
            } else if(nums[mid] == nums[mid-1]){
                if(isEven)
                    h = mid-2;
                else
                    l = mid+1;
            } else
                return nums[mid];
        }
        return nums[l];
    }
};
