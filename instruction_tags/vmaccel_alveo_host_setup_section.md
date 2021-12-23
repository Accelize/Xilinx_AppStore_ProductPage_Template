# 1. Prerequisites
## 1.1 Obtain an Account Access Key:
An access key is required to authenticate a user and grant them access to the application based on their entitlements.
To obtain your account access key, follow these steps:
+ Login to the [Xilinx App Store Portal](https://appstore.xilinx.com/)
+ Click the \"Access Key\" link on the left side menu
+ Click the \"Create an Access Key\" button.
+ Download the resulting file “cred.json” to /tmp directory

**Note**:  The resulting access key will enable all entitlements within your account.  
If you have not yet obtained entitlements from the \"TRY OR BUY\" section above, you must do so before following these steps for generating your access key.'
![Obtain an Account Access Key](assets/common/get_access_key.png)

---

## 1.2 Setup VMAccel
+ Sign-up for [VMAccel](https://www.vmaccel.com/xilinxtrial)
+ On EC2 console launch an instance corresponding to the Deployment Options table
+ Copy (scp) your “cred.json” file to the home directory of the instance and SSH into the instance.

```bash
scp -i \"$VMACCEL_ACCESS_KEY_FILE\" cred.json ubuntu@$VMACCEL_PUBLIC_IPV4:/home/ubuntu/
ssh -i \"$VMACCEL_ACCESS_KEY_FILE\" ubuntu@$VMACCEL_PUBLIC_IPV4
```

---

## 1.3 Instance Setup
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
source Xilinx_Base_Runtime/utilities/xilinx_docker_setup.sh
```
