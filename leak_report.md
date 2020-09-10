# Leak report

## Memory Leaks Beginning Ideas


### Strip

The memory in this function comes from the array result, this one cannot just be closed since what is causing this leak is also being returned
so if `free()` is used before the return statement its going to fundemently change the program. Though result can't be free I am inclined to belelieve
`str` can be here. Hopefully I am right

### Is_Cleaned 

This memory leak seems to be fairly simple it is from the variable cleaned. Luckily this variable is only used here so it can be freed here as well

### Main

`main()` might have a memory leak with the array of strings but I am not entirly sure

### End
 
So I was definitly wrong about my ideas to fix the leaks... besides for `is_cleaned()`. So initially I figured the leak would need to be closed
directly in `strip()` but that wasn't right since the item was being used outside of it and str just didn't need it. In `main()` I thought it 
would be need on the all of the Strings but from what I gathered it is not needed since the array is not being set up dynamically.
While `cleaned`  in `is_clean` is from result in `strip` which is. Freeing `cleaned` frees the allocated memory in `result` since its stuff is moved there  

