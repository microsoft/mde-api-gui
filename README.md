# GUI for MDE API sample app
Simple PowerShell GUI for Microsoft Defender for Endpoint API machine actions.
![image](https://user-images.githubusercontent.com/25099900/195406810-55511f50-d1c7-4e80-94e1-945cfca2a219.png)
## Get started
1. Create Azure AD application as described here: https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/apis-intro?view=o365-worldwide
2. Grant the following API permissions to the application:

| Permission | Description |
|-------------------------|----------------------|
| AdvancedQuery.Read.All	| Run advanced queries |
| Machine.Isolate |	Isolate machine |
| Machine.ReadWrite.All |	Read and write all machine information (used for tagging) |
| Machine.Scan |	Scan machine |

3. Create application secret.
## Usage
1. **Connect** with AAD Tenant ID, Application Id and Application Secret of the application created earlier.
2. **Get Devices** that you want to perform actions on, using one of the following methods:
    * Advanced Hunting query (query result should contain DeviceName and DeviceId fields)
    * CSV file (single Name column with machine FQDNs)
    * Devices list separated with commas
3. Confirm selection in PowerShell forms pop-up.
4. Choose action that you want to perform on **Selected Devices**, the following actions are currently available:
    * Specify device tag in text box and **Apply tag**.
    * Run **AV Scan**.
    * **Isolate**/Release device.
5. Verify actions result with **Logs** text box.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
