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
