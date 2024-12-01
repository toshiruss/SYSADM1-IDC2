![image](https://github.com/user-attachments/assets/fa9ac964-5768-4a7d-887b-b0295a51fbd7)


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
![image](https://github.com/user-attachments/assets/04d6bfeb-92ca-40b8-b8f4-6f9f0b7ae0b4)![image](https://github.com/user-attachments/assets/41a0408c-c3e5-465e-9408-0c139d1baa2d)![image](https://github.com/user-attachments/assets/b0befa7c-e2e2-422c-9ceb-0866bc80831b)![image](https://github.com/user-attachments/assets/bcabebc3-67e8-4032-9600-f8cf5039643f)





4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
>
> **Network Location Awareness**: **Windows Event Collector
> Properties:**
>
![image](https://github.com/user-attachments/assets/725f2687-17b0-410f-9f3f-12b5bb5659ef)![image](https://github.com/user-attachments/assets/9fda7ccb-cb87-4918-9748-9afbe0e11e11)


>
> **Workstation: Fax:**
>
![image](https://github.com/user-attachments/assets/4e6e5513-719a-460c-a514-8f7790a9f6ea)

>
> **Telephony:**
>
![image](https://github.com/user-attachments/assets/8465dc80-4c69-4409-8933-0dad574e083e)



5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

-   In general tab, you can see the service name, display name,
    description, path and you can also modify its startup type depending
    on what you want to do (Automatic, Manual, Disabled)

![image](https://github.com/user-attachments/assets/e8fc7849-ea2d-48eb-9db0-d4fe593203cb)


-   In the Log On tab, we can see there the account, password and local
    system account.

![image](https://github.com/user-attachments/assets/f042ee29-45f5-4519-bf6d-9c1abba4c80f)


-   In recovery tab, we can see the options if ever the service will
    fail. It displays first failure, second, failure, subsequent
    failures that has different functions that we can modify like take
    no action, restart the service, run a program, and restart the
    computer. And also the restart service after, that we can modify if
    how many minutes it should be.

![image](https://github.com/user-attachments/assets/fcdea9a4-99d3-4174-b591-1aea0b25ebb1)


6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

![image](https://github.com/user-attachments/assets/3080931b-8de3-4c9d-a641-f2ce4c11482f)


7.  Save the batch file in Z:\\lastname_timer.bat

> I did partitioning first to save my batch file in Z: drive.
>
![image](https://github.com/user-attachments/assets/2b73da1c-4fb8-47cf-b40e-4a3f18d20a1f)

>
![image](https://github.com/user-attachments/assets/6ee7af0a-e65a-431c-a9bf-1624b83205c4)


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
![image](https://github.com/user-attachments/assets/7757ef3a-575d-4592-920c-c16e8ee68791)


9.  Verify that BatchTimerService has been added to the services.

> **SS:**
>
![image](https://github.com/user-attachments/assets/fed487bd-8e57-43d3-b422-f64b769ab199)

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
![image](https://github.com/user-attachments/assets/c46270ca-12a3-457b-a6b1-ac818d8eb4af)

>
![image](https://github.com/user-attachments/assets/a7c43199-8745-44dd-9732-6d5577ad9842)


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
