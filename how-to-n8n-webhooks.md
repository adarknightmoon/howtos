# How to Capture External Data Streams using n8n Webhooks?

**Question:** 
How do I set up n8n to automatically receive and process JSON data payloads from an external application or API?

**Answer:**
You can capture external data payloads by setting up a **Webhook Node** as the trigger in your n8n workflow.

1. Add the **Webhook** node to a new workflow.
2. Set the **HTTP Method** to `POST` (or `GET`, depending on the sending application).
3. Copy the **Test URL** provided by the node.
4. Go to your external application (e.g., Moodle, GitHub, or a custom script) and paste the Test URL into its webhook configuration settings.
5. Click **Listen for Test Event** in n8n, and trigger the event from the external app.
6. Once n8n captures the JSON data, you can map the incoming variables to subsequent nodes (like Google Sheets or a Database) to automate your data pipeline. Remember to switch to the **Production URL** when making the workflow live.
