![image](https://github.com/user-attachments/assets/bfd4a60c-b5ea-4a0c-86a8-29defcb4efdd)


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
![image](https://github.com/user-attachments/assets/c5ed681a-db42-4267-8d26-2a0060c01db5)


![image](https://github.com/user-attachments/assets/ebcdfa0e-8305-4791-9b98-0af7903a7d82)

*Server*

![image](https://github.com/user-attachments/assets/8a036e6d-a7f1-4c6c-8ce3-195b1cae93ab)

![image](https://github.com/user-attachments/assets/cf78e082-8359-4c5a-ab00-f7040f3c162e)


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

![image](https://github.com/user-attachments/assets/c5cb21dc-add5-4dea-a9c0-504c624db6d7)

![image](https://github.com/user-attachments/assets/705480aa-3564-4f1d-8a9b-cd6cac61f061)

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
![image](https://github.com/user-attachments/assets/0ede1f88-8316-4ebc-b922-5c4dc5866040)


2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

*bash*

*sudo krb5_newrealm*

![image](https://github.com/user-attachments/assets/06c5306c-16c2-4b8a-bef7-d28c857180dc)


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

![image](https://github.com/user-attachments/assets/ee62cec0-c56b-4f7a-aa62-da98e4269744)


**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

*bash*

*sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser

![image](https://github.com/user-attachments/assets/7588d857-eb6f-4f7f-85b5-37fc4e2ba58c)

2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

*bash*

*sudo kadmin.local -q \"listprincs\"*

![image](https://github.com/user-attachments/assets/67dd6f8c-3928-44ec-89c6-843be73628e5)


**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

*bash*

*sudo nano /etc/krb5.conf*

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set on VM1.

![image](https://github.com/user-attachments/assets/671cb06a-f52f-44dc-a150-33d981fdede0)

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit <testuser@MYLAB.LOCAL>*

![image](https://github.com/user-attachments/assets/b191bb16-7203-4ed5-813b-96241ff7780a)


-   Enter the password you set for testuser.

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*klist*

![image](https://github.com/user-attachments/assets/af53c1d1-f400-4d46-89da-81109056a76f)

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.

CONCLUSION:

*Therefore, if there is a problem during the installation, then some of
the commands cannot be recognized by the terminal. Hence, the
installation should be successful so that the commands will work well
and can be recognize by the terminal. It is crucial if there is an error
in the beginning of the installation because it might lead to a domino
effect.*
