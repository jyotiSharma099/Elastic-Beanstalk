 - [What is Elastic Beanstalk](https://github.com/karanbawa48/Elastic-Beanstalk#what-is-elastic-beanstalk)
 - [Deploy a docker container by Elastic Beanstalk with CI/CD.](https://github.com/karanbawa48/Elastic-Beanstalk#deploy-a-docker-container-by-elastic-beanstalk-with-cicd)
 - [Create  AWS code pipeline](https://github.com/karanbawa48/Elastic-Beanstalk#step-2--create--aws-code-pipeline)
 - [Create a connection with Github](https://github.com/karanbawa48/Elastic-Beanstalk#create-a-connection-with-github-by-clicking-on-connect-with-github)
 -  [Blue Green Deployment](https://github.com/karanbawa48/Elastic-Beanstalk#blue-green-deployment)

# What is Elastic Beanstalk
Elastic Beanstalk is a service for deploying and scaling web applications and services. Upload your code and Elastic Beanstalk automatically handles the deployment—from capacity provisioning, load balancing, and auto scaling to application health monitoring.

## Deploy a Containerized Application by Elastic Beanstalk with CI/CD.
In this tutorial we will deploy a **Docker container** by **Elastic Beanstalk**. we will use **Github** as a source code repo and AWS pipeline for **CI/CD**. 
## **Prerequisite**

 - **GitHub** account.
 - sample app (we will deploy a simple static website by dockerfile)
 - AWS Account
 ### **Step 1 — Setup AWS Elastic Beanstalk**
- **First click on Create Application**. 
(you will see the following page and fill details according. we are using **test** as the application name. use tags. For **Platform** we are docker (as we are deploying a docker container). In **Platform branch**. you can either use *docker on EC2 *or *ECS*. In Application code, upload your code. here you can upload from local or you can use S3 as well.

**![](https://lh3.googleusercontent.com/kBbcqDYe3wKQ5erZn__t8qzkbBrGCyGzxMksDEbJbeRdeGkVUyLcAxl3XI3A0Jgcn9-lcQulIIewVP0KKy0g4H9E4KevYgroA8ptLItvp_uJ_rAxOsrtdXXxusqnbjSHokmbgqQuWKbsDQjQ3CTZBso3Sh-DMT66c8VnTNjniAy4rDFf_wNDz-Xo_g)**

 After Providing required details. click  Create Application.
(The Application will start deploying you can see the events what  Elastic Beanstalk is doing at the backend. )

**![](https://lh6.googleusercontent.com/CRYZH3G7n6qBYXakg4Sy17543-U6ZUajvzanVeMLsmxNO7-xMzOAoy2tvPx0ajEJHvvQMrEBVRLLVMwrDKJHfi0HwFOe7PtFsXZ0Q7AsSh4enovkBMdmWrUHuSUrT0KzWFJidhUrNZ-qwhHQTRBv9l10WcxgCKc3SFDefW-LiUhOW7zS42Xo4ZW57w)**

*note: It'll take some time*
- The Env will be created. If the status is Green. EB will give a URL, that will redirect you to your application. 

 **![](https://lh6.googleusercontent.com/dvPaC0t-d0Q5DaqOD6XinqPv6tEhmxU6F-KGF8JTPIbT9RWaq2yYIdCQLgkmQDPnTOy4RhjD4GJVkVvHEwnzRbWrRYBsJZktDYG6YRpZrS6zLB7y18tDSRFM74gogad-gexMzpHS6gCvQTa8ZVV_n8Tu6bN7O7Hw9hgQhhtT0MXj4wPbrinrO3bLjQ)**

 ### **Step 2 — Create  AWS code pipeline**
 - **First click on go to AWS Developer tools and select Code pipeline**.
- Now click on Create Pipeline.
- Provide pipeline's name.
- A role will be created on behalf of you for this pipeline	or you can give your own custom role as well.
- Click on **Next**.

 **![](https://lh3.googleusercontent.com/dufjJZR8EA0qzyrSpf_VfzKUvC2wWPY8pszBzZe1KTiLt5ERsqIoTUlf-_ScwGO48KPXwdMapx3WuujlhLDVgFINS8um_1N4yeS_lc6T0wi8LbL2xiY3LUqDsGllM8aHK1SeKS1zWmOSu6qS7qpGOOyc_Dek7ubx4ctDbxx6Jp78FvWb1NlN4yNAMQ)**	

 - **Now  Add source stage**.
- here you will chose from where you want to take you source code. We are using **GitHub Version2**


![](https://lh5.googleusercontent.com/LEdslmLiaT5KPMI6glbyvfyL8t_PxoUYyQd36uriCcLzvm77h8OSEKNfxj5u5zFTfssB8gk8mLZjcYeS_Mlt7yTufKhrX2UzXlXFtuVKmICrJ8u7xZ-yiqVegZUy5FmYPVYLul26yuC6YZzTUgsADS8VDwR9TbuMVAl8hTqnoRhGYQ96YHKpMRxJMw)**
## Create a connection with Github by clicking on **connect with Github**. 
- A pop window will open as shown in the image below. Enter any name for connection. click on *Connect to GitHub*
- Create a GitHub app 
(GitHub Apps create a link for your connection with GitHub.)
- Log in with your github account where you have your source code.
- In **Repository access** . 
(you can give access to all repository. But good practice is to give minimum access)
- Select you Repo from Only select repositories and Click on  **Save**.

**![](https://lh6.googleusercontent.com/W_-8GYXxnsJBTurR52WPYCmrWNJluaBO25h9BmAA3_B3iLUBo1qiETYXqbZXP08XJ60LPzXI_js8vusIrdw8GCTorgo35LNTKLYfZyI_-ni8wh0RnXElIp79PcHgJ7fuZ7gvLq3WjzW-TdHbTHpbj2vgBslH7y27i4CD3NG0m1JXdr_Qii2X2wrjbA)**
- Now your App will be created and Click on **connect**.
	   The pop up window will auto close and looks like :

**![](https://lh4.googleusercontent.com/kYaAM-dd6a02mjauHgQzLPBPjkSJ-62DFudrE4umOMUWH6WyAciJ116h6MfggQ777fXw8hTZB2kKGUY6XIzRXwgDtu34hpHFbCShWbeIl_p0zHkAg5W2chm9rTivD7lUUI84-P7ZBOTWoUW7igNQldw2woVsILzttIsgnTEEHLdmQTUg92S4zabP_A)**

 - Select the Repo and Branch.
- Click on **Next**.
- **Spike the build part**
-  **Add deploy stage**
	 
  **![](https://lh3.googleusercontent.com/IQcjBIB3X1hQDyWMQcfFJgJE73lUclFB5ECVrNZIkmyuE4V2p_tjsgtvvCrWdwdCxkZGqt05rvGYsTDV1C-Mi3vTDZSJeBfxh1dzJIgZ7Bd-9ZqEtp2PEPJCwXwjiACJmar8RkuRlHXTaz2jtdZPM9Q9YskAwIbKvPAHXV0_wu16pHWh9ysEpwO8Hg)**

 - Here select Elastic Beanstalk as Deployment provider.
 - select region, where your EB application is running.
- select **application** in **Application name**.	
-  select **Environment** in **Environment name**. and click on Next.
- Review your Pipeline. if all good, click on create pipeline.


 **![](https://lh6.googleusercontent.com/rmTFJHCfBABtyiRID-F2rWfwumwP2KiJtvCt8TmMduqM4OkSNm7vfEklyH0Wst4ZavQQOv7ZDtHDjFE81HQD49ERTfWzPvXdrjacu0t9SUQQx9zOnK27_BXhJQJoope-gNUQgM71JyXHZnLyWvGDgUQHg5bdwWL68bJC6dWOOIKKYIeu-r3IIqTZOA)**


 The pipeline will be created and will start deploying your application
	  
# Blue Green Deployment
## what is Blue Green deployment?
A blue/green deployment is a deployment strategy in which you create two separate, but identical environments. One environment (**blue**) is running the **current application** version and one environment (**green**) is running the **new application version**. Using a blue/green deployment strategy increases application availability and reduces deployment risk by simplifying the rollback process if a deployment fails. Once testing has been completed on the green environment, live application traffic is directed to the green environment and the blue environment is deprecated.

## Blue/Green deployments with Elastic Beanstalk

- Go to your running Environment of ElasticBeanstalk.
- Click on **clone environment** 

**![](https://lh6.googleusercontent.com/ewnwVJs77fLlSInhRu2NizxLWEfucaTtyzMkEDaBJsZ-br8Sov0fiD2D3Behjrx4xupY74Xl75WVTK1fPiEBTvvzenl2BGsIdyUB_oiHCJikuszpomFlN_zi_WWwNzn97R12ifQxr4zW4GvlMtGNlp8JoVyWLeWKcn3Wst9xq5sQKHKPXK6TVVEz-g)**


- You can Change the Name of your new env (cloned env).
- Click on **clone**.


**![](https://lh3.googleusercontent.com/mpBhhAQonLjcGdaqMx4DVfKtJUsQ4ERRw6luWx2SHLtD-bFr_ZvTnRggnKWmmmcyCmFORBMr4miAm2kVIjAAVnSEoqWEZRxlj351hYATkAZZqYUnB-dRIktE0Hmxo2GC_Z7_Dp7mq3bbnJYqrYQrcMccxL-e0qrfP22FOMrS-YLP5V_J_5BSFUi0kA)**

 **Imortant: Environment URL must be unique.**
 If you see the following message. change the URL.

 **![](https://lh4.googleusercontent.com/MCwLbHlHiJYxjWbO5IpWkbm81eyFb2qUYHpOwj6KLo-yGT5kUx1VZ3jgGEixHpLkl-4bCfzjzel89qXq1HYWXqfJkotmx-9B1HeDxTCl3Q-l8J6_wueRO6tRVJV6odEE_pBidIChDs2aw3K8RS64shZz_qbTyKKT7-HsUr1_3MwGUoFidSRLDk6v9g)**

 The env will start cloning. you can check the Events. after it all done.
 *(It'll take few minutes)*
 meanwhile, follow me on Github [karanbawa48](https://github.com/karanbawa48)

 **![](https://lh6.googleusercontent.com/UMtWBvTqwPK22dw-Ueljdk_EofXKfpqzPta6LCMVoqo5AvNa0jY2iyRupJHjnwtGpQCb-Y4bokwMZZa9oFhmBsb0spxGsDnpzoOJ5NNEd0NyYnK4tDpLGbGeuq2WWeQTaRMPFua61-SR94Qws-PvyZLzk-2tGcOuktY_SHFhvoEekY6RHFVE14KySA)**

- The Env will be cloned, You can observe that the Env URL is different from the existing one. 
- Now, upload your **latest code** by clicking on *upload and deploy*.


**![](https://lh5.googleusercontent.com/BZoM_RKb63W-OJQyNC7SRNAe6xPqKvlCzsYqaJSh_0RRkPA4Ydrqz74y5lfGPBDk6Xkf-8ThaSWoIB2POGwe5AUDa3P7RdCbPWnx3VoM6BR_bBihD7eQknblm78IwJZXDhM4MKd76lOr4dvYgYBx-ezwMTQsELKQ0zrKgQDdXQtQYmkGB46AUAhvIQ)**

- Click on **Deploy**.

**![](https://lh3.googleusercontent.com/VZUWPRAHDq_O42BdyJRYIcBtPoYvzxSdXdqEQkaDhqWTcx9Xl13VWMfRcKnEon4Dfc_iFJMQD2i2G5lvDkIpMvx8LGPUKGP7CYWSW0adKFGMW6ZL1LIJ1fL1ba7NxtQ00qEahwaSYRLmQ6bMTI5BkdFA_dwAlFnr2-sICGWHC3I81usmcfPBsxsZ6Q)**

The New Application will start deploying.  if you source code is working. The Application will deployed.

**![](https://lh6.googleusercontent.com/1a39vGbRy8jM1m5cTOsQS-L7cDbOpVRWBPqe4GMLXcGppnz4InyGZ-HxiOBRLbHVN1xfJo0-o4mU8vs0zhDmRTtAlaBFHvmh4McZfsEbEKAdmEcF4H7H-09rH5ZADMjPKNtTk2ihkmzrO40JpEjUW4TvV4OAX1rVQcH4urCmqHncm6G9TzXL9ktBag)**


If the health new env is ok, It mean you have successfully deployed you new version of application. 
Test the new version on the new environment. 


**![](https://lh6.googleusercontent.com/_tGIhCEQdLT_GHNnhZH0eOhiTf_MjudUuUYkx8a9OWPZtHgQq70fxmosNrBcMuqUyYQ9-qGg2H6zaN9VLs4JTCbnt0KUJCdQt2uCHOyT1MOObBSTYKyTReEmLiRTRG6L3ws1q1qHuoi1B0DyoOdquQaeUPib_SiPzzvEO-14J_FolcrXpXlgtVLw8A)**

Now, here comes the Blue/green deployments in the picture.
- On the environment overview page, choose  **Environment actions**, and then choose  **Swap environment URLs**.

**![](https://lh5.googleusercontent.com/R2VcddtCfG2E8mmF1O_q3X85MB4g0vmyEODTc1MGyPu-7xsm4QqdI2z3d4_mCc5XRMd4T3baa9eMJXJbIc8LjzEpSEUdr7toSsaCDYE7AH250cJFGvHmgpiZm7H9wTuquiqlf9cdvzO79xs7dbV-E_YvKNwgnnfzOC3JQpNqBWucUqvyzHSevrQCAQ)**

- Click on **swap**

**![](https://lh6.googleusercontent.com/i-PqJjyFZeED1pPcjJovCSc_VxWe6j4Gj-J5pFTSVvdx_faomvnsWnzkqZk2o3ZsxWCqg0hQZHki0s5PsweO7ltjO7ojNZ9jdqQZ7SOofHyGX2v59lnuS2ehQl3QFSTs3lOJUCnzknBlII-DXr5gYxbsJGbfeSAiKD1Qo9YtyY7ZCvqXGWrG76CeMw)**

Elastic Beanstalk swaps the CNAME records of the old and new environments, redirecting traffic from the old version to the new version.

After Elastic Beanstalk completes the swap operation, verify that the new environment responds when you try to connect to the old environment URL. However, do not terminate your old environment until the DNS changes are propagated and your old DNS records expire. DNS servers don't always clear old records from their cache based on the time to live (TTL) that you set on your DNS records.

## All done!!

*Note: Blue/green deployments require that your environment runs independently of your production database, if your application uses one. If your environment includes a database that Elastic Beanstalk created on your behalf, the database and connection of the environment isn't preserved unless you take specific actions. If you have a database that you want to retain, use one of the Elastic Beanstalk database lifecycle options. You can choose the Retain option to keep the database and environment operational after decoupling the database.*
