## 1. Prerequisites
### 1.1 Obtain an Account Access Key:
An access key is required to authenticate a user and grant them access to the application based on their entitlements.
To obtain your account access key, follow these steps:
+ Login to the [Xilinx App Store Portal](https://appstore.xilinx.com/)
+ Click the button labeled \"Manage Account\" to view entitlements.
+ Click the \"Access Key\" link on the left side menu
+ Click the \"Create an Access Key\" button.
+ Download the resulting file \"cred.json\" to the location ABC

**Note**:  The resulting access key will enable all entitlements within your account.  
If you have not yet obtained entitlements from the \"TRY OR BUY\" section above, you must do so before following these steps for generating your access key.'
![Obtain an Account Access Key](assets/common/get_access_key.png)

---

### 1.2 Setup AWS
+ Sign-up for Amazon Web Services (AWS)
+ On EC2 console launch an F1 instance of your choice (f1.2xlarge recommended) with FPGA Developer AMI corresponding to the Deployment Options table
+ Copy (scp) your “cred.json” file to the home directory of the instance and SSH into the instance.

```bash
scp -i \"$AWS_ACCESS_KEY_FILE\" cred.json centos@$AWS_PUBLIC_IPV4:/home/centos/
ssh -i \"$AWS_ACCESS_KEY_FILE\" centos@$AWS_PUBLIC_IPV4
```

---

### 1.3 Instance Setup
The application is containerized and thus needs Docker to be installed.
Use the following command to install and configure Docker:

---

+ Install and Configure Docker

```bash
git clone https://github.com/Xilinx/Xilinx_Base_Runtime.git
sudo Xilinx_Base_Runtime/utilities/docker_install.sh
```

---

+ Setup Environment Variables

```bash
source Xilinx_Base_Runtime/utilities/xilinx_aws_docker_setup.sh
```
