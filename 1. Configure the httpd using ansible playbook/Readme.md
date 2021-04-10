### Step1: Installing the httpd on the managed nodes.
### Step2: Start the httpd services
### Step3: Copy the the webpages to /var/www/html directory 


![1](./Images/1.PNG)

![2](./Images/2.PNG)

![3](./Images/3.PNG)

![4](./Images/4.PNG)

```yml

- hosts: all
  tasks:
  - package: 
      name: "httpd"
      state: present
  - copy:
    src: "my.html"
    dest: "/var/www/html/index.html"
    
  - service: 
    name: "httpd"
    state: started
    
```
