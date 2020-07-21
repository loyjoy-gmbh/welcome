# How to transfer giveaway participants from LoyJoy to ProCampaign

## 1. What this solutions will do for you

LoyJoy lets you create a giveaway or raffle for your customers within the chat experience. Your customers will be asked to enter their email address in order to participate. 
In addition you can draw the winners on the platform and export them.

You can **automatically transfer your new giveaway participants to your ProCampaign database**. LoyJoy will forward the email addresses of your participants to ProCampaign.

## 2. What you need for this solution

To start transferring participants from LoyJoy to ProCampaign you will need three things - your ProCampaign administrator will help you with these:

 - The **Participation transaction name** in ProCampaign.
 - The **Participation list name** in ProCampaign.
 - The **API key that has the needed rights** to send the transaction.

## 3. Add the Giveaway participation process block to your chat flow

Create or copy an new experience and add the `Giveaway participation` process block. Also add the `Sign up`process block if your chat flow does not have one yet. The sign up process block collects the email adresses from your customers and is required for a valid giveaway participation.

<p align="center">
  <img src="giveaway/giveaway_process_block.png" alt="giveaway process block in LoyJoy" title="Giveaway Process Block in LoyJoy" width="600"/>
</p>

After adding the process block to your chat flow, close the process editor. The process block `Giveaway participation` gives you the opportunity to maintain multiple give aways organized by tabs. Use the `timer button` in the right corner to set different give aways for different days. You can decide how many times one customer can participate to your giveaway and set a date to automatically draw a winner from your participants. Also set the number of winners that should be picked.

<p align="center">
  <img src="giveaway/giveaway_1.png" alt="Give away process brick part 1" title="Give away process brick in LoyJoy" width="600"/>
</p>

The section `Confirm participation by email` lets you define a confirmation email send to your customer after participating for your give away. If you wish to send a confirmation email, activate the button. Here you can set a subject line and a message to your customers. Use the HTML template field to paste your individual design and brand the confirmation email due to your preferences.

<p align="center">
  <img src="giveaway/giveaway_2.png" alt="Give away process brick part 1" title="Give away process brick in LoyJoy" width="600"/>
</p>

The section `Send winner email` can be used to notify the winner(s) of your giveaway. Here you can configure the winner email to inform the lucky participants about their price.

<p align="center">
  <img src="giveaway/giveaway_3.png" alt="Give away process brick part 1" title="Give away process brick in LoyJoy" width="600"/>
</p>

The section `Other texts` lets you define the intro messages to your customers in the chat to invite them to sign up for your newsletter. Then you can define a post-participation message send in the chat to confirm the participation (here: Done. You are now entering the competition. I keep my fingers crossed. :crossed_fingers: :trophy:) You can also 
define a message in case your customer has already participated and you only allow one participation per person. 

<p align="center">
  <img src="giveaway/giveaway_4.png" alt="Give away process brick part 1" title="Give away process brick in LoyJoy" width="600"/>
</p>

Awesome! :tada: You just created your first giveaway in the LoyJoy chat. One more step to go!

## 4. Configure the data transfer

You completed all the configurations within the chat. Now you have to set up the data transfer.

On the LoyJoy platform, go to settings, then choose integration. Choose ProCampaign and click on "Add now".

<p align="center">
  <img src="pro_campaign_integration/pro_campaign_integration.png" alt="LoyJoy to ProCampaign" title="LoyJoy to ProCampaign" width="800"/>
</p>

This will add a new tab with the name "ProCampaign" below the cards.

Scroll down to "General settings".

Set a name for your integration (since you can have several integrations this will help you keep an overview).
Enter **your API key** that you got from your ProCampaign admin.

<p align="center">
  <img src="pro_campaign_integration/procampaign_api_key.png" alt="LoyJoy to ProCampaign API key section" title="LoyJoy to ProCampaign API key" width="800"/>
</p>  

Scroll down to the section `Fields for giveaway participation`. Now fill in the **Newsletter list name** and the **Newsletter transaction name** into the according fields in LoyJoy. The field Participation privacy is not required and meant for special cases (to transfer the privacy attribute).

<p align="center">
  <img src="giveaway/api_giveaway.png" alt="LoyJoy to ProCampaign API giveaway section" title="LoyJoy to ProCampaign API giveaway" width="800"/>
</p>


Scroll down and activate the integration for your bot in the field "Choose on which bots the integration should be active". Click on "Add a mapping" to create a mapping for the email field. Then choose `process variable` and type in **customer_email** to refer to your data field in your chat flow. Now just type in the source name of the data field in ProCampaign **Email**.

<p align="center">
  <img src="newsletter/procampaign_newsletter_customer_email_api.png" alt="LoyJoy to ProCampaign API newsletter section mapping" title="LoyJoy to ProCampaign API newsletter mapping" width="800"/>
</p>

Congratulations! You just have successfully connected your LoyJoy chatbot with ProCampaign and all giveaway participants within the chat will automatically tranferred to ProCampaign.:tada:
