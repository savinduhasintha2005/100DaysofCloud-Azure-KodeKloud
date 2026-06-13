# ❤️ Day 10 - Attach Public IP to Azure Virtual Machine

---

### 💡Step-by-Step Guide

### 🧑‍💻 Step 1: Find the VM's Network Interface

1. Log in to the [Azure Portal](https://portal.azure.com) using the credentials provided.
2. In the top search bar, type **Virtual machines** and select it from the services list.
3. Click on your virtual machine: **datacenter-vm-pip**.
4. On the left-hand menu, under the **Settings** section, click on **Networking**.
5. Look at the top of the networking section to find the name of the **Network Interface** (it usually looks like `datacenter-vm-pip-nic` or similar). Click on that NIC name to open its properties.

### 🧑‍💻 Step 2: Configure the IP Settings on the NIC

1. Now that you are on the Network Interface page, look at the left-hand menu and click on **IP configurations** (under *Settings*).
2. In the main panel, you will see a list of IP configurations (usually named `ipconfig1`). **Click on the name of the IP configuration** to edit it.

### 🧑‍💻 Step 3: Associate the Public IP

1. Inside the IP configuration settings, look for the **Public IP address** section.
2. Change the setting from *Associate* `No` to **`Associate` -> `Yes**` (or check the box/radio button to enable it).
3. Under the **Public IP address** dropdown menu, select the existing public IP: **datacenter-pip**.
4. Click the **Save** button at the top or bottom of the blade to apply the changes.

> ⚠️ **Note:** Azure will take a minute or two to update the network interface and bind the public IP. Do not close the browser tab until you see a "Successfully saved IP configuration" notification.

---

## Verification

To ensure everything is properly assigned:

1. Go back to the **datacenter-vm-pip** Virtual Machine overview page.
2. Look at the **Essentials** section at the top right.
3. Verify that **Public IP address** now displays the IP mapping for `datacenter-pip`.


