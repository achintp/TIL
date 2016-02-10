#Three way paritioning

A way to divide an unsorted array into three different sections, with the first
having elements greater than the median, the second having elements equal to the
median and the third having elements less than median. O(n) running time.

```
void three_way_partition(vector<int>& nums, int median){
    int sz = nums.size()-1;
    int i = 0;
    int j = 0;

    while(j <= sz){
        if(nums[j] > med){
            swap(nums[i++], nums[j++]);
            continue;
        }
        if(nums[j] == med){
            j++;
            continue;
        }
        if(nums[j] < med){
            swap(nums[sz--], nums[j++]);
            continue;
        }
    }
}

```
