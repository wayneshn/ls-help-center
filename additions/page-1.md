# Page 1

Question title Question content Answer

how is this better than using an existing automation tool? Any automation tool (zapier make activepieces etc) will have SHeets connection with calculation options.  Other than saving us from opening a separate tab for that, how is this better?  It looks like there are limited options in here and also gsheets is always evolving, so I'm curious if this has a sustainable advantage.  Also data privacy wise, what assurances do we have?  Thanks! Hi, the difference between Logic Sheets and the alternatives you mentioned is that LS is centered around GSheets and it has more GSheets-specific actions and triggers. LS is also evolving all the time. We currently don't support calculations because it can be done in GSheets but we will add this to our actions. Regarding data privacy, LS only runs in your GSheets and your data never leaves GSheets. Think of it as a piece of software that runs in your local device. We don't store any data already in your Google Sheets. Thanks!

Can I schedule something like webhook trigger 1 row of the sheet per hour using Logic Sheet And then the next hour, does it trigger the next row? Hi, yes, this is possible. There might be some extra setup, you need to reverse the order of the spreadsheet manually so that the latest data to be sent is always in the bottom. YOu can set up an hourly trigger and send the last row to a webhook using our HTTP request action, then use the "Remove last row" action to remove the last row so that the next hour the next row is the last row, and will be sent to webhook. This will remove data in your spreadsheet so you'd better backup the sheet before the automation runs.

Grist ? Hi. Can you make a good integration with Grist. It's very popular and very advanced database administration and management software, Google sheets alternative. Hi thanks for your feature request. We are currently working on integrating with as many services as possible and we will look into Grist asap. Thanks!

Gmail or Workspace account do I need a Google Workspace email account, or can I use a standard Gmail account? Asking cos I know your other tool required a Workspace plan. Thanks. Hi, yes you can use a standard Gmail account for Logic Sheet and purcahse the individual plan. Google Workspace is only required for the Team and Enterprise plans. The individual plan has the full features of Logic Sheet but it only contains one license. The Team and Enterprise plans contain multiple licenses for users in the same Google Workspace.

Data parse from email and forward? Can I identify a data value within a received email - an email address - and then create an automation - forward the received email to that email - with this app? HI, thanks for your question. Logic Sheet is capable of sending emails from Google Sheets. It however can't access your Gmail because it only runs in Google Sheets. So it can't parse values received by your email. Please let me know if you hare more questions! Wei

null telegram, noysi or ninjapipe\nI see whatsapp is in your status, do your consider also integrate telegram or noysi for sending messages (like to slack) and/or integrate with ninjapipe.? Hi, yes, we will try to integrate Telegram in the future.

awesome one more question do you consider noysi as integration. it is as slack, but a LTD an - as i think much better. unfortunatelly only the big ones (pabbly, zapir) do have direct connections to noysi. I know you focus on the most useful application, but since you are on platform and already have slack integrated, it could be interesting for you.!? :)

null could i do anything with you software which i cant via pabbly/activepieces/...?\nI work a lot with google sheets, but i am just curious if would be a benefit for me. With activepieces i just "ask" if something changed and if yes if it changed to a specific pattern and then i do something. so what can your software do more of?\nAdditionally do you already have an implementation for activepieces and if not do you offer an api and the code for it so we just could send an http request in activepieces.? Hi, Logic Sheet is an automation tool designed for Google Sheets and it's actions and triggers are centered around Google Sheets capabilities, such as sheet edit, form submit, and so on. It can perform actions such as sending email/Slack, update rows or cells in Google Sheets. It is also capable of sending HTTP Requests so if activepieces has an API, it can be automated by Logic Sheet. Best, Wei

null For Tier 1, it's one account but any number of sheets within that account? Hi yes, the tier 1 license is for on Google account and there is no limit on how many spreadsheets you use Logic Sheet in.

null I have created My Stock portfolio sheet in Google sheet.\n\nIs it possible to develop a condition on the Entire column L (Which represents per cent UP/Down from Purchase price), for example, if the Cell value of L26 is updated with 12 then the automation tool will send a mail with the following details\n\nSubject: {C26} up by {L26}\nBody:\n{C26} is Up by {L26}% from your purchase price of {E26}. its CMP is {F26} and running profit is {G26}.\n\nColumn Details are as Follows:\nColumn : Data\nA : Serial Number\nB: Bought Date\nC: Stock Name\nD: Quantity Purchased\nE: Purchase Price\nF: Current Market Price of Stock\nG: Profit /Loss of stock\n\nThe condition will Check for the Entire column L and the second condition would be that the D column is Greater than Zero. Hi thanks for your question! Yes, that is exactly what Logic Sheet is built for. Except that instead of using {C26}, we use \{{Range C26\}} to refer to the value of cell C26 in the sheet. The condition can also be achieved by setting the condition to "When cell L26 is 12" in this case. You can try to set the automation up after redeeming your code. You can also contact us for help via our live chat. Wei

null Is it customisable? can it be connected to Notion agency kit? Hi, yes you can connect Google Sheets to Notion using Logic Sheet. Notion agency kit is Notion templates so you can connect to it. Logic Sheet supports sending data from Google Sheets to Notion when an automation is triggered.

null can i use this for send data as a webhook to whatsapp gateway unofficial platform? Hi, thanks for your question. Yes, you can send webhooks to API endpoints. This can be done via our HTTP Request action(sending webhook is essentially sending a GET or POST HTTP Request). I have tested WHAPI to send WhatsApp messages before and it works perfectly. Best, Wei

Hi. What app whapi you mean? Is it https://whapi.id or https://whapi.cloud?

null Can I track and add events on public read google sheets which are not located in my google account but shared with me? Hi thanks for your question. You can track events in Google Sheets that are shared with you, but you need to have the "editor" access to create automations and track events in the sheet. The read permission is not sufficient for tracking events. Let me know if you have more questions. Wei

null Does tier 1 support unlimited google sheets (with only one gmail account?) Just to make sure I understood correctly. Hi, thanks for your question. Yes, it supports unlimited Google Sheets files for one Google account. There is no limit on how many files you can use Logic Sheet in. Wei

null I want to create automations for clients.  Some of the sheets that I am working on have been created by a different author (in client's company), but share with me.  Can I use this automation for shared sheets? Hi thanks for your question. Yes, you can create automations using Logic Sheet as long as you have editor access to the spreadsheet file shared with you. It is recommended that the owner of the spreadsheet installs Logic Sheet but it's not required. Only the user who creates the automation needs a Logic Sheet license.

If you no longer want the original person who shared the Google Sheet to have ownership or access, you can make a copy of the file. \n\nThen you will own the copy and control access.\n\nThis would become your new working version.

null We are collecting contact details from google Forms, can we use this tool to add them to Google Contats ? Hi yes, this is made possible with our Google Forms Received trigger and the HTTP Request action. With this automaiton, you can trigger an automaiton everytime when a Google Form response is received. Then in the action, you can use HTTP Request to send the form data to Google People API to create a contact. You can read the documentation here https://developers.google.com/people/api/rest/v1/people/createContact.\nThis may need a little bit of API knowledge to set up, you can reach out to me when you have redeemed your license. I will help you set it up.\nWei

null Glad to see you back here. I just want to understand the new stacking option. I have already purchased a code before and linked it to my personal Gmail account. If I stack 2 or more codes, will I be able to use them with additional Gmail accounts? Can I install them on other personal Gmail accounts or on those of my team?\n\nI'm confused because you mentioned that the user should be from the same Google Workspace organization. However, many of us, including myself, do not use Google Workspace. We use Zoho and other CRM tools for organization, and Yandex for business emails. Nonetheless, most of us have free Google accounts for Google Sheets. How can we utilize the stacking feature to use Logic Sheet with my team?\n\nThank you. Hi thanks for your question. I understand the situation you mentioned. For your specific case, if you already have an individual license, by stacking 1 more code you will be upgraded to the 5-user Team plan, and by stacking 2 more codes you will be upgraded to the unlimited users Enterprise plan. Since Google Sheets runs in Google Workspace, we rely on the Google Workspace Organization to verify user licenses, and to avoid abuse of your license system. But if you don's use Google Workspace, here is what we normally do: \n\nIf you have the Team plan and you don't use Google Worksapce,  please send us 5 email address that you want to license, stating that they all work in your organization that thaty they are not external users. We will add them to your license.\n\nIf you have the Enterprise plan and you don't use Google Worksapce,  please send us up to 30 email address that you want to license, stating that they all work in your organization that thaty they are not external users. We will add them to your license.\n\nThank you very much.\n\nWei

Thank you for quick and clear response. I believe I do understand your concern as well. Idea is to avoid abuse by reselling license to other random users etc. which completely makes sense. In situations like me, I can extend my team up to 30 emails for enterprise version. For my current needs, I believe 2 stacks should be sufficient. But since I love this, may be I should stack total 3 codes.

null Hi does it have workflow triggers such as email opened, replied, read, clicked etc? Hi thanks for your question. Logic Sheet works in Google Sheets, so it cannot monitor actions taken in Gmail. The only Gmail action Logic Sheet takes is to send an email when the automation is triggered in Google Sheets. Thanks. Wei

null I'm looking at importing orders and email lists from Shopify to Google sheets automatically and also data migration from one Shopify app to another. Are these actions possible? HI thanks for your question. Logic Sheet can only send Google Sheets data to other apps. But we have developed another tool Uniquery(https://uniquery.io/) that allows you to import data from third-party data sources including Shopify. It's not on platform but we do offer a special offer for platform customers. Please reach out to me if you have purcahsed Logic Sheet and I will send you the offer. Wei

null i have data in 2 Google sheet.\nCan it help to synchronise the data between two Google sheet under same account?\nlike if based on certain set of condition data is on main sheet it is updated on sheet a,some in sheet b and whenever there is update in sheet a or b it is updated in main sheet? Hi, this is possible with the "spreadsheet is edited" trigger with monitors updates in all tabs and then you need to set conditions in each action to monitor if the update happens in Sheet A or Sheet B, then the action can be set a new value or insert a new row in the main sheet. Please reach out to us via our live chat when you try to set up the workflow and I will provide more help based on details of your spreadsheet setup. Wei

Hi, to piggy-back on this question, what if we have 10 sheets from different sources: 1 parent + many sheets e.g. child a + child b and so on, can we merge specific changes and updates from the child to the parent master by columns/rows and control the data pulled in and (assume then set up the triggers, like emails and slack or Trello or whatever...) correct assumption what this can do?

null Please add integration to OpenRouter API, so that we can access dozen of other LLMs easily. Thank you very much!\nAPI Docs: https://openrouter.ai/docs/quick-start Hi, thanks for your question. Logic Sheet is not an AI tool. I assume you are inquerying about another of deal Power Formulas, please check it here\nWei

null Will all UTILITIES features in docs be supported currently? \nAs it's say UTILITIES (DEPRECATED) in help center, thank you.\neg. LogicSheetAPI() and LogicSheetMySQL(), LogicSheetImportWebElement(), Finance HI, I'm sorry for the confusion. The Utilites featuers are still available and we don't have plans to take them down. These featuers are also maintained and supported. Thanks, Wei.

null Can Logic Sheet be triggered when a row is added through an API? I use ManyChat, which integrates with Google Sheets. I want that, when ManyChat inserts a new row into the sheet, an HTTP POST request is made to another tool, sending some data from that newly inserted row in this request. Hi, thanks for your question. Yes, Logic Sheet has a trigger called "A new row is inserted(by an app)", which will trigger automations when a new row is added by an external app, including APIs. The workflow you described is perfectly doable with Logic Sheet. Wei

null Is it possible to Download Facebook leads automatic Hi thanks for your questions. Logic Sheet is not designed to download data into Google Sheets. But you can our new product Uniquery, which is capable of importing marketing data into Google Sheets automatically. Wei

null Hi, is it possible to upload and/or update products (with images, categories, descriptions, etc.) from Google Sheets to WooCommerce using LogicSheets? If not, do you have this on your roadmap? Hi, this is not what Logic Sheet is designed to do, it is an automation tool for you to automate workflows in Google Sheets. You can try to use the LogicSheetAPI formula to do this to send data to WooCommerce, I think this is possible but you need some knowledge of WP API. Thanks for your feedback.

Thanks for your quick response! Ah, I understand, makes sense! Still, we might look into it to see if it's possible.

null Do we need Google workspace for this or free Google account (Gmail) is sufficient for logic sheet,? Hi, you can use Logic Sheet both with free Gmail accounts and Google Workspace accounts. There is no limit on what type of accounts you have. The team and enterprise plans are for Google Workspace organizations tho.

null Hi there. If my google workspace has 1 domain and some  alias domain, could alias domain email users be counted unlimited in Tier4? Hi, yes you can do that. You can reach out to us after you redeemed your enteprise plan and we will add your alia domains to your enterprise license for free. Wei

null Hi Wei, this tool looks very interesting to me. \nCan we take prospect information from Wordpress website form (Elementor form/ Formaloo form / Google form / LeadPal) to google sheet and trigger a welcome/onbaording email via Vbout /Acumbamail /Mailer lite\nCan it add user to group in mailerlite using name/ email from Google sheets?\nThank you! Hi, this is possible with Google Forms, because Google Forms can send the form data directly to Google Sheets, then you can use Logic Sheet to trigger automations based on form submisssions. In the automation you can trigger HTTP Requests to send API calls to services like Vbout and Mailer lite to send welcome emails. Via API, it can also add user to a group in mailer lite using email and name data stored in Google Sheets. Wei

null I create templates in google sheets, when someone makes a copy of them and completes part of the template if I wanted it to trigger an email, is it possible to do that from each copied version? Hi, copying a template can't trigger an automation. Google Sheets doesn't support this kind of trigger. Currently the only available triggers are based on edits, time, or for submission.\n\nWei

null I'd like to use LS in conjunction with another extension, SheetsFinance, but I'm concerned that they will conflict with one another? Can these two extensions play well together? Hi thanks for your question. Currently there is no known conficts of Logic Sheet with other Google Sheets extensions, and there is no reason why there will be a conflict. So please don't worry about this. Also, if there is any technical issues when you use Logic Sheet you can always reach out to us and we will fix it ASAP.

null Hi Wei, Are you planning to connect Logicsheet with Google Chat? If yes, when can we expect it to be ready? Thank you! Hi, this integration is not on our road map yet but we can add it. May I know what is your use case and what kind of action do you want to automate?\nThanks

We don't use Slack; we prefer using the Google platform exclusively and use Google Chat for our operational communications. It would be great if we could receive notifications in our Google Chat spaces.

null Let's say that on our site we are running a form to collect contact info and that info is sent to our google worksheet.\n\nIs it possible for this tool to see a new row was built when a new lead comes in- then we send the lead through a webhook to our email marketing software?\n\nIs this possible? Hi, yes, this is a very popular use case of Logic Sheet. You can use the HTTP request action to send data to your email marketing tool. May I know what email marketing tool you are using? We may have an already made integration or template.

null Hi Wei,\n\nIs Build part on the deal ?\nhttps://logicsheet.co/build\n\nThank you Hi, this is not part of the deal. Logic Sheet Build is our service where we offer custom coding to clients and we charge customers by hour(€75 per hour). This is more like a consulting service. It just shares Logic Sheet’s brand name and operated by LogicLabs OÜ(the company that owns Logic Sheet). I hope this is clear. Let me know if you have more questions!

null Can I store links, images, PDfs, attachments, video files, audio files inside your tool and it triggers to send it via email or SMS like when people fill out a form or purchase a product (digital) or request via SMS/email? I have full-stacked PowerFormula and Magic sheet.    Thinking I have overlap have PowerFormula and MagicSheet.  Trying to decide which is better for digital product sending and article creation. Your  product different how?  Thanks Hi thanks for your question, but this is the listing page for Logic Sheet, not Power Formulas. I understand your concerns tho, I'd say Power Formulas now supports all OpenAI models and supports connection to any API and SQL databases. Also, regarding your question about sending digital products after people fill out a form, this is possible with Logic Sheet. We already have users doing so. But the sending email action cannot include attachments like PDFs or Video files. It is only possible if you store them somewhere else and send the link via email. It is also possible to send emails via APIs like SendGrid that supports attachment, but it requires knowledge of API connection. Let me know if you have more questions! Wei

null What is the future of Logic Sheet? How do you plan to grow? I would like to invest but if I invest big I would hate to loose my money because the company went out of business.  \nDoes you tool place everything on my end? \nAre you housing anything that would increase your server cost do to the unlimited LTD? Hi, great questions. Logic Sheet is a software company, and we’re committed to the development of a diversified range of software products within the Google Workspace ecosystem. Our current product lines have not only been well-received but are also generating profits, indicating our positive trajectory and long-term stability.\n\nOur strategy for growth includes:\n\n- Expanding Product Lines: We are continually working on new tools and features that integrate with Google Workspace. Our goal is to simplify and enhance productivity for businesses of all sizes.\n- Custom Solutions: Through services like Logic Sheet Build, we offer bespoke coding solutions tailored to individual customer needs, further establishing us as a go-to resource within this ecosystem.\n- Customer-Centric Development: We actively seek and incorporate user feedback to ensure our products remain relevant and valuable.\n\nRegarding your concerns about the operating costs. Logic Sheet operates primarily on Google Apps Script, hosted by Google Sheets. This setup is akin to running software on your local device, significantly reducing hosting and operational costs on our end. While we do utilize some microservices on AWS to support Logic Sheet, these costs are manageable and do not scale uncontrollably with user growth. This cost-effective model allows us to offer a sustainable and profitable service.\n\nI understand your concerns about server costs, especially concerning our Unlimited Deal. Rest assured, the majority of Logic Sheet’s functionalities run on Google’s infrastructure, ensuring that we don’t incur substantial server expenses. This model helps us maintain competitive pricing and longevity in our services without compromising on quality or stability.\n\nPlease let me know if you have more questions or concerns!\n\nWei

null Can you use this to create a macro or to separate data in the columns? I get data in three different formats that need to be separated. HI thanks for your questions, but I'm afraid I couldn't understand what is the problem you want to solve. But Logic Sheet cannot be used to separate data into columns. This is a feature that is already provided by Google Sheets. We try to not repeat what Google Sheets already is capable of. But if you have another question, please feel free to reply to this thread. Thanks!

null Hi Wei, this tool looks very interesting. Can it register a user on a specific Lifter LMS (my wordpress course plugin) course using name/ email from Google sheets? \nCan it add subscriber to group in mailerlite using name/ email from Google sheets? \nThank you! Hi, this is only possible if the WP plugin you use supports API connection. For the MailerLite integration, yes, you can connect to it with its API, using Logic Sheet's HTTP Request action. Please see Mailer Lite API docs for more details. https://developers.mailerlite.com/\nWei

Hi, this is only possible if the WP plugin you use supports API connection. For the MailerLite integration, yes, you can connect to it with its API, using Logic Sheet's HTTP Request action. Please see Mailer Lite API docs for more details. https://developers.mailerlite.com/\nWei

null Can  it link with Monday's? Hi, Monday integration is on our development plan, but currently you can send data to Monday.com via their API. This is very easy to do with our HTTP Request action. Wei

null I’m looking to automate the workflow so that when a new form response is received and a new row is added to a sheet, the sheet will conduct a column sort action by the first column which is the Date field. Is this possible? Hi yes, this is possible. You can use the Form response trigger to trigger the automation and choose the Sort Sheet action. The Sort Sheet action can sort a specific sheet/tab by a column, in ascending or descending orders.

null Can we send sms? Hi you can use the HTTP Request action to send an API request to SMS service providers like Twillo so send SMSs automatically.

null Hi! Can i generate pdfs from a google sheets file? Hi we are developing this feature to generate PDFs from GOogle Sheets and save them in Google Drive or send it as an attachment in emails. It will be available soon. Thanks!

null could I use this tool to automate domain purchase, inbox setup, moving nameservers to cloud flare, setting up dns settings etc. Is this possible? Hi, I don't think this is possible, Logic Sheet mainly focuses on automating workflows in Google Sheets. It doesn't seem that any of these actions happen in Google Sheets. Thanks!

null Hello Wei\_Sheng,\n\nWhat is the response time for messages sent to you through Intercom on your websites? I wrote to you 2 days ago and have not received a response yet.\n\nBest regards,\nFlorence. Hi, the live chat on our website is for existing customers to resolve technical issues. I just checked your message and it's about feature inquiry. Please email help@logicsheet.co if you want to inquire about whether your use cases are achievable. Thanks. Wei

null "License unlimited Google Sheets accounts in the same Google Workspace domain"\n\nWhat does this mean? I am ready to buy the Enterprise Plan cos unlimited but what does this mean exactly?\n\nCan anyone explain? Hi, thanks for your question! The Enterprise Plan is for Google Workspaces and it gives all users in one organization access to Logic Sheet. Since Google Workspaces all have domains, the licenses are distributed to all users under the same licensed domain. For example, if a company XYZ has the domain xyz.com and buys the Enterprise Plan, all its employees, for example, john@xyz.com, dave@xyz.com, will automatically have access to Logic Sheet. Hope this explains! Wei

\
\
\


Introduction to Logic Sheet

Manually doing time-consuming and repetitive tasks every day is frustrating. Why not automate the boring stuff and find more time in your life?

\


Learn how to use Logic Sheet to save your time and boost productivity by automating repetitive tasks in Google Sheets.

\


Set up a single automation workflow, and let Logic Sheet do the work for you. Logic Sheet is a Google Sheets add-on that helps you automate your work. For example, you can set up automation workflows to let Logic Sheet send an email notification or send a Slack message when your spreadsheet is edited.

\


What you can do with Logic Sheet Automation:

\


Listen to triggers like spreadsheet edits, form submissions, or run automations hourly, daily, or weekly

Set up conditions for each automation workflow

Run automatic automations like sending email/Slack, updating sheet data, Notion, Airtable, or HubSpot etc.

Use merge tags to refer to dynamic data in your message

\
\


You can also create automations within one click with our pre-defined templates and recipes.

\


Triggers kick off your automation. You can choose from various types of triggers that put your spreadsheets on autopilot.

\


Currently, we support the following triggers:

\


Time driven: Run automation hourly, daily, weekly, or monthly

\


Form submission: Runs the automation when a Google Form submission is received

\


On-edit trigger: Runs the automation when the spreadsheet is edited. You can set your automation to listen to events like a certain row, column, or range is edited.

\


Webhook: Turn your spreadsheet into a webhook, receive HTTP requests, and trigger automations.

\
\
\
\
\


null

Run automations conditionally.

Only run automated workflows when all conditions you set are met.

\


You can use dynamic data in conditions. Like, only run the automation when the content in cell A10 is larger than 100, or when the form submission's value contains a certain word.

\


null

Run automations conditionally.

If the workflow is triggered, Logic Sheet will run automated actions, like sending an email or a Slack message.

\


Actions you can do now:

\


Send emails

Send Slack messages

Update your spreadsheet

Update Airtable

Update Notion database

Send contact to Hubspot

Subscribe user to Mailchimp

Grant or remove access to the spreadsheet

Remove rows from the spreadsheet

Refresh formulas

Send HTTP/API requests

\
\


Actions coming soon:

\


Add Google Calendar event

Update CRMs like Zendesk, Salesforce

Post on social media like Twitter, Facebook, or LinkedIn.

Create tasks in project management tools like Asana or Trello

Generate invoices based on spreadsheet data

Integrate with e-commerce platforms like Shopify or WooCommerce

\
\


For more features in the pipeline, please take a look at our product roadmap.

\


null

Create automations from templates and recipes.

Simplify your automation journey with Logic Sheet's template gallery, a curated collection of pre-defined templates and recipes designed to cater to a variety of tasks and industries.

\


Explore a diverse range of templates tailored for different needs, from project management and data analysis to customer relationship management and beyond. Each template is crafted with industry best practices in mind, ensuring that you can leverage the power of automation without the need for extensive configuration.

\


Harness the collective knowledge of the Logic Sheet community and our dedicated customer support through the "Import from Recipe" feature. Share automation recipes with fellow users or import ready-made solutions directly into your Logic Sheet environment.

\


Importing automation recipes becomes effortless as you can simply paste the shared recipe, allowing you to replicate proven workflows with just a few clicks. Benefit from the collective expertise of community members and our support team to accelerate your automation projects.

\
