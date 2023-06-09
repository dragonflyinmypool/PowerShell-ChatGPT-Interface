# PowerShell interface to query GPT3/4
This is a general interface to query GPT3/4 from PowerShell.

**Type in powerShell**: q create a new folder called helloWorld

**And get the answer**: New-Item -ItemType Directory -Name "helloWorld"
(all without leaving the terminal)

## Requirements
- Windows PowerShell
- Node.js

## Usage
1. Create a file called `api.js` containing the following code:
   ```javascript
   // export the api key
   module.exports = {
     apiKey: 'paste api key here',
   };
   ```
   Note: This file is set to be ignored by Git to protect the API key.

2. Run the `mainScript.ps1` file by opening PowerShell and navigating to the directory containing the file. Then, run the command:
   ```powershell
   .\mainScript.ps1    >your query here<
   >open response will appear here<

   ```   
   Note: You can customize the prompt output in the `index.js` file under the "content" field.

## Setting a permanent alias (OPTIONAL)
After completing these steps, you can use the q alias to run the mainScript.ps1 file from anywhere in PowerShell.
1. To create a permanent alias for the `mainScript.ps1` file, open Notepad and enter the following command:

   ```powershell
   Set-Alias q C:\path\to\mainScript.ps1
   ```
   Replace `C:\path\to\mainScript.ps1` with the actual path to the `mainScript.ps1` file on your computer.

2. Save the file as `Microsoft.PowerShell_profile.ps1` in the following directory:

   ```plaintext
   C:\Users\{your_username}\Documents\WindowsPowerShell\
   ```
   Note: If the `WindowsPowerShell` folder does not exist, create it. Once the file is saved, close and reopen PowerShell for the changes to take effect.

you can now use the `q` alias to run the `mainScript.ps1` file from anywhere in PowerShell.
