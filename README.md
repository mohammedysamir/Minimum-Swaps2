# Minimum-Swaps2
Problem in HackerRank Difficulty  Medium  Max Score  40
### i made the function
```cpp
int minimumSwaps(vector<int> arr) {
int swaps=0,Size=arr.size();
vector<int>::iterator index;
for(int i=0;i<Size-1;i++){
    if(i+1==arr[i])continue;//in the right place
        else{
           index=find(arr.begin()+i,arr.end(),i+1);
           swap(arr[i],*index);
           swaps++;
        }
}
return swaps;
}

```
* first of all initialize a variable for swaps to Zero
* Define iterator 
__input : 1<=arr[i]<=Size__
**so index will be less than arr[i] by 1 in the correct order**
* the if condition search if the element is bigger than its index by 1 ;
* else we need to order it 
**Search for the right number to put it in its right place by Find()**
* and increase the number of swaps
