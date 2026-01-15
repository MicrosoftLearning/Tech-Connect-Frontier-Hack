# Setup a Project in Azure AI Foundry

## Create a Project in Azure AI Foundry

1. Open the Edge browser and navigate to +++https://ai.azure.com+++

1. Select **Sign in** in the top right corner and sign in with the following account details:

    - **Username:** +++@lab.CloudPortalCredential(User1).Username+++
    - **Password:** +++@lab.CloudPortalCredential(User1).Password+++

        > [!TIP]
        > If the login UI prompts you for the user's **temporary password**, provide the following value: **+++@lab.CloudPortalCredential(User1).AccessToken+++**

1. After a few moments, you should see an Azure AI Foundry resource displayed under **Keep building with Microsoft Foundry**. Select the resource that starts with **Lab-** and ends with **-foundry**.

    ![Foundry resource image](../Media/foundryresource.png)

1. In the **Overview** tab, under **Resource details**, select **Open in management center**.

    ![Open in management center](../Media/managementcenter.png)

1. Select **New Project**. In the **Create Project** pane, enter the following:

    - **Project Name**: `<user-id>-foundry-project`
      (use your username without the domain suffix: +++@lab.CloudPortalCredential(User1).Username+++)

1. Select **Create**.

1. After the project is created, you will be taken to the project overview page. Ensure your user ID appears under **Project users** with a role of **Azure AI User**.

    ![Project users image](../Media/projectusers.png)

    > [!IMPORTANT]
    > If your user ID does not appear, select **+New User** and add your user ID with the role of **Azure AI User**.

## Navigate to the new Azure AI Foundry Portal and deploy your first model

Next, you’ll switch to the new Azure AI Foundry portal to continue the lab.

1. In the top right hand corner, select **Start Building**.

    ![Start building image](../Media/startbuilding.png)

1. You will be taken to the new Azure AI Foundry portal. In the top right corner, you will see several tabs like **Home**, **Discover**, **Build**, and **Operate**. Select the **Discover** tab.

    ![Discover tab image](../Media/discovertab.png)

1. While in the **Discover** tab, select **Models** from the left navigation pane.


    ![Models navigation image](../Media/modelsnavui.png)

1. In the search box, type `gpt-4.1-mini` and select the model from the search results.

    ![Model catalog image](../Media/searchmodelui.png)

1. Under **Details**, ensure that you see **Direct from Azure**.

    ![Direct from Azure image](../Media/directfromazure.png)

1. Select **Deploy** from the top right corner, then select **Default setting**. You will be brought to the Agent playground once the model is deployed.

## Create Your First Agent in Azure AI Foundry

1. While still in the Azure AI Foundry portal, select the **Agents** from the left navigation pane.

1. Select **Create agent**.

    ![create agent](../Media/newagentui.png)

1. In the **Create an agent** window that appears, name the agent `crm-data-access-agent`.

1. In the Agent setup page that appears, edit the following fields:

    - **Model:** ensure `gpt-4.1-mini` is selected
    - **Agent instructions:**

       ```text
       You are the CRM Data Access agent.
       Your ONLY job is to retrieve and return data from the provided CRM JSON file
       (Accounts, Leads, Opportunities).
    
       Rules:
       - Use only the attached CRM JSON data (file/knowledge).
       - Do not invent values or infer missing fields.
       - Do not provide recommendations or “next steps” unless the user explicitly asks.
       - Prefer exact matches for record names.
       - If you can’t find an exact match, say match_found=false and offer up to 5 close matches.
    
       Output format (always valid JSON):
       {
         "match_found": true,
         "entity_type": "account|lead|opportunity",
         "record_name": "",
         "record": {},
         "close_matches": []
       }
    
       If match_found=false, set record to {}.
       ```

1. Under **tools** select **Upload files**. This will allow the agent to ground its responses in the provided CRM dataset.

1. In the **Adding Files** window that appears, change the name and upload the file as follows:

    - **Vector index name** `crm-data-file`
    - Select **browse for files**, navigate to the desktop, select the **Sample Docs** folder, and then select **CRM_Synthetics_JSON_Data.json**.

1. Once the file is uploaded, select **Attach**.

1. Back in the **Agent setup** page, select the **Parameters** icon to the right of your model selection.

    ![Agents parameters](../Media/parameters.png)

1. Configure the following settings in the **Model parameters** pane that appears:

    - Lower the **Temperature** to `0.1` (If not set by default)
    - **Choose when to use tools**: set to `Always use`.

1. In the chat window to the right of the agent setup page, test the agent with the following prompt:

    ```text
    List all manufacturing accounts.
    ```

1. Review the agent's response in the chat window. You should see a valid JSON response with a list of manufacturer accounts from the CRM data you uploaded.

## Create a new workflow in Azure AI Foundry

1. In the Azure AI Foundry portal, select the **Workflows** tab from the left navigation pane.

1. Click on **Create**, then select **Blank workflow**.

    ![Create workflow image](../Media/createblankworkflow.png)

1. In the workflow canvas that appears, under **Add a workflow action**, select **Send message**.

1. In the **Send message** pane that appears, under **Message to send**, enter the following:

    ```text
    How can I help you today?
    ```

1. Select **Done**.

    Your workflow should now look like this:

    ![Workflow canvas image](../Media/workflowcanvas.png)

1. Select **Save**, and when prompted, name the workflow `crm-workflow`.

## Next steps

You’ve now completed the required setup for Zone 3. From here, you will move into a group-based challenge focused on:

- Designing agent responsibilities
- Orchestrating agents using workflows
- Testing and refining behavior in the Foundry UI

All challenge tasks can be completed **entirely in the Azure AI Foundry portal**.

If you prefer working in code, you may optionally configure the Azure AI Foundry extension in Visual Studio Code in the next task. VS Code can be useful for inspecting agents and experimenting, but it is not required for this zone.

➡️ Optional: Set up VS Code for Azure AI Foundry  
➡️ Continue to the **Zone 3 Challenge**
