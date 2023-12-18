# Ubuntu

  Ubuntu is a popular, open-source Linux distribution that is widely used for desktop computing, server environments, and various other applications.

## Key features and aspects of Ubuntu:

  - Ubuntu is based on the Linux kernel, which is the core of the operating system.
  - Ubuntu is \ open-source software, which means its source code is freely available, and users have the right to modify, distribute, and contribute to the development of the operating system.
  - Ubuntu features a user-friendly GNOME desktop environment.
  - Ubuntu uses the Debian package management system.
  - Ubuntu provides a vast repository of software packages that users can access to install applications, libraries, and system tools.
  - Ubuntu Long-Term Support (LTS) releases are supported for five years, providing stability and extended support for enterprise environments.
  - Ubuntu has a large and active community of users and developers.
  - Ubuntu also offers a server edition that is widely used for hosting websites, running applications, and managing server infrastructure.
  - There is also a specialized version called Ubuntu Core for IoT devices.

## Installing Ubuntu:

  - To install Ubuntu in VMware, you'll need the Ubuntu ISO file, which you can download from the official Ubuntu website.
  - Make sure you have VMware installed on your computer. Create a VM with Ubuntu Desktop OS. If you need assistance please refer to https://github.com/Agnesh-K/VMware
  - The VM will boot from the Ubuntu ISO.
    
    ![Screenshot (22)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/7854a61e-2e46-4410-8912-52f2e31abaac)
    
  - Choose your language, keyboard layout, and other preferences.
    
    ![Screenshot (23)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/09e0209e-2b9d-4d48-be4e-4a7af779b120)
    
  - Follow the on-screen instructions to install Ubuntu. Allow the installation process to complete.
    
    ![Screenshot (25)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/9cded07c-9fa6-4b74-9ff5-d105ecb7798b)
    
  - After Ubuntu is installed, start using your Ubuntu V.M.
    
    ![Screenshot (27)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/290edd4b-e240-4afc-9421-02836e1890a7)
    
    ![Screenshot (28)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/3469ffcc-e90e-4cd3-9c76-3b75c35d5111)

## Basics of using Ubuntu:
  1. Use ALT+CTRL+T to open Terminal also called the command-line interface (CLI) which is a text-based interface for users to interact with the O.S. by typing commands.
     
     ![Screenshot (29)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/d174d9c1-b4c9-44a0-916f-b4724e342f0b)
     
  3. Set password for root user: (for security password enetered is not shown in linux)
     ```
     sudo root passwd
     ```
     
     ![Screenshot (31)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/9359dcc0-d5b8-4eb0-8d9b-2a2119e88d28)
     
  4. Switch user to root
     ```
     su
     ```
     ```
     sudo bash
     ```
     
  5. Run apache2 web server from your device:
     - Run below commands in sequence
       
     ```
     sudo apt update
     sudo apt install apache2 -y
     sudo apt install net-tools
     sudo systemctl start apache2
     sudo netstat -anp | grep apache2                 #to_see_at_which_port_server_is_running
     sudo systemctl status apache2                    #to_check_status_whether_server_is_running_or_not
     ```
     
     ![Screenshot (32)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/e806c2d8-7d10-43ae-8e63-7bfa84f28c32)

     - Open mozilla firefox and go to url localhost:80 to check default apache2 webapage
     
     ![Screenshot (33)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/080fadaa-b19e-4c3c-8a57-3b464917b9ea)

     - Change default apache html page to personalised html webpage
     ```
     touch index.html                                 #create a file named index.html
     nano index.html                                  #paste the html code inside the file index.html
     sudo cp index.html /var/www/html/index.html      #replace the default apache2 html page with personalised html page
     ```
     - Open mozilla firefox and go to url localhost:80 to check if created webpage is online

     ![Screenshot (34)](https://github.com/Agnesh-K/Ubuntu/assets/154126091/08dc1c8d-4f36-4094-b848-8e81bb1e6485)
     
     - Stop the running apache2 server:
      ```
      sudo systemctl stop apache2
      ```

      ![image](https://github.com/Agnesh-K/Ubuntu/assets/154126091/30fe09f3-b613-4d15-b835-e873337e01b3)

  6. Run 

   11  sudo status apache2
   12  apache2 status
   13  sudo netstat
   14  sudo check apache2
   15  sudo netstat | grep apache2
   16  
   17  sudo netstat
   18  sudo netstat | grep apache2
   19  sudo systemctl apache2 restart
   20  sudo systemctl restart apache2
   21  sudo netstat | grep apache2
   22  
   23  history

