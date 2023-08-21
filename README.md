# Add Dynatrace extension for azure-appservice

- Go to Azure CLI Cloudshell 
  - https://portal.azure.com/#cloudshell
- On the command prompt type the following: 
  - ``` git clone https://github.com/jgurbani/azure-app-dt-ext-deploy ```
  - ```  cd azure-app-dt-ext-deploy/ ```
- Make changes to the parameters file
  ```
   vim app-service-dtExtension-install-parameters.json
  ```
    - Update the site_name, environmentID, APIToken, APIUrl and location values
- Run the ARM template in Azure CLI Cloudsheell with the following command:  
    ```
      az deployment group create  --subscription  <AzSubscriptionName> --resource-group <AzResourceGroup> --template-file app-service-dTExtension-install-armTemplate.json --parameters @app-service-dtExtension-install-parameters.json  
    ```
- Restart the App Service
  
    ```
    az webapp
    ```
