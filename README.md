# Penn Cloud

Penn Cloud is the final project of CIS505 (University of Pennsylvania) in Fall 2022. The team members of Penn Cloud are: Yao Tong, Jingyi Li, Gaoxiang Luo. 

In this project, we built a platform, somewhat similar to Google Apps, with webmail service, analogous to Gmail, as well as a storage service, analogous to Google Drive.

The figure bellow illustrates the high-level structure of the systems:

Users can connect to a set of frontend servers with their
browsers and interact with the services using a simple web
interface. Each frontend server runs a small web server that
contains the logic for the different services; however, it does not
keep any local state. Instead, all state is stored in a set of backend
servers that provide a key-value store abstraction. That way, if one
of the frontend servers crashes, users can simply be redirected to a
different frontend server, and it is easy to launch additional frontend servers if the system becomes overloaded.
