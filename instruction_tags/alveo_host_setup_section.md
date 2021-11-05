## 1.  Prerequisites
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

### 1.2 Host Setup:
The Xilinx Runtime (XRT) host application is supported on **Ubuntu 16.04 /18.04** and **CentOS 7.x.**
With **sudo access**, use the following command to download and run the setup script:

---

+ Clone GitHub Repository for Xilinx Base Runtime

```bash
git clone https://github.com/Xilinx/Xilinx_Base_Runtime.git
cd Xilinx_Base_Runtime
```

---

+ Run the Host Setup Script

```bash
./host_setup.sh -v {XRT_VERSION} -p {TARGET_BOARD}
```
**Notes**:
+ Please wait for the installation to complete.  During this time you may need press [Y] to continue the host setup.
+ If you choose to flash the FPGA, you will need to cold reboot the local machine after the installation is completed to load the new image on the FPGA.
+ The script for host setup can be used to setup other versions XRT and shell. Please check https://github.com/Xilinx/Xilinx_Base_Runtime for more details.

---

+ Install Docker (if not installed yet)

```bash
Xilinx_Base_Runtime/utilities/docker_install.sh
```

---

+ Setup Environment Variables

```bash
source Xilinx_Base_Runtime/utilities/xilinx_docker_setup.sh
```

