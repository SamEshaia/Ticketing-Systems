# Ticketing-Systems
 Welcome to this comprehensive guide on the installation, setup, and utilization of ticketing systems, with a focus on osTicket. Whether you're new to ticketing systems or seeking to enhance your knowledge, this guide will provide you with valuable insights

<h1>osTicket Systems Guide</h1>
<h3>Overview</h3>
<p>This project aims to implement and explore the functionalities of osTicket, an open source ticketing system. Our primary objective is to install osTicket and gain a thorough understanding of its fundamental features and capabilities.

Throughout the project, we will delve into the various components of osTicket, assessing its basic functions and how they can be utilized effectively. This will involve exploring key functionalities such as ticket creation, management, and resolution processes. By closely observing osTicket in action, we aim to comprehend how it streamlines the ticketing process and enhances overall efficiency in handling customer support or service requests.

To accomplish our goals, we will begin by installing osTicket and configuring it to align with our specific requirements. This will involve setting up the necessary infrastructure, configuring user roles and permissions, and customizing the system to cater to our organizational needs.

Once the installation is complete, we will dive into the ticketing system's core functionalities. We will explore how to create and assign tickets, track their progress, and communicate with customers throughout the support cycle. Additionally, we will examine features like ticket prioritization, escalation, and ticket resolution workflows, gaining insights into how these functionalities can be leveraged to streamline customer support operations.

Throughout the project, we will document our observations, noting any challenges, successes, or potential areas for improvement in utilizing osTicket. By the end of this project, we aim to have a comprehensive understanding of osTicket's basic functions and its potential to enhance our organization's ticketing and support processes.</p>

<h1>osTicket Installation Setup</h1>
<h3>Step 1: Establish Your Foundation</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/a6d1c644-cea3-4b61-a093-147a24c13437">
<p>Create a robust foundation for your project by setting up a Resource Group and deploying a Virtual Machine running Windows 10. Choose a suitable name for your Resource Group, such as "RG-LAB-03," and designate your Virtual Machine as "VM-osTicket."

When configuring the Virtual Machine, ensure it is equipped with 2-4 Virtual CPUs to ensure optimal performance. Remember to select the same location for both the Resource Group and the Virtual Machine to ensure seamless integration.

Crucially, don't forget to record the username and password assigned to your Virtual Machine. These credentials will grant you access and control over the system throughout the project.</p>

<h3>Step 2: Empower Your Virtual Machine with IIS</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/4203e4a6-6b33-4229-8e36-94597d850e23">
<p>Empower your Windows virtual machine by installing and enabling Internet Information Services (IIS) alongside CGI and Common HTTP Features. To accomplish this, navigate to the programs section in the control panel and select "Turn Windows features on or off."

Within the window that appears, expand the World Wide Web Services section by clicking the plus button. Next, expand the Application Development Features by clicking the plus button once more. Check the box for “CGI”, and then proceed to select all the "Common HTTP Features."

By enabling these essential components, you will unlock the full potential of your virtual machine, ensuring seamless integration and enhanced performance for your osTicket installation.</p>

<h3>Step 2a: Verify IIS Success</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/b492ff85-b9fe-4f4a-8d34-cfdfe5535dba">
<p>Confirm the success of your Internet Information Services (IIS) installation by entering "127.0.0.1" in your web browser. If the displayed webpage resembles the image above, congratulations! Your IIS setup is successful.

In the event that the page does not load correctly, you will need to revisit and repeat Step 2 to ensure proper configuration.</p>

<h3>Step 3: Set up Required Files and Programs</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/be571f5d-0750-4844-b65c-9e148bab6eab">
<p>To ensure a proper setup of osTicket, proceed with the installation or extraction of the following essential files:</p>
<ul>
 <li>PHPManagerForIIS_V1.5.0.msi</li>
 <li>rewrite_amd64_en-US.msi</li>
 <li>php-7.3.8-nts-Win32-VC15-x86.zip</li>
 <li>mysql-5.5.62-win32.msi</li>
</ul>
<p>Create a designated folder, such as "C:\PHP," and extract all the contents of php-7.3.8 into this folder.

During the installation of mysql-5.5.62-win32.msi, choose the "Typical" setup option. Ensure that the checkbox for launching the Configuration Wizard is selected. Proceed by selecting the "Typical Standard Configuration" and creating a password (remember to keep it secure).

By completing these steps, you will successfully install the necessary files and programs required for osTicket's proper functioning.</p>

<h3>Step 4: Register PHP with IIS</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/78ca33b3-a834-4cfc-b090-664aa58990e2">
<p>Launch Internet Information Services (IIS) as an administrator. Access the PHP Manager by clicking on it, then choose "Registering new PHP version." Click the "..." button and select "php-cgi" to complete the registration process.

By following these steps, you will successfully integrate and register PHP within IIS, ensuring seamless communication between osTicket and the web server.</p>

<h3>Step 5: Deploy osTicket v1.15.8</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/6324851b-1ae0-490f-8f08-658935d5bc62">
<p>Download osTicket v1.15.8 and extract the contents. Copy the "upload" folder and paste it into the C:\inetpub\wwwroot directory. Once inside the C:\inetpub\wwwroot folder, rename the "upload" folder to "osTicket."

By completing this step, you will successfully install osTicket v1.15.8 and configure it for deployment.</p>

<h3>Step 5a: Accessing osTicket</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/a23b2ceb-c066-4bc9-a656-3d4851792e21">
<p>After restarting IIS, you will find the dedicated osTicket section under the Default Web Site in IIS. This confirms the successful configuration of osTicket. To access osTicket, simply click on "Browse :80" within the osTicket section.

By following these steps, you can conveniently access and explore osTicket through the provided link, allowing you to begin utilizing its features for efficient ticket management and support.</p>

<h3>Step 6: Activate Essential Extensions</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/d9c33cb7-944e-4706-924f-6f8bfe01f376">
<p>Access IIS, go to sites, then Default, and select osTicket. Double-click on PHP Manager. Next, click on "Enable or disable an extension."

Enable the following vital extensions for optimal osTicket functionality:</p>
<ul>
 <li>php_imap.dll</li>
 <li>php_intl.dll</li>
 <li>php_opcache.dll</li>
</ul>
<p>Once you have enabled these extensions, refresh the osTicket site in your browser to witness the applied changes. You will now experience enhanced features and capabilities within osTicket, enabling seamless ticket management and support operations.</p>

<h3>Step 7: Configure ost-config.php and Set Permissions</h3>
<img width="700" height"400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/84256b90-6906-4c4d-866e-a0d998cd6793">
<p>Go to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename the file from "ost-sampleconfig.php" to "ost-config.php."

Next, access the properties of the newly renamed "ost-config.php" file. Navigate to the security tab and click on "Advanced." In the ensuing window, select "Disable inheritance" and then choose "Remove all inherited permissions from this object."

Click "Add" and another window will appear. Select "Select Principal" (underlined in blue). In the text box, type "Everyone" and click "Check Names." Once validated, click "OK."

Check the "Full control" box and click "OK." Apply the changes and confirm by clicking "OK."

By completing these steps, you have successfully configured the necessary file and set the appropriate permissions for "ost-config.php," ensuring proper functionality and security for osTicket.</p>

<h3>Step 8: Continue osTicket Setup Page</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/8c5b0523-e585-4509-b27a-abf9e02240dd">
<p>Proceed with filling out the osTicket setup page in your browser. Remember, the email addresses entered can be fictitious, but ensure you remember or note them down along with the chosen username and password.

Note that you can leave the MySQL Database field blank for now, as it will be addressed in the following steps.</p>

<h3>Step 9: Set up Database with HeidiSQL</h3>
<img width="1000" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/6b5ea2e5-fce4-40f5-a324-bb0e8f6328e4">
<p>Install HeidiSQL using the provided setup file (HeidiSQL_12.3.0.6589_Setup.exe). Once installed, the program will open automatically. Locate the "New" button at the bottom left of the program window and click on it. Enter the password you created earlier for MySQL, then click "Open."

To configure the osTicket database, right-click on the empty space below the menu options on the left side of the program. Hover over "Create New" and select "Database." Name the database as "osTicket" and click "OK."

Next, in the osTicket set up page in your browser, fill in the “MySQL Database:” textbox with “osTicket” then click “Install Now”.

By following these steps, you will successfully install HeidiSQL and establish the necessary database for osTicket, laying the foundation for effective data management within the application.</p>

<h3>Step 10: Verify osTicket Functionality</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/43c14932-e81b-4586-ba8a-8084ea7d4c0d">
<p>To ensure osTicket is functioning correctly, access the following URL: http://localhost/osTicket/scp/login.php. Enter the username and password you set up on the osTicket login page.

By visiting this URL and successfully logging in, you can confirm that osTicket is operational, allowing you to start utilizing its ticketing system and support features effectively.</p>

<h3>Step 11: Tidy Up</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/10cf1538-640b-4eb0-b8a1-15a134399bf3">
<p>Before delving into the ticket system, perform some cleanup tasks:

Delete the following directory: C:\inetpub\wwwroot\osTicket\setup.

Next, set the permission of the following file to "Read-only": C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>

<h1>osTicket Post Installation Setup</h1>
<p>In this section, we'll configure osTicket to get a better feel how different parts of the system are created. We'll set up roles, departments, teams, agents, and users to enhance collaboration and streamline support workflows. Service Level Agreements (SLAs) will be defined to ensure prompt and effective customer service. We'll also create helpful help topics to address common user inquiries.</p>

<h3>Step 12: Set up Roles</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/105867e9-6b9a-4b86-882c-0bc44c806ec6">
<p>After logging in successfully, you will receive a warm greeting, confirming the successful installation of osTicket. Congratulations!

To configure roles, proceed to the admin panel. Click on the "Agents" tab, then select the "Roles" menu option. Add a new role, such as "Supreme Admin," as an example.

Feel free to create additional roles according to your requirements, as the example provided is just a starting point.

By establishing roles, you can effectively manage user permissions and access levels within osTicket, ensuring efficient administration and delegation of tasks.</p>

<h3>Step 13: Establish Departments</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/d2f9a9c4-7621-44d3-8855-571c16cc6e90">
<p>In the Admin Panel, access the Agents tab and click on Departments. Proceed to click on "Add New Department." On the setup page, name the department as "System Administrators" and maintain the default settings.

Once you have named the department, click on "Create Dept" to finalize the setup.</p>

<h3>Step 14: Set up Teams</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/4e87a745-a5b7-425c-bb22-43ffcb6e8dce">
<p>Within the Admin Panel, select the Teams tab under the Agents section. Create a new team called "Level II Support." In the setup page for the new team, keep the Team tab at its default settings.
In the Members tab, add your own user account to the team.</p>

<h3>Step 15: Enable Ticket Creation for All Users</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/7d48f332-3f69-44a0-850e-7497fa2f513b">
<p>In the Admin Panel, access the User Settings and make sure the option to "Require registration and login to create tickets” is unchecked. Uncheck this box to allow anyone to create tickets without requiring registration or login.</p>

<h3>Step 16: Add Agents</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/993baae6-b4aa-42e9-92b5-8d0cd7ef7db3">
<p>In the Admin Panel Agents section, click on "Add New" to create new agent profiles. Assign names such as Jane Doe and John Doe, providing their respective email addresses, usernames, and passwords (which can be set to remain unchanged upon login).

Next, navigate to the Access tab and assign the department as "System Administrators" and the role as "Supreme Admin" for the agents. Ensure that all permissions are checked, and add them to the Level Support II Team.

Additionally, in the Access tab, add support give them supreme admin to the Extended Access.</p>

<h3>Set up Users (Customers)</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/843a4690-8a84-4bb7-984d-07f9e5a5be32">
<p>In the Agent Panel, select the Users tab. Click on "Add New User" to create new user profiles. Input desired names and email addresses. As an example, I used “Karen Karen” and “Ken Ken”.</p>

<h3>Step 18: Set up SLA (Service Level Agreement)</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/8130ab36-3a6d-4e71-9f3e-2d7c6254a06b">
<p>Return to the Admin Panel and access the manage tab. Click on SLA and select "Add New SLA Plan" to configure the following SLA plans:</p>
<ul>
 <li>Name: SEV-A (1 hour response time, available 24/7)</li>
 <li>Name: SEV-B (4 hours response time, available 24/7)</li>
 <li>Name: SEV-C (8 hours response time, available during business hours)</li>
</ul>
<p>Leave the rest of the options at the default configurations.

By defining SLA plans, you establish clear expectations for response times based on the severity level of tickets, ensuring prompt and efficient resolution of customer issues.</p>

<h3>Step 19: Set up Help Topics</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/1aa809b5-329f-4b3b-b395-5464442a096f">
<p>Within the Admin Panel, navigate to the Manage tab and select Help Topics. Click on "Add New Help Topic" to create the following topics:</p>
<ul>
 <li>Topic: Business Critical Outage</li>
 <li>Topic: Personal Computer Issues</li>
 <li>Topic: Equipment Request</li>
 <li>Topic: Password Reset</li>
</ul>
<p>You don't need to fill out any additional details and can leave the options as they are. Once you've entered the topic, click on "Add Topic" to save the settings.

Configuring help topics allows for streamlined categorization and efficient management of different types of support requests, ensuring that tickets are appropriately classified and addressed by the support team.</p>

<h1>Tickets and Ticket Lifecycle</h1>
<p>In this section, we practice creating, triaging, and solving tickets.</p>

<h3>Step 20: Creating Tickets</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/57cd4189-a286-45b7-ac1e-d8f32737613a">
<p>Go to http://localhost/osTicket and click the "Open a New Ticket" button. Fill out the Issue Summary for each ticket with the following topics:</p>
<ul>
 <li>Entire Mobile/Online Banking System is down</li>
 <li>Entire Accounting Dept Adobe Reader Not Working</li>
 <li>When are we getting a hardware Refresh</li>
</ul>
<p>In the large text box, provide detailed information regarding each topic. Refer to the provided image for examples.</p>

<h3>Step 21: Troubleshooting and Solving Tickets</h3>
<img width="700" height="400" alt="image" src="https://github.com/SamEshaia/Ticketing-Systems/assets/124312452/89c98e8c-e16f-400a-b84d-003ae7c55e2c">
<p>To begin, log in as Jane.Doe, one of the agents you created earlier in this guide.

As Jane, you will observe the tickets, set priority levels, assign them to different staff members and departments, and apply the appropriate SLA plan. Assign two of the tickets to Jane and one to John. Now, switch to John's account and resolve the ticket assigned to him.</p>

