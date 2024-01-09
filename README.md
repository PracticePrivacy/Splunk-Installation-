# Splunk-Installation-
Instructions for installing Splunk on an Air Gapped System (No internet)

# ![Splunk](https://github.com/PracticePrivacy/Splunk-Installation-/assets/156040138/c1c24e3f-b01d-47af-9cbc-954af1de160f) 
## Installing a Splunk Server

**To set up Splunk on Linux, you can follow these steps:**

1. Download Splunk: Visit the Splunk website (www.splunk.com) and download the appropriate version of Splunk for your Linux distribution. You can choose between the free Splunk version or the enterprise versio n, depending on your needs.

2. Extract the Splunk package: After downloading the Splunk package, navigate to the directory where the package is saved and extract it using the following command:
   ```bash
   tar -xvf splunk_package_name.tgz
   ```

3. Install Splunk: Once the package is extracted, navigate into the extracted directory and run the installation script:
   ```bash
   cd splunk_package_name
   ./splunk install
   ```

4. Start Splunk: After the installation is complete, start Splunk using the following command:
   ```bash
   ./splunk start
   ```

5. Access Splunk Web: Open a web browser and access Splunk Web by entering the following URL: http://localhost:8000


6. Complete the setup wizard: Follow the instructions in the Splunk Web setup wizard to configure Splunk, create an admin account, and set up your data inputs.

These steps should help you get started with setting up Splunk on Linux. Make sure to refer to the Splunk documentation for any specific requirements or additional configuration steps related to your environment.

[def]: splunk-white-black-bg.png

## Installing a Splunk Universal Forwarder 
**To setup a Splunk Universal Forwarder, you can follow these steps:**


1. Download the Splunk Universal Forwarder: Visit the Splunk website (www.splunk.com) and download the appropriate version of the Splunk Universal Forwarder for your Linux distribution.

2. Extract the Splunk Universal Forwarder package: Navigate to the directory where the package is saved and extract it using the following command:

   ```bash
   tar -xvf splunkforwarder_package_name.tgz
   ```

3. Install the Splunk Universal Forwarder: Once the package is extracted, navigate into the extracted directory and run the installation script:

   ```bash
   cd splunkforwarder_package_name
   ./splunk install
   ```

4. Start the Splunk Universal Forwarder: After the installation is complete, start the Splunk Universal Forwarder using the following command:

   ```bash
   ./splunk start
   ```

5. Configure the Splunk Universal Forwarder: Use the splunk add forward-server command to specify the address and port of the Splunk indexer where you want to send the data. For example:

   ```bash
   ./splunk add forward-server <indexer_address>:<indexer_port>
   ```

6. Set up data inputs: Configure the Splunk Universal Forwarder to monitor and forward specific log files or directories using the inputs.conf file. Edit the inputs.conf file located in the **$SPLUNK_HOME/etc/system/local/** directory to define your inputs.

7. Restart the Splunk Universal Forwarder: After making any configuration changes, restart the Splunk Universal Forwarder for the changes to take effect:

   ```bash
   ./splunk restart
   ```

These steps should help you set up the Splunk Universal Forwarder on Linux. Make sure to refer to the Splunk documentation for any specific requirements or additional configuration steps related to your environment.

## Installing Splunk Heavy Forwarder

 **To set up the Splunk Heavy Forwarder on Linux, you can follow these steps:**


1. Download the Splunk Heavy Forwarder: Visit the Splunk website (www.splunk.com) and download the appropriate version of the Splunk Heavy Forwarder for your Linux distribution.

2. Extract the Splunk Heavy Forwarder package: Navigate to the directory where the package is saved and extract it using the following command:

   ```bash
   tar -xvf splunkheavyforwarder_package_name.tgz
   ```

3. Install the Splunk Heavy Forwarder: Once the package is extracted, navigate into the extracted directory and run the installation script:

   ```bash
   cd splunkheavyforwarder_package_name

   ./splunk install
   ```

Start the Splunk Heavy Forwarder: After the installation is complete, start the Splunk Heavy Forwarder using the following command:

```bash
./splunk start
```

Configure the Splunk Heavy Forwarder: Use the splunk set deploy-poll command to specify the address and port of the Splunk deployment server where you want to manage the Heavy Forwarder. For example:


```bash
./splunk set deploy-poll <deployment_server_address>:<deployment_server_port>
```

Set up data forwarding: Configure the Splunk Heavy Forwarder to forward data to the appropriate Splunk indexers or other forwarders. Edit the outputs.conf file located in the **$SPLUNK_HOME/etc/system/local/** directory to define your data forwarding settings.

Restart the Splunk Heavy Forwarder: After making any configuration changes, restart the Splunk Heavy Forwarder for the changes to take effect:

```bash
./splunk restart
```

These steps should help you set up the Splunk Heavy Forwarder on Linux. Make sure to refer to the Splunk documentation for any specific requirements or additional configuration steps related to your environment.

