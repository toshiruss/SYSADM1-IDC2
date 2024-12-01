![image](https://github.com/user-attachments/assets/bde9b939-afd0-482b-bd31-ef516f39d712)


# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![image](https://github.com/user-attachments/assets/cab03e2c-5615-48d3-97fa-7077575a5a59)

Complete this lab as follows:

1.  Use the service --status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  alsa-utils                             anacron

  apport                                 apparmor

  cron                                   bluetooth

  cups                                   console-setup.sh

  dbus                                   cryptdisks
  -----------------------------------------------------------------------

SS:

![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image3.png){width="7.027083333333334in"
height="4.946527777777778in"}

![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image4.png){width="7.027083333333334in"
height="5.022222222222222in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image5.png){width="4.359946412948381in"
height="1.1875in"}

3.  Check the status of the Bluetooth service. What is its status?

**Active**

SS:
![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image6.png){width="7.027083333333334in"
height="1.7201388888888889in"}

4.  Check the status of the cups services. Since when was it running?

**Since Sept 12 01:08:12**

SS:
![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image7.png){width="7.027083333333334in"
height="3.4298611111111112in"}

5.  Stop cups services.

![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image8.png){width="7.027083333333334in"
height="0.8097222222222222in"}

6.  Verify if the service was stopped.

![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image9.png){width="7.027083333333334in"
height="3.6590277777777778in"}

7.  Restart the cups services

![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image10.png){width="5.46951334208224in"
height="0.2396172353455818in"}

8.  Verify if the service was restarted.

![](vertopal_aa659dc81d1142608a5f86fe86f579e8/media/image11.png){width="7.027083333333334in"
height="3.6305555555555555in"}
