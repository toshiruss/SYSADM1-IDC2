+----------------------------------+----------------------------+-----+
| ![](vertopal_                    |                            |     |
| 041ff26734c04cad99f069a7b94749d5 |                            |     |
| /media/image1.png){width="2.4in" |                            |     |
| height="0.5881944444444445in"}   |                            |     |
|                                  |                            |     |
| SCHOOL OF INFORMATION AND        |                            |     |
| TECHNOLOGY                       |                            |     |
+----------------------------------+----------------------------+-----+
| NAME: VICENTE, RUSSEL C.         | DATE PERFORMED: 14 NOV     | /   |
|                                  | 2024                       | 50  |
+----------------------------------+----------------------------+-----+
| Section:IDC2                     | DATE SUBMITTED: 14 NOV     |     |
|                                  | 2024                       |     |
+----------------------------------+----------------------------+-----+

# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

**Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos
manages secure logins through ticket-based access.

**Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

**Step 1: Initial Setup and Package Installation**

1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

*bash*

*sudo apt update && sudo apt upgrade --y*

*Client:*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image2.png){width="5.688293963254593in"
height="2.4795122484689416in"}

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image3.png){width="5.6570395888014in"
height="4.781917104111986in"}

*Server*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image4.png){width="7.027083333333334in"
height="3.595833333333333in"}

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image5.png){width="7.027083333333334in"
height="4.6375in"}

*Based upon my observation, the two machines (client and server) have
different errors wherein the Client some of the packages didn't install
well while the Server most of the packages was installed but there is
still error but I don't understand what it is.*

2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

*bash*

*sudo apt install krb5-kdc krb5-admin-server --y*

3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

*bash*

*sudo apt install krb5-user --y*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image6.png){width="7.027083333333334in"
height="4.032638888888889in"}

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image7.png){width="7.027083333333334in"
height="4.221527777777778in"}

-   During installation, when prompted, enter the Kerberos realm you
    plan to set up, e.g., MYLAB.LOCAL.

**Step 2: Configure the Kerberos Server (VM1)**

1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

*bash*

*sudo nano /etc/krb5.conf*

-   Set the realm as MYLAB.LOCAL. You should also specify the KDC and
    admin server as VM1's hostname or IP address:

ini

\[libdefaults\]

default_realm = MYLAB.LOCAL

\[realms\]

MYLAB.LOCAL = {

kdc = \<VM1_IP_or_hostname\>

admin_server = \<VM1_IP_or_hostname\>

}

-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

> ![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image8.png){width="4.943522528433946in"
> height="4.4483956692913385in"}

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

*bash*

*sudo krb5_newrealm*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image9.png){width="4.615227471566055in"
height="0.8751224846894138in"}

*Since there are still errors, I can't execute some commands because I
think there are problems upon my installation process. It might be the
other packages were not installed well.*

-   You will be prompted to set a password for the Kerberos database.

3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:

*bash*

*sudo systemctl start krb5-kdc*

*sudo systemctl start krb5-admin-server*

*sudo systemctl enable krb5-kdc*

*sudo systemctl enable krb5-admin-server*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image10.png){width="6.084181977252843in"
height="3.125436351706037in"}

**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

*bash*

*sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image11.png){width="7.027083333333334in"
height="0.4201388888888889in"}

2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

*bash*

*sudo kadmin.local -q \"listprincs\"*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image12.png){width="5.354913604549432in"
height="0.44797900262467194in"}

**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

*bash*

*sudo nano /etc/krb5.conf*

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set on VM1.

> ![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image13.png){width="4.469373359580053in"
> height="0.21878062117235345in"}
>
> ![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image14.png){width="4.557608267716535in"
> height="2.103511592300962in"}

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit <testuser@MYLAB.LOCAL>*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image15.png){width="6.094600831146106in"
height="1.5939720034995626in"}

-   Enter the password you set for testuser.

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*klist*

![](vertopal_041ff26734c04cad99f069a7b94749d5/media/image16.png){width="6.063346456692913in"
height="1.531463254593176in"}

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.

CONCLUSION:

*Therefore, if there is a problem during the installation, then some of
the commands cannot be recognized by the terminal. Hence, the
installation should be successful so that the commands will work well
and can be recognize by the terminal. It is crucial if there is an error
in the beginning of the installation because it might lead to a domino
effect.*
