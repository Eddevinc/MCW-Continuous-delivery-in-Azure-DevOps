![Microsoft Cloud Workshops](https://github.com/Microsoft/MCW-Template-Cloud-Workshop/raw/master/Media/ms-cloud-workshop.png "Microsoft Cloud Workshops")

<div class="MCWHeader1">
Continuous delivery in Azure DevOps
</div>

<div class="MCWHeader2">
Before the hands-on lab setup guide
</div>

<div class="MCWHeader3">
March 2020
</div>

Information in this document, including URL and other Internet Web site references, is subject to change without notice. Unless otherwise noted, the example companies, organizations, products, domain names, e-mail addresses, logos, people, places, and events depicted herein are fictitious, and no association with any real company, organization, product, domain name, e-mail address, logo, person, place or event is intended or should be inferred. Complying with all applicable copyright laws is the responsibility of the user. Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.

Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document. Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.

The names of manufacturers, products, or URLs are provided for informational purposes only and Microsoft makes no representations and warranties, either expressed, implied, or statutory, regarding these manufacturers or the use of the products with any Microsoft technologies. The inclusion of a manufacturer or product does not imply endorsement of Microsoft of the manufacturer or product. Links may be provided to third party sites. Such sites are not under the control of Microsoft and Microsoft is not responsible for the contents of any linked site or any link contained in a linked site, or any changes or updates to such sites. Microsoft is not responsible for webcasting or any other form of transmission received from any linked site. Microsoft is providing these links to you only as a convenience, and the inclusion of any link does not imply endorsement of Microsoft of the site or the products contained therein.

© 2020 Microsoft Corporation. All rights reserved.

Microsoft and the trademarks listed at <https://<span></span>www.microsoft.com/en-us/legal/intellectualproperty/Trademarks/Usage/General.aspx> are trademarks of the Microsoft group of companies. All other trademarks are property of their respective owners.

**Contents**

<!-- TOC -->

- [Continuous delivery in Azure DevOps before the hands-on lab setup guide](#continuous-delivery-in-azure-devops-before-the-hands-on-lab-setup-guide)
  - [Requirements](#requirements)
  - [Before the hands-on lab](#before-the-hands-on-lab)
    - [Prerequisites](#prerequisites)
    - [Task 1: Use Azure Shell as your development environment](#task-1-use-azure-shell-as-your-development-environment)
    - [Task 2: Download the exercise files](#task-2-download-the-exercise-files)

<!-- /TOC -->

# Continuous delivery in Azure DevOps before the hands-on lab setup guide

## Requirements

1.  Microsoft Azure subscription

## Before the hands-on lab

Duration: 10 minutes

In this lab, you will configure a developer environment and download the required files for this course if you do not already have one that meets the requirements.

### Prerequisites

-   Microsoft Azure subscription <http://azure.microsoft.com/en-us/pricing/free-trial/>

### Task 1: Use Azure Shell as your development environment

>**Note**: This workshop can be completed using only the Azure Cloud Shell.

1.  In a web browser, navigate to https://shell.azure.com. Alternatively, from the Azure web portal, launch the **Azure Cloud Shell**. It has common Azure tools preinstalled and configured to use with your account.

    ![This is a screenshot of an icon used to launch the Azure Cloud Shell from the Azure Portal.](images/Setup/image3.png "Azure Cloud Shell launch icon")
    
2.  After log in to **Azure Cloud Shell** select the **Bash** option from the **Welcome to Azure Cloud shell** dialog box and now you will see a **You have no storage mounted box** and click the option for **Show advanced settings**.

3.  Select **Create new** under **Storage account** and provide values as below:
 
      - **Storage account** : **storageDeployementid**
      - **File Share** : **blob**
      
  >**Note**: Storage account name should be always unique, Deployement Id can received from **Environment Details** tab     

4.  From inside the Azure Cloud Shell type these commands to configure Git:

    ```bash
    git config --global user.name "<your name>"
    ```

    ```bash
    git config --global user.email <your email>
    ```

>**Note**: Replace the <your name> and <your email> placeholders with your own full name and e-mail address respectively, removing the '<' and '>' characters from the placeholders. This information will be used by the Git CLI for any commits you might do from Azure Cloud Shell.

### Task 2: Download the exercise files

1.  Using the Azure Cloud Shell, you can download the file by executing the following command inside the Cloud Shell window (all on one line):

    ```bash
    curl -o studentfiles.zip https://cloudworkshop.blob.core.windows.net/agile-continous-delivery/studentfiles.zip
    ```

2.  Extract the contents of the file to the new folder. Using the Azure Cloud Shell, you can execute the following command inside the Cloud Shell window:

    ```bash
    unzip studentfiles.zip
    ```

3.  When unzipped, there will be a new folder named **studentfiles**. Navigate to the newly created **studentfiles** directory.

    ```bash
    cd studentfiles
    ```
   
4.  Inside the **studentfiles** folder, there are two folders named **armtemplate** and **tailspintoysweb**. The workshop will refer to these folders throughout the exercises.

>**Note**: Using the Azure Cloud Shell, you
 can load the integrated code editor (Cloud Shell Editor) at any time with the following command:
```bash
code .
```

You should follow all steps provided *before* starting the Hands-on Lab.
