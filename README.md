<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Tools Workshop</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        h1, h2, h3 {
            color: #0070d2;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 4px;
            overflow-x: auto;
        }
        .tip {
            background-color: #e3f2fd;
            border-left: 5px solid #2196f3;
            padding: 10px;
            margin: 10px 0;
        }
        img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <h1>Modern Tools Workshop</h1>

    <h2>1. Code Builder</h2>
    <h3>1.1 Sign up for a Salesforce org</h3>
    <ol>
        <li>Follow your instructor's instructions to get a Salesforce org provisioned with Code Builder.</li>
        <li>Write down your user ID and password for later use.</li>
        <li>Go to <a href="https://login.salesforce.com">login.salesforce.com</a> and log in to your org.</li>
    </ol>

    <h3>1.2 Enable and launch Code Builder</h3>
    <h4>Step 1: Launch Code Builder</h4>
    <ol>
        <li>Click the Setup icon (gear icon in the upper right corner), and click Setup.</li>
        <li>In Quick Find, search for Code Builder, and select Code Builder.</li>
        <li>Dismiss the error message (due to pre-installation of Code Builder).</li>
        <li>Click the Enable Code Builder toggle. Review and accept the license agreement.</li>
        <li>Click the App Launcher icon (waffle icon in the upper left corner), and select the Code Builder app.</li>
        <li>In the Code Builder Dashboard, click the Launch button.</li>
    </ol>
    <div class="tip">
        <strong>TIP:</strong> It will take a few minutes for Code Builder to fully initialize. Wait for the Let's Get You Started page to appear before continuing.
    </div>

    <h4>Step 2: Create an SFDX Project</h4>
    <ol>
        <li>Open the command palette (Press CMD+SHIFT+P on Mac or CTRL+SHIFT+P on PC).</li>
        <li>Search SFDX and Click on SFDX: Create Project with Manifest</li>
        <li>Click Standard</li>
        <li>Enter MODERN_TOOLS_WORKSHOP for the project name and press Return.</li>
    </ol>

    <h4>Step 3: Authorize your Org</h4>
    <ol>
        <li>Open the command palette (Press CMD+SHIFT+P on Mac or CTRL+SHIFT+P on PC).</li>
        <li>Search for "Authorize an Org". If not available, wait for Code Builder to fully initialize.</li>
        <li>Select SFDX: Authorize an Org.</li>
        <li>Select Project Default.</li>
        <li>Enter MODERN-TOOLS-WORKSHOP for the org alias and press Return.</li>
        <li>Click Connect.</li>
        <li>Log in to your org using your credentials.</li>
        <li>Click Allow.</li>
        <li>Click Continue.</li>
    </ol>

    <h2>2. Retrieving Metadata from the Development Org</h2>
    <h3>2.1 Retrieving Custom Objects Metadata Using Org Browser</h3>
    <ol>
        <li>In the VSCode Activity Bar, click on the Salesforce icon to open the Org Browser.</li>
        <li>Expand the metadata types by clicking on the dropdown arrows.</li>
        <li>Locate the CustomObject metadata type.</li>
        <li>Click on the CustomObject metadata type to view all custom objects.</li>
        <li>Click the download icon (cloud with a down arrow) at the top of the Org Browser panel to retrieve the selected custom objects' metadata.</li>
    </ol>
    <p>The metadata will be retrieved and stored in your project's <code>force-app/main/default/objects</code> directory.</p>

    <h2>3. Create an Apex Class PersonalizedExperiencesController</h2>
    <ol>
        <li>Open the Command Palette (Ctrl+Shift+P on Windows or Cmd+Shift+P on Mac).</li>
        <li>Type "SFDX: Create Apex Class" and select it.</li>
        <li>Enter "PersonalizedExperiencesController" as the class name.</li>
        <li>Select the default directory for the class (usually <code>force-app/main/default/classes</code>).</li>
    </ol>
    <p>The new <code>PersonalizedExperiencesController</code> class file will be created and opened in the editor.</p>

    <h2>4. Einstein for Developers (Beta)</h2>
    <h3>4.1 Activate Einstein for Developers</h3>
    <img src="https://gist.github.com/user-attachments/assets/15e4fab1-1903-40f0-9ace-e58c270d1d42" alt="Activate Einstein for Developers">

    <h3>4.2 Create a Prompt to generate the Apex class</h3>
    <p>Use the following prompt:</p>
    <pre>Generate a class PersonalizedExperiencesController with method name getMatchingExperiences. The method has a parameter of contact Id and the method fetches Experience records matching type field by fields Interest1__c or Interest2__c or Interest3__c from the contact record. Keep the query static</pre>
    <img src="https://gist.github.com/user-attachments/assets/c3093677-3738-4603-ab9c-52fdc6e69102" alt="Einstein for Developers Prompt">

    <h2>5. Code Analyzer</h2>
    <h3>5.1 Install Code Analyzer CLI Plugin</h3>
    <ol>
        <li>Open the Integrated Terminal in VSCode.</li>
        <li>Run the following command:
            <pre>sf plugins install @salesforce/sfdx-scanner</pre>
        </li>
    </ol>

    <h3>5.2 Install Code Analyzer VSCode Extensions</h3>
    <ol>
        <li>Open the Extensions view in VSCode.</li>
        <li>Search for "Salesforce Code Analyzer" in the search bar.</li>
        <li>Click on the "Salesforce Code Analyzer" extension.</li>
        <li>Click the Install button and wait for the installation to complete.</li>
        <li>Reload VSCode if prompted.</li>
    </ol>

    <h3>5.3 Scan for Code Vulnerability</h3>
    <img src="https://gist.github.com/user-attachments/assets/3db96129-575c-43ba-9f30-b64089ba9e74" alt="Code Analyzer Scan">

</body>
</html>
