# ANSIBLE REFACTORING AND STATIC ASSIGNMENTS

## STEP 1:- 
1. I created a new directory; "ansible-config-artifact" and I changed permissions to the directory
     ![Project12](images/image1.PNG)
2. On jenkins console, I installed "copy artifact" plugin then I created another freestyle project named save_artifacts which I configured accordingly
      ![Project12](images/image2.PNG)
      ![Project12](images/image3.PNG)    
      ![Project12](images/image4.PNG)

3. I tested the setup and it worked very much well
      ![Project12](images/image5.PNG)
      ![Project12](images/image6.PNG)


## STEP 2:-

1. I created a new file in Playbooks folder and named it site.yml
2. I created a new folder in the root repository and named it "static-assignments"
3. I moved "common.yml" file into the newly created folder then I configured the file to import playbook
       
       ![Project12](images/image7.PNG)


## STEP 3:-

1. I launched two new ec2-instances and tagged them web-uat
            ![Project12](images/image8.PNG)
2. I created a new directory named Roles and I initialized Ansible-galaxy webserver
             ![Project12](images/image9.PNG)
             ![Project12](images/image10.PNG)

3. I updated my ./inventory/uat.yml file with the IP address of my uat-webservers
              ![Project12](images/image12.PNG)

4. Then I provide a full path to my Roles directory in the ansible.cfg file
              ![Project12](images/image13.PNG)

5. I wrote some configuration tasks in the main.yml file of the tasks directory
              ![Project12](images/image14.PNG)

6. I created a new file; uat-webservers.yml in the static-assignments folder so as to create new assignments for the uat-webservers
              ![Project12](images/image15.PNG)

7. Then I refered the uat-webserver's role in my site.yml file
                ![Project12](images/image16.PNG)


                



