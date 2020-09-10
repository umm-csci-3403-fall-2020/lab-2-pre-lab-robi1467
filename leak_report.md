#Leak report

##Memory Leaks
###Strip
	The memory in this function comes from the array result, this one cannot just be closed since what is causing this leak is also being returned so if `free()` is used before the return statement its going to fundemently change the program. Though result can\'t be free I am inclined to belelieve str can be here. Hopefully I am right
###is cleaned 
	This memory leak seems to be fairly simple it is from the variable cleaned. Luckily this variable is only used here so it can be freed here as well.



