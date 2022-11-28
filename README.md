# Part 3: Red Hat Satellite 6.12 - Preparing the Satellite Environment

[Tutorial Menu](https://github.com/pslucas0212/RedHat-Satellite-6.12-VM-Provisioning-to-vSphere-Tutorial)

In Part 3 of the tutorial we will prepare the Satellite environment.  Note: We have Simple Content Access enabled on our customer portal and with any manifests that we create.  For more information regarding Simple Content Access, please refer to the Simple Content Access article link in the reference section below.  

### Create a Manifest for Satellite. 
To enable content on Satellite, you must first create a manifest file containing any Red Hat software subscriptions for that content and import the manifest into Satellite.  

Go to [Red Hat Customer Portal](https://access.redhat.com/) and login with your Red Hat customer account user id and password.  

Click the person icon in the upper right corner of the Red Hat customer portal page.  

![Red Hat Customer portal page](images/sat03.png)  

On the **Log in to your Red Hat account** page, fill in your Red Hat login or email and click the Red Next button.

![Red Hat Customer portal login button](images/sat04.png)  

Enter your password in the Password field and click the red Login button.  

On your Red Hat portal customer page, click the Subscriptions tab in the upper left side of the screen.  

![Red Hat Customer portal Subscriptions tab](images/sat05.png)  

You are now on the Overview tab of the Subscriptions section of the Red Hat Customer Portal.  Click the Subscription Allocations tab found near the top middle portion of the Red Hat Customer Portal.  

![Click Subscription Allocation tab](images/sat06.png)  

Click the blue Create New subscription allocation button.  

![Click the blue Create New Subscription allocation button](images/sat07.png)  

On the Create a New Subscription allocation page give the manifest a name and chose the version of Satellite that will use the manifest.  In our example we are creating manifest for the Moline Operations team and adding the manifest to our Satellite 6.12 environment.  Click the blue Create button to continue.

![Click the Create button](images/sat08.png)  

On the Subscription Allocations >> Moline-Operations page make sure that Simple content access is enabled and click on the Subscriptions tab.  

![Click on the subscriptions tab](images/sat09.png)  

On the Subscriptions tab click the blue Add Subscriptions button.  

![Click on the Add Subscriptions button](images/sat10.png)  

On the Add Subscriptions to Moline-Operations page you will see the subscriptions available to add to the manifest.  Since we have Simple Content Access enabled we only need to add one subscription per Red Hat product to the manifest.  For this example we are adding one subscription for RHEL Premium with Smart Management. 

![Add subscription ](images/sat11.png)  

If needed scroll down and click the submit button. 

![Click submit button](images/sat12.png)  

Back on the Subscription Allocations >> Moline-Operations page, click the Export Manifest button to download the manifest file that you just created.  We will import this file into Satellite.

![Click Export Manifest](images/sat13.png) 

We can now logout of the Red Hat customer portal.  

### Importing the Manifest in Satellite

Login to the Satellite console by entering [http://sat01.example.com](http://sat01.example.com) for the Satellite url.  Satellite will redirect the browser to Satellite's secure login page.  If this is the first time you have accessed your Red Hat Satellite console, you will need to accept Satellite's certificate for your browser.  

Enter the user id and password and click the Login button.  

![Click Login button](/images/sat14.png)  

You are now at the Satellite home screen.  

![Satellite Home Srceen](/images/sat15.png)  

We will now import the manifest into Satellite for the Operations Department organization.  

On the side menu click Content -> Subscriptions.  

![Content -> Subscriptions](/images/sat16.png)   

Click on the blue Import a Manifest button.  

![Import Manifest](/images/sat17.png)   

In the Manage Manifest dialog box, we will leave the default settings.  Click the Browse... button. A navigation dialog box will popup.  Navigate to the location of the manifest file you downloaded and click the Open button.  

![Chose Manifest](/images/sat18.png)  

The manifest will automatically be imported into Satellite and you will next see the Subscriptions page.

![Subscriptions Page](/images/sat19.png)

We have now completed preparing the Satellite environment.



## References  
[Installing Satellite Server from a Connected Network](https://access.redhat.com/documentation/en-us/red_hat_satellite/6.12/html/installing_satellite_server_in_a_connected_network_environment/index)
[Simple Content Access](https://access.redhat.com/articles/simple-content-access)  
[Provisioning VMWare using userdata via Satellite 6.3-6.6](https://access.redhat.com/blogs/1169563/posts/3640721)  
[Understanding Red Hat Content Delivery Network Repositories and their usage with Satellite 6](https://access.redhat.com/articles/1586183)

