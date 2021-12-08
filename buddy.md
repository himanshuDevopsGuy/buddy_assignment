# <u>**A.W.S**</u>
# <u>**Assignment_Buddy**</u>

## **Topics that we learn**

* What is public subnet
* What is private subnet
* Difference between public & private subnet
* What is route tabel 

## </u>**Things to understand in public subnet**</u>
* Subnet is made in VPC.
* VPC is attached with IGW.
* Route tabel is created for each subnet
* And IGW route is entered in route tabel to access internet for the instance that is created in that subnet

## <u>**TASK**</u>

* The subnet which has IGW internet gateway route in route tabel is called public subnet.
* To understand more about public subnet , private subnet & route tabel lets see two case. 

## <u>**CASE 1**</u>
 ~ Create a VPC\
 ~ Create a subnet in that VPC\
 ~ launch an intsance in this subnet.

![Screenshot from 2021-12-04 18-07-27](https://user-images.githubusercontent.com/93082056/144709832-8b54db99-f86f-4d4a-8790-661bc540f5b2.png)
![Screenshot from 2021-12-04 18-07-34](https://user-images.githubusercontent.com/93082056/144709833-98e1bacb-f9c4-45f2-93dd-2b3db275cc71.png)
![Screenshot from 2021-12-04 18-08-28](https://user-images.githubusercontent.com/93082056/144709834-92cd7670-5454-4c90-9087-e761b1b4c3bc.png)
![Screenshot from 2021-12-04 18-09-39](https://user-images.githubusercontent.com/93082056/144709839-26f160ac-52cb-4ddb-a97a-d457f317aaa1.png)

### As you can see when i am creating an instance in this subnet by default option for ip allocation is disable

## <u>**CASE 2**</u>
~ Create a VPC\
~ Create a IGW\
~ Create a Subnet\
~ create a route tabel\
~ Attach IGW to VPC\
~ ADD IGW route in that route tabel of subnet\
~ launch an instance in this subnet.


![Screenshot from 2021-12-04 18-19-04](https://user-images.githubusercontent.com/93082056/144710355-ecaceef8-626f-47d6-a199-88bd7a166509.png)
![Screenshot from 2021-12-04 18-20-00](https://user-images.githubusercontent.com/93082056/144710358-d5385ef9-bc2e-4ab9-b75d-a464f477b32c.png)
![Screenshot from 2021-12-04 18-20-32](https://user-images.githubusercontent.com/93082056/144710359-0a8eecc8-a52e-4732-a1ee-3ebbb2a4493d.png)
![Screenshot from 2021-12-04 18-20-54](https://user-images.githubusercontent.com/93082056/144710360-fd90317d-f2d2-4083-acbf-64568b42a319.png)
![Screenshot from 2021-12-04 18-21-36](https://user-images.githubusercontent.com/93082056/144710361-d160a987-40b3-4f21-8f3e-0532f14c5e00.png)
![Screenshot from 2021-12-04 18-22-10](https://user-images.githubusercontent.com/93082056/144710362-56f9ef16-4960-400f-a1d5-c94debae753f.png)
![Screenshot from 2021-12-04 18-22-24](https://user-images.githubusercontent.com/93082056/144710363-12c29d44-e87f-43d8-a8be-80e9c8b4b5c5.png)
![Screenshot from 2021-12-04 18-22-40](https://user-images.githubusercontent.com/93082056/144710364-b90290e7-9590-418d-9354-2a9912034164.png)
![Screenshot from 2021-12-04 18-32-58](https://user-images.githubusercontent.com/93082056/144710427-2bbab996-f5cf-4d1b-a891-eb247c1286d1.png)


### As you can see when i am creating an instance in this subnet by default option for ip allocation is enable

## <u>**Summary**</u>
* The Subnet which has internet gateway route enetered in its route tabel is called public subnet
* The subnet which doesnt have internet gateway route enetered in its route tabel is called private subnet
* Route Tabel is used to enter data of route for that subnet.
* If route is eneterd only the internet access is made.

## Routes cases to understand more about if we give igw and what if we dont
* Instance in public subnet \
```
Ping google.com -->Instance -->VPC with IGW -->Subnet public -->Checking for internet access in route table --> Available

```
![Screenshot from 2021-12-04 18-56-32](https://user-images.githubusercontent.com/93082056/144711370-50f4085c-8cc9-4b18-bd0a-ed13769569e4.png)
### We are able to get data from google.

* Instance in private subnet
```
Ping google.com -->Instance -->VPC with IGW -->Subnet public -->Checking for internet access in route table --> NotAvailable
```
![Screenshot from 2021-12-04 19-01-27](https://user-images.githubusercontent.com/93082056/144711400-5e37869c-26d3-45d7-a7f1-10651fc41c4c.png)
### We are not getting any respond.