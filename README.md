<h1>🗂️ Shared Folders, Security Groups, and Drive Mapping</h1>

<p>
This guide demonstrates how to create <b>shared folders</b>, configure <b>security groups</b>, set permissions, and map drives in a <b>Windows Server</b> environment.  
The goal is to showcase hands-on skills in <b>server administration</b>, <b>active directory management</b>, and <b>network resource configuration</b>.
</p>

<hr/>

<h2>⚙️ Platforms and Technologies</h2>
<ul>
  <li>Windows Server 2016</li>
  <li>Server Manager & Active Directory Users and Computers (ADUC)</li>
</ul>

<h2>🛠️ Required Components</h2>
<ul>
  <li>Windows Server with administrative access</li>
  <li>Users to assign to security groups</li>
  <li>Shared folders on the server</li>
</ul>

<hr/>

<h2>📌 Step 1: Create Shared Folders</h2>
<ul>
  <li>Open <b>Server Manager → File and Storage Services → Shares</b>.</li>
  <li>Right-click <b>Shares → New Share → SMB Share – Quick</b>.</li>
  <li>Name the share (for this example: <b>Personal</b> and <b>HR</b>).</li>
</ul>
<p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/31db343e-180b-4dad-9c06-754564223c3e" height="60%" width="60%" alt="Server Manager"/>
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/f67f6fca-d862-4e62-81be-b20ead727b3f" height="60%" width="60%" alt="File Storage"/>
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/06902505-4000-4816-827d-ce58004c6f4e" height="60%" width="60%" alt="Share Name"/>
</p>

<hr/>

<h2>📌 Step 2: Create Security Groups</h2>
<ul>
  <li>Open <b>Active Directory Users and Computers → Users → New → Group</b>.</li>
  <li>Create groups matching your shares: <b>Personal</b> and <b>HR</b>.</li>
  <li>Add members to the groups (e.g., user <b>Patty</b> belongs to both groups).</li>
</ul>
To add members to the groups:
<ul>
  <li>Go to the security group (e.g., <b>HR</b>) → <b>Members → Add</b>.</li>
  <li>Select the user to add (e.g., <b>Patty</b>).</li>
  <li>To verify, find the user in ADUC (e.g., <b>Patty</b>) → right-click → <b>Properties → Member Of</b> tab. You can see all the groups the user belongs to.</li>
</ul>
<p align="center">
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/7e7b190a-554f-4227-8396-107ceae360bc" height="60%" width="60%" alt="Security Group HR"/>
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/6f5829f1-567b-4f08-81c6-5c353962952d" height="60%" width="60%" alt="Security Group Personal"/>
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/7c829d1f-e6bf-414a-b9b3-3af2b56cd7cf" height="60%" width="60%" alt="Groups Overview"/>
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/544e54b5-b8bc-4367-87ab-bedd905c07b9" height="60%" width="60%" alt="Add Member"/>
  <img src="https://github.com/roberta-bueno/sharesecuritymap/assets/135675237/10db1670-4f59-4406-9175-6e2bc539c784" height="60%" width="60%" alt="Member Confirmation"/>
</p>

<hr/>

<h2>📌 Step 3: Configure Folder Permissions</h2>
<ul>
  <li>Right-click the shared folder → <b>Properties → Security → Advanced</b>.</li>
  <li>Disable inheritance and convert inherited permissions to explicit permissions.</li>
  <li>Remove default <code>Users</code> group and add <code>Helpdesk</code> plus the corresponding security group.</li>
  <li>Go to <b>Sharing → Share → Read/Write</b> for the assigned group.</li>
  <li>Repeat for all shared folders.</li>
</ul>

<hr/>
