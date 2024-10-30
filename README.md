# Magento 2 module for Zero downtime deployment.

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Module prevents showing database versions exception when you pull new code to the server.
The best idea is to use CI/CD with Docker/Kubernetes.
Suggested deployment:

- get docker base image
- run php bin/magento setup:upgrade on destination database
- run php bin/magento setup:di:compile and php bin/magento setup:static-content:deploy on build container
- deploy new container

NOTICE: If new version contain new classes (for example in EAV) or changed logic, Magento could behave unpredictable.
You are using this module at your own risk!

# **Install**

### Git
- Locate the **/app/code** directory which should be under the magento root installation.
- If the **code** folder is not there, create it.
- Create a folder **Monogo** inside the **code** folder. 
- Change to the **Monogo** folder and clone the Git repository (https://github.com/nholuongut/magento-2-module-for-zero-downtime-deployment.git) into **Monogo** specifying the local repository folder to be **OptimizeDatabase** 
e.g. 

``` git clone https://github.com/nholuongut/magento-2-module-for-zero-downtime-deployment.git```

### Composer
```composer require monogo/magento-2-module-for-zero-downtime-deployment```

### Magento Setup
- Run Magento commands

```php bin/magento setup:upgrade```

```php bin/magento setup:di:compile```

```php bin/magento setup:static-content:deploy```

# **App Configuration Options**

Go to Stores->Configuration->Monogo->Zero downtime deployment

- Enable module **Default value is 0 (No)**
- Enable logger **Default value is 0 (No)**

# **TODO**
- Tests

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟