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

## Implementation - Backend Key-Value Storage Servers
My individual work focused on the backend (key-storage servers, including working with Gaoxiang on the Load Balancing (master backend servers) and individually developing the storage servers. 

These are some of the features implemented on the backend:
- Sequential Consistency among Replicas
- Leader Election among Replicas
- Checkpointing and Logging and Recovery from Failure
- Key-value Store for both Texts and Binaries
- Locking and Synchronization of the Key-value Store
- Load Balancing between Master Backend Server and the Group of Replicas of Storage Servers

The report below shows some of the implementation details:
https://github.com/jyl-jyl/penn-cloud-2022-Fall/blob/main/report_backend.pdf

Here is a video demoing features of the storage servers:
https://drive.google.com/file/d/1ryPkeIVJyIvWvyg3bYHlxHUyM81RCBCL/view?usp=share_link


