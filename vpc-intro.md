# VPC for Beginners :smiley:

VPC is like your own data center in cloud where you can create your own resource and secure it from the outer world.:thinking:

so Let me put this in a better way imagine you start your own company and now you have a website which you want to run you created your website with all the products you want to sell. So you will now host your website so you buy a server for those who don't know about the server. It is like a computer only but it is more like a cpu only. So you host your website on this server and now it is up and running. After a month traffic increase on your website since you sell very good handmade crockery now your website needs to be scaled since the request are increasing and you want to fullfill all the request so you buy another server and spin it up.So now the traffic basicaaly the requests by your customer is divided in both the servers and everything is going great. But soon after a month the traffic decreases since the festival season is over like "DIWALI" it is an indian festival where people buy so many new products.Since traffic is less now so your website can work on single server since you are paying for the electricity and cooling of these servers.So you shut down your server. These same stuff like buying a server hosting a website can be done on cloud basically on the server within minutes and you save a lot a money isn't that amaizing.But there is a catch since you are hosting your own server it is easy to secure it since you can take care of your stuff but what happens in cloud or on internet when you buy a server your resources are open and anyone can access it if they have the password or key. So in that case you can use VPC it stands for Virtual Private Cloud where you can have a room like a server room or a datacenter in the cloud where you can control everything isn't that cool enough.




## VPC Deep Dive 

it enables you to launch your **AWS** resources in a virtual network that you have defined.It resembles like you are operating in your own data center.VPC spans to all the availabity zones in the region.

* Amazon VPC acts as a networking layer for your EC2.

### Imortant Contents:

1.VPCs and Subnets
While creating a VPC you will specify the ip adress range. you will create various subnets,security groups and route table for VPC.
Subnet is nothing but just the ip-adress range you can launch your aws resource in a particular subnet.The specified ip adress range for the subnet should be subset for the VPC CIDR block.Each subnet is created in one zone means your subnet cannot spans among multiple a-z zones.
There are 2 types of subnets.

  * **Private Subnet** : subnet will have some resources associated it with so for the resources which are inside the private subnet
                         are not accessible to the internet.If the subnet traffic is routed to an Internet gateway than that subnet is a
                         public subnet.
                         
  * **Public Subnet**  : The resources which are in public subnet can access the resources over to the internet.
                         If a subnet traffic is not routed to an internet gateway than that subnet is a private subnet.
                         
**Example**: For example, if you create a VPC with CIDR block 10.0.0.0/24, it supports 256 IP addresses. You can break this CIDR block into two subnets, each supporting 128 IP addresses. One subnet uses CIDR block 10.0.0.0/25 (for addresses 10.0.0.0 - 10.0.0.127) and the other uses CIDR block 10.0.0.128/25 (for addresses 10.0.0.128 - 10.0.0.255).
    
