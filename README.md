# Penn Cloud


<p align="center">
<img src="https://github.com/jyl-jyl/penn-cloud-2022-Fall/blob/main/images/penn-cloud.png" width="700"/>
</p>

Penn Cloud is the final project of CIS505 (University of Pennsylvania) in Fall 2022. The team members of Penn Cloud are: 
  - Yao Tong
  - Jingyi Li
  - Gaoxiang Luo. 

In this project, we built a platform, somewhat similar to Google Apps, with webmail service, analogous to Gmail, as well as a storage service, analogous to Google Drive.

The figure bellow illustrates the high-level structure of the systems (image is from project's handout):
<p align="center">
<img src="https://github.com/jyl-jyl/penn-cloud-2022-Fall/blob/main/images/structure.png" width="400"/>
</p>

Users can connect to a set of **_frontend servers_** with their
browsers and interact with the services using a simple web
interface. Each frontend server runs a small web server that
contains the logic for the different services; however, it does not
keep any local state. Instead, all state is stored in a set of **_backend
servers_** that provide a **_key-value store_** abstraction. That way, if one
of the frontend servers crashes, users can simply be redirected to a
different frontend server, and it is easy to launch additional frontend servers if the system becomes overloaded.

Below is our proposal:

