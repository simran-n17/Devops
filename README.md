# 🚀 DevOps 

## **Demonstrating the Usage of Subversion (SVN) and Mercurial (Hg) in Windows**

### **By:**
📌 **Simran Negi**  
📌 **500107302**  

---

# **📌 Part 1: Subversion (SVN) Usage**

## **📌 Introduction**
Apache Subversion (SVN) is a centralized version control system that helps developers track changes in source code and collaborate effectively. This document provides a step-by-step guide to installing, configuring, and using Subversion on a Windows system to manage code efficiently.

---

## **📖 Step-by-Step Guide for Windows Users**

### **🛠️ Step 1: Install Subversion**
Before using SVN, ensure it is installed on your system. Download and install the latest version from the official website:  
🔗 [Subversion Download](https://subversion.apache.org/download/)

To verify the installation, open **Command Prompt (cmd)** or **PowerShell** and run:
```sh
svn --version
```
If SVN is installed correctly, it will display the installed version.

### **🛠️ Step 2: Set Up a Local Repository**
To create a new SVN repository on your system, use the following command:
```sh
svnadmin create C:\svn_repository
```
🔍 **Explanation:** This command initializes a new SVN repository at the specified path (`C:\svn_repository`).

### **📂 Step 3: Check Out a Working Copy**
To start working on a project, check out a working copy from the repository:
```sh
svn checkout file:///C:/svn_repository my_project
```
🔍 **Explanation:** This command creates a working directory named `my_project` with a copy of the repository.

### **✍️ Step 4: Add New Files**
After creating new files or modifying existing ones, add them to version control:
```sh
svn add new_file.txt
```
🔍 **Explanation:** This stages `new_file.txt` for version control.

### **✅ Step 5: Commit Changes**
To commit your changes to the repository with a meaningful message:
```sh
svn commit -m "Added new_file.txt with initial content"
```
🔍 **Explanation:** This command permanently records your changes in the repository with a descriptive message.

### **📤 Step 6: Update Working Copy**
To ensure your local working copy is up-to-date with the latest changes from the repository:
```sh
svn update
```
🔍 **Explanation:** This fetches the latest changes from the repository and merges them into your working copy.

### **🔄 Step 7: View Repository History**
To check the commit history of the repository:
```sh
svn log
```
🔍 **Explanation:** This command displays the history of changes, including commit messages and authors.

### **🚀 Step 8: Revert Changes**
If you want to undo uncommitted changes, use:
```sh
svn revert new_file.txt
```
🔍 **Explanation:** This restores `new_file.txt` to its last committed state.

### **🔧 Step 9: Resolve Merge Conflicts**
When multiple users modify the same file, conflicts may occur. To resolve them:
```sh
svn resolve --accept mine-full conflicted_file.txt
```
🔍 **Explanation:** This retains your version of `conflicted_file.txt` while discarding conflicting changes.

---

## **❌ Common Errors & Troubleshooting**

### **🔑 Error: `E170001: Authentication failed`**
This occurs if your credentials are incorrect when accessing a remote repository.

### **🛠️ Possible Solutions:**
1️⃣ **Verify Credentials** 🔑  
Ensure you are using the correct username and password for the remote repository.

2️⃣ **Store Credentials Securely** 🔏  
To avoid repeated login prompts, store credentials using:
```sh
svn auth
```
3️⃣ **Check Network Connectivity** 🌐  
Ensure you have an active internet connection and the remote repository is accessible.

### **🔑 Error: `svn: E175002: Connection refused (HTTP/HTTPS issue)`**
This error occurs when there is a mismatch in the protocol used (HTTP vs. HTTPS) while accessing the repository.

### **🛠️ Possible Solutions:**
1️⃣ **Ensure URL Consistency** 🔗  
Check that you are using the correct URL format. If the repository is hosted on HTTPS, ensure you are not mistakenly using HTTP.

2️⃣ **Verify Network and Firewall Settings** 🌍  
Ensure that your system or firewall is not blocking the connection.

3️⃣ **Check Server Configuration** 🛠️  
If you are hosting the repository, verify that the SVN server is correctly configured to accept HTTP or HTTPS connections.

---

## **🎯 Conclusion**
By following this guide, Windows users can effectively utilize Subversion (SVN) for version control. This ensures better collaboration, structured code management, and a streamlined workflow.

🔹 **Version control is essential for efficient software development—keep learning and innovating!** 🚀💻

---

# **📌 Part 2: Mercurial (Hg) Usage**

## **📌 Introduction**
Mercurial is a distributed version control system that allows developers to track changes in their code and collaborate with others. This section outlines the steps to clone a repository, make changes, and push those changes back to the remote repository using Mercurial.

---

## **📖 Steps to Clone a Repository and Push Changes**

### **🛠️ Step 1: Clone the Repository**
To clone a repository, use the following command:
```sh
hg clone <repository_url>
```
🔍 **Explanation:** This command creates a local copy of the repository located at the specified URL.

### **📂 Step 2: Change Directory**
Navigate into the cloned repository directory:
```sh
cd <repository_name>
```
🔍 **Explanation:** This command changes the working directory to the repository folder.

### **✍️ Step 3: Edit Files**
Make the necessary changes to the files using any text editor or IDE.

### **➕ Step 4: Add New Files**
If you have created new files or modified existing ones, add them to version control:
```sh
hg add
```

### **✅ Step 5: Commit Changes**
To commit changes with a meaningful message:
```sh
hg commit -m "My changes"
```

### **📤 Step 6: Push Changes**
To push your committed changes to the remote repository:
```sh
hg push
```

---

## **❌ Common Errors & Fixes**

### **🔑 Error: `abort: authorization failed`**
Occurs if Mercurial is unable to authenticate your credentials.

### **🛠️ Possible Solutions:**
1️⃣ **Check Access Permissions** 🔏 Ensure you have write access.

2️⃣ **Verify Credentials** 🔑 Ensure you are using the correct username and password.

---

## **🎯 Conclusion**
By following these steps, you can efficiently use both Subversion and Mercurial for version control, allowing seamless collaboration and project management. Happy coding! 🚀💻

