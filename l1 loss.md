looking for least absolute deviations!! between predicted and original
minimizing the sum of the absolute differences between the true and predicted value![[Screenshot 2023-11-16 at 5.36.09 PM.png]]

how do you sample from 1 to n 

l2 is minimizing the error between the squared differences


both dont maintain the sign!![[Screenshot 2023-11-16 at 5.36.47 PM.png]]

l2 is worse when u have outliers because those will be heavily amplified: itll look like you have a lot more error than u actually do
	after training a lot with l1 loss, to try to make a general network, can u then train on l2 loss to capture the nuance of outliers?