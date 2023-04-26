# Auto-GPT Notion Plugin
> Under rapid development

Extend Auto-GPT capabilities:
- Read Notion pages
- Write to Notion pages

Applications:
- Automatically collects information from the web and archives it to Notion.
- Notion as a knowledge base, chat with it on Discord/Slack.

## Demo
```
# ai_settings.yaml
ai_goals:
- Use "google" command to search what is Auto-GPT, and save the result to a Notion page
ai_name: Notion-GPT
ai_role: Research assistant
```

![image](https://user-images.githubusercontent.com/20609724/234296458-f303140f-bf58-48d8-89e2-06f52806893d.png)

## Install
**Do not clone this repo**, the working directory and environment are under **Auto-GPT**.

1. Install [Auto-GPT](https://github.com/Significant-Gravitas/Auto-GPT) and make sure you can run it successfully.
2. Install extra dependencies for this plugin.
    ```
    pip install notion-client python-dotenv auto_gpt_plugin_template
    ```
3. [Click Here](https://github.com/doutv/Auto-GPT-Notion/archive/refs/heads/master.zip) to download the source code as **ZIP**, and place the **ZIP** file under `plugins/`.
4. Notion settings:
   1. Create an integration [here](https://www.notion.so/my-integrations), and get the token `NOTION_TOKEN`.
   2. Duplicate [this database template](https://doutv.notion.site/e3187aaa1aed42c39f0f372fdf84655e?v=b892e5b7d13f49ec8ff200916e79cf5b), click "Duplicate" on upper right corner.
   3. Share the newly created database with your integration, click "..." on upper right corner, then click "Add connections" and input the integration name in the first step.
   4. Save the database ID `NOTION_DATABASE_ID`, you can get from the database url.
        ```
        For example:
        https://www.notion.so/doutv/2e2030693c624c258bcc402ef8d4b357?v=...
                                    |-------- database ID ----------|
        NOTION_DATABASE_ID=2e2030693c624c258bcc402ef8d4b357
        ```
   6. [Check the Notion official docs for detailed instructions.](https://developers.notion.com/docs/create-a-notion-integration)
5. Edit `.env`:
   1. Add this plugin `AutoGPTNotion`to Auto-GPT plugin whitelist.
        ```
        ALLOWLISTED_PLUGINS=AutoGPTNotion
        ```
   2. Add Notion token and database id to `.env` under Auto-GPT directory.
        ```
        ################################################################################
        ### Notion
        ################################################################################

        NOTION_TOKEN=<Notion integration token>
        NOTION_DATABASE_ID=<Notion database id>
        ```
6. Run Auto-GPT and enjoy!

If you encounter problems or have any ideas, feel free to discuss:
- [Issues](https://github.com/doutv/Auto-GPT-Notion/issues)
- [Discord Channel](https://discord.com/channels/1092243196446249134/1098882305000472626)

## Contribution
This plugin is under development. 

Join me by submitting issues and pull requests.
