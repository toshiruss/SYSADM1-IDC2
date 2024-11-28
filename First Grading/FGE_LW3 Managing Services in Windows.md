+----------------------------------+-----------------------------+----+
| ![](vertopal_                    |                             |    |
| 3979900a992f4035abb3509489ce2052 |                             |    |
| /media/image1.png){width="2.4in" |                             |    |
| height="0.5881944444444445in"}   |                             |    |
|                                  |                             |    |
| SCHOOL OF INFORMATION AND        |                             |    |
| TECHNOLOGY                       |                             |    |
+----------------------------------+-----------------------------+----+
| NAME: VICENTE, RUSSEL C.         | DATE PERFORMED: 29 AUGUST   |    |
|                                  | 2024                        |    |
+----------------------------------+-----------------------------+----+
| Section: IDC2                    | DATE SUBMITTED: 29 AUGUST   |    |
|                                  | 2024                        |    |
+----------------------------------+-----------------------------+----+

# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

+------+-------------------+------------------------------------------+
| **   | **Name of         | **Screenshot**                           |
| Stat | Service**         |                                          |
| us** |                   |                                          |
+======+===================+==========================================+
| S    | OPTIMIZE DRIVES   | ![](vertopal                             |
| tart |                   | _3979900a992f4035abb3509489ce2052/media/ |
|      |                   | image2.png){width="3.0930227471566054in" |
|      |                   | height="1.76956583552056in"}             |
+------+-------------------+------------------------------------------+
| Stop | System Event      | ![](vertopal                             |
|      | Notification      | _3979900a992f4035abb3509489ce2052/media/ |
|      | Service           | image3.png){width="3.7135323709536308in" |
|      |                   | height="2.28963145231846in"}             |
|      |                   |                                          |
|      |                   | ![](vertopal                             |
|      |                   | _3979900a992f4035abb3509489ce2052/media/ |
|      |                   | image4.png){width="3.7858595800524935in" |
|      |                   | height="0.5019455380577428in"}           |
+------+-------------------+------------------------------------------+
| Res  | Shell Hardware    | ![](vertopa                              |
| tart | Detection         | l_3979900a992f4035abb3509489ce2052/media |
|      |                   | /image5.png){width="3.800057961504812in" |
|      |                   | height="2.0926192038495186in"}           |
+------+-------------------+------------------------------------------+
| P    | Workstation       | ![](vertopa                              |
| ause |                   | l_3979900a992f4035abb3509489ce2052/media |
|      |                   | /image6.png){width="3.488475503062117in" |
|      |                   | height="2.415628827646544in"}            |
|      |                   |                                          |
|      |                   | ![](vertopal                             |
|      |                   | _3979900a992f4035abb3509489ce2052/media/ |
|      |                   | image7.png){width="3.5749015748031496in" |
|      |                   | height="0.71498031496063in"}             |
+------+-------------------+------------------------------------------+

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
>
> **Network Location Awareness**: **Windows Event Collector
> Properties:**
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image8.png){width="3.1023906386701663in"
> height="3.4814720034995625in"}
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image9.png){width="2.94248031496063in"
> height="3.397428915135608in"}
>
> **Workstation: Fax:**
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image10.png){width="3.035900043744532in"
> height="3.4522954943132107in"}
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image11.png){width="3.0501476377952756in"
> height="3.5199945319335084in"}
>
> **Telephony:**
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image12.png){width="3.5226301399825024in"
> height="4.059830489938758in"}

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

-   In general tab, you can see the service name, display name,
    description, path and you can also modify its startup type depending
    on what you want to do (Automatic, Manual, Disabled)

> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image13.png){width="2.620287620297463in"
> height="2.9946150481189853in"}

-   In the Log On tab, we can see there the account, password and local
    system account.

> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image14.png){width="2.9213517060367455in"
> height="3.326291557305337in"}

-   In recovery tab, we can see the options if ever the service will
    fail. It displays first failure, second, failure, subsequent
    failures that has different functions that we can modify like take
    no action, restart the service, run a program, and restart the
    computer. And also the restart service after, that we can modify if
    how many minutes it should be.

> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image15.png){width="2.9217377515310585in"
> height="3.3880500874890638in"}

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image16.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

7.  Save the batch file in Z:\\lastname_timer.bat

> I did partitioning first to save my batch file in Z: drive.
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image17.png){width="4.045378390201225in"
> height="2.9927548118985126in"}
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image18.png){width="4.018511592300962in"
> height="1.9629899387576553in"}

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath=
> &quot;path_to_your_batch_file.bat&quot; start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image19.png){width="7.027083333333334in"
> height="1.0895833333333333in"}

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image20.png){width="7.027083333333334in"
> height="2.0520833333333335in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image21.png){width="5.926909448818898in"
> height="2.345883639545057in"}
>
> ![](vertopal_3979900a992f4035abb3509489ce2052/media/image22.png){width="5.886237970253719in"
> height="3.323380358705162in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **/50**                                            
  ---------------------------------------------------------------------------------------
