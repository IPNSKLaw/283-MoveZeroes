# 283-MoveZeroes
void moveZeroes(int* nums, int numsSize){
    int save[numsSize];
    int j = 0, k = 0;
    for(int i = 0; i <= numsSize - 1; i ++){
        if(nums[i] == 0){
            save[numsSize - 1 - k] = nums[i];
            k++;
        }
        else{
            save[j] = nums[i];
            j++;
        }
    }
    for(int i = 0; i <= numsSize - 1; i ++){
        nums[i] = save[i];
    }

}
