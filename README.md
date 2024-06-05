<h1>Share Folders, Security Group and Map Drives </h1>
This guide provides an overview of how to create share folders, security groups and two ways of how to map a drive.<br />


<h3>Creating a shared folder</h3>
  - Go to server manager/file and storage services/shares/right click on  share/new share - SMB share quick.<br />
  - Choose the share name <br />
  For this guide's purpose I'm creating two, one named Personal and one named HR.
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/31db343e-180b-4dad-9c06-754564223c3e" height="60%" width="60%" alt="Server Manager" /></p>
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/f67f6fca-d862-4e62-81be-b20ead727b3f" height="60%" width="60%" alt="File Storage" /></p>
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/06902505-4000-4816-827d-ce58004c6f4e" height="60%" width="60%" alt="Share Name" /></p>
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/58ad9ed9-4f65-4f23-b301-b53d02de915a" height="60%" width="60%" alt="Share Name" /></p>
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/8df36857-d24c-43a0-9a86-4f81d549eabc" height="60%" width="60%" alt="Shares" /></p>

  <h3>Creating Security Groups</h3>
  For this guide, I'm creating two security groups, with same names of share folders.<br/>
  - Go to active directory users and computers/right click on users/new/group (HR).<br/>
  - Go to active directory users and computers/right click on users/new/group (Personal).<br/>
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/7e7b190a-554f-4227-8396-107ceae360bc" height="60%" width="60%" alt="SG" /></p>
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/6f5829f1-567b-4f08-81c6-5c353962952d" height="60%" width="60%" alt="SG" /></p>
   <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/7c829d1f-e6bf-414a-b9b3-3af2b56cd7cf" height="60%" width="60%" alt="SG" /></p>

  To add the members to the security groups go to active directory users and computers/HR security group/members/add (Add desired user, in this case, Patty).
  In this case Patty is added to both Personal and HR. To confirm the groups Patty is member of, go to active directory users and computers, look for the user Patty, right clik on it, go to member of and you can see the groups there.
  <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/544e54b5-b8bc-4367-87ab-bedd905c07b9" height="60%" width="60%" alt="Add member" /></p>
   <p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/10db1670-4f59-4406-9175-6e2bc539c784" height="60%" width="60%" alt="member" /></p>

  <h3>Permissioning the Folders</h3>
    - Go to this PC, Local Disk, Shares, choose the share folder you want to add permissions to, right click on it, click properties, go to security tab, choose advance.<br/>
    - Click on disable inheritance, convert inherited permissions into explicit permissions on this object.<br/>
    - Remove "users", and add helpdesk (in my labs an user who has access to server manager and specific features.) and Personal to it<br/>
    - Go to Personal shared folder, right click on it, click properties/sharing/choose read and write for Personal click share.
    - Repeat the same steps for HR folder.

    (add images)
    
    
  
  

  

  


  




 


  
