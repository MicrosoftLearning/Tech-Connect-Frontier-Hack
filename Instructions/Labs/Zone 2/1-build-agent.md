## Create a New Agent in Copilot Studio

### Step 1: Access Microsoft Copilot Studio

- Open the Edge browser and navigate to +++https://copilotstudio.microsoft.com+++ and login with the following suggested Microsoft 365 work or school account:

**Username: +++@lab.CloudPortalCredential(User1).Username+++**

For the **user's password**, provide the following value:

**Password: +++@lab.CloudPortalCredential(User1).Password+++**

> [!TIP]
> If the login UI prompts you for the user's **temporary password**, provide the following value:
> 
> **Temporary Access Pass: +++@lab.CloudPortalCredential(User1).AccessToken+++**

- Wait between 10 and 15 seconds for the process to configure your personal developer environment to start. You will see a dialog informing you about the ongoing process of creating your personal environment.

### Step 2: Create the agent

Once you are in Copilot Studio, the tool will start with the agent creation wizard. Select **Configure** to switch to the agent configuration. If you cancel the wizard, select **Create** in the left navigation menu of Copilot Studio, then choose **+ New agent** to create a new agent and select **Configure** in the agent creation wizard.

Once you are in the **Configure** panel, define your new agent with the following (you can copy and paste the values):

- **Name**:

```text
Opportunity Review Advisor
```

- **Description**:

```text
An intelligent assistant that helps users explore customer opportunities by retrieving records and generating concise, data-grounded summaries.
```

- **Instructions**:

```text
You are a data-grounded assistant specializing in customer opportunity information.

You help users retrieve, understand, and summarize individual customer opportunities using the provided CRM dataset as your source of truth.

You can support users by:

- Locating a specific opportunity by name and returning the corresponding record
- Surfacing key fields such as customer, stage, value, and timeline indicators
- Producing concise, structured summaries based strictly on available data
- Calling out missing, incomplete, or ambiguous information

Always base your responses on the CRM data provided. Do not infer, assume, or generate recommendations unless explicitly instructed.
```

![Screenshot of Name, Description, and Instructions.](../Media/Name_description.png)

Select **Create** to create your new agent. 

The agent will be provisioned. Wait for the alert, "Your agent has been provisioned" or for the **Publish** button to become enabled to proceed with configuring your agent.

### Step 3: Attach knowledge

 Scroll down to the **Knowledge** section, select **+ Add knowledge**.

1. Select **Select to browse**
1. In file explorer, select **Desktop**
1. Select **Local Disk (C:)**
1. Select the file named **CRM_Opportunities.csv**
1. Select **Add to Agent**
1. A message will appear indicating that the file is being uploaded. This window will close after a few moments.

> **Note:**
> The process of uploading a file in this way may take up to 15 minutes. A status of **In Progress** will be shown next to the file name. You may move on to the next tasks while the file is being uploaded.

### Step 4: Build initial conversation starters

In this task, you are going to configure some conversation starters, which will provide users with suggested prompts when they start using your agent.

Scroll down to the **Suggested prompts** section, select the command **+ Add suggested prompts**, and add these helpful prompts:

1. Title: `Summarize an Opportunity` - Prompt: `Can you provide an Opportunity summary?`
1. Title: `Review a Customer Opportunity` - Prompt: `Can you review the details of a Customer Opportunity?`

Select **Save**.

For now, this is all you need to do in this step. You will revisit this section later to add more suggested prompts after you have configured topics for your agent.

![Screenshot of suggested prompts.](../Media/suggested_prompts.png)

## Step 5: Configure agent settings

Ensure that the following settings are configured for optimal performance:

- In the agent's **Select your Agent's model** section, ensure that the **GPT-5 Chat** model is selected for the best natural language understanding capabilities.

    ![Screenshot your agent's model.](../Media/gptmodel.png)

Now select the **Settings** command in the upper right corner of the screen and under the **Generative AI** section of settings, ensure the following settings:

- **Use generative AI orchestration for your agent's responses**: Yes
    ![Screenshot your agent's model.](../Media/orchestration.png)

- **Use general knowledge**: Off
- **Use information from the web**: Off

    ![Screenshot your agent's model.](../Media/Knowledge.png)

Select **Save** to update the settings and to ensure that only the knowledge base explicitly provided to the agent will be used when processing user's prompts.

Your "Opportunity Review Advisor" agent is now ready to be enhanced with intelligent topic routing capabilities.

Close the Settings panel by selecting the **X** icon in the upper right corner.

You may now move on to the next task in Zone 2, **Configure Topic flows for your agent**.
