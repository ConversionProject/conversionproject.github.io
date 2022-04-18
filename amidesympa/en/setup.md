---
title: 'Sympa AMI: AMI setup proceduce'
---

\[[Japanese](../ja/setup.md)\]
\[**English**\]

\[[Sympa AMI](../en.md) &gt; AMI setup proceduce\]

Sympa AMI
=========

AMI setup procedure
-------------------

### 1. Launch instance from image

  1. On EC2 Dashboard, select 'Image' > 'AMI' in the left pane.
  2. Select 'Public Image' from the search box pull-down and enter AMI ID above.
  3. Select the image and under 'Action' select 'Launch'.
  4. Create an instance and set the security group according to your requirements.
     Create the SSH key pair as necessity.
  5. Once the created instance has been started, select 'Network & Security' > 'Elastic IP' in the left pane and associate the IP address with the instance.


### 2. Initial configuration

  1. Access to the instance via SSH. Note that the login user is 'admin'.

     ----

  2. Log in and a menu will appear.

     <img src="../images/sympa_001.JPG" width="70%" />

     Select "(Re)configure Sympa": Enter '1' and press Enter.

     Thereafter, perform basic configuration of the Sympa and related software.

  3. Launch web browser and access to web UI.
     Follow "First login" link, input a listmaster address chosen on previous chapter, and then click "Send my password" button.
     According to description in the email sent to that address, choose the password.
