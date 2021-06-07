# Getting Started

Acquire uses two types of webhook events: 

* **Inbound** - collects information from outside sources to be displayed within Acquire. Works with chatbots and during live chats.
* **Outbound** - collects information from within Acquire to be displayed in outside sources.

### Inbound

Once you've configured an inbound webhook in another system, you’ll need to create a reference to it in Acquire. To create a new webhook, go to **Settings &gt; For Developers &gt; Webhooks** and click on the **‘Create Webhook’** button.  
  
[![3zk0ZP84f0U7G1sEpKw995NNpUU4cmAxrI6O-oiqEx0\_\_5AUxzUJ-BOG\_H3mhm28LLBMsZb5Rm7YvhhBYDDLd-YFdw6BHvUC6WNcdOa0i68gNdL7\_d5S7sfrnS4WQcK375uLJfCE](https://lh6.googleusercontent.com/3zk0ZP84f0U7G1sEpKw995NNpUU4cmAxrI6O-oiqEx0__5AUxzUJ-BOG_H3mhm28LLBMsZb5Rm7YvhhBYDDLd-YFdw6BHvUC6WNcdOa0i68gNdL7_d5S7sfrnS4WQcK375uLJfCE)](https://lh6.googleusercontent.com/3zk0ZP84f0U7G1sEpKw995NNpUU4cmAxrI6O-oiqEx0__5AUxzUJ-BOG_H3mhm28LLBMsZb5Rm7YvhhBYDDLd-YFdw6BHvUC6WNcdOa0i68gNdL7_d5S7sfrnS4WQcK375uLJfCE)

Provide a new name for your webhook in the ‘Webhook Name’ field. Then, select **Inbound** in the ‘Webhook Flow’ section. 

Next, set your format, status, and security preferences as well as an email address. Should your webhook fail, a notification will be sent to the email address provided.  
[![Y4HOdBdM5r5CyV2OzfcQD\_vxo3LzT1ukJ1iknqufwysDTTmHKJoavUweKcMQiJptWIm0tG0fAz\_gzCp-JxemrKBn\_uTI-qcruz9KCg82sGBWIGGJtVtZ2ciQKn2A4qfld9sXR1Wt](https://lh6.googleusercontent.com/Y4HOdBdM5r5CyV2OzfcQD_vxo3LzT1ukJ1iknqufwysDTTmHKJoavUweKcMQiJptWIm0tG0fAz_gzCp-JxemrKBn_uTI-qcruz9KCg82sGBWIGGJtVtZ2ciQKn2A4qfld9sXR1Wt)](https://lh6.googleusercontent.com/Y4HOdBdM5r5CyV2OzfcQD_vxo3LzT1ukJ1iknqufwysDTTmHKJoavUweKcMQiJptWIm0tG0fAz_gzCp-JxemrKBn_uTI-qcruz9KCg82sGBWIGGJtVtZ2ciQKn2A4qfld9sXR1Wt)

Paste the webhook URL. Once pasted, you’ll see a list of the available variables.   
[![ecbijG0r4UzXAbTUGeftAIhrngvTQQs7umWwPHVr4pQxazFN3wHSLsofRRJirwqDP9\_nBmFNQ7RWVQzbh8m7Wz-pPvkCoIOjA61HVAKd3\_i6up8jjgcXalb8whSuyewciZAgv8cD](https://lh4.googleusercontent.com/ecbijG0r4UzXAbTUGeftAIhrngvTQQs7umWwPHVr4pQxazFN3wHSLsofRRJirwqDP9_nBmFNQ7RWVQzbh8m7Wz-pPvkCoIOjA61HVAKd3_i6up8jjgcXalb8whSuyewciZAgv8cD)](https://lh4.googleusercontent.com/ecbijG0r4UzXAbTUGeftAIhrngvTQQs7umWwPHVr4pQxazFN3wHSLsofRRJirwqDP9_nBmFNQ7RWVQzbh8m7Wz-pPvkCoIOjA61HVAKd3_i6up8jjgcXalb8whSuyewciZAgv8cD)  


Set a fallback JSON response under “Fallback response, when webhook URL fails”. The system will try to get a response from the original webhook URL three times. If the system does not get a valid response by then, It will send the fallback response.  
[![5vwKFle5g0Jy4mNwIX9v5we5\_hT3KufFSe3xoGuHkRhKBajPvqWKUCRg5Ewg1VyJELH1COPl\_WwiH5CSEU0gJGIuSW7KZwjcOxBdLkV37ZWDNhlXCJlsyHVX-cQEt\_yB0xFUPyr6](https://lh3.googleusercontent.com/5vwKFle5g0Jy4mNwIX9v5we5_hT3KufFSe3xoGuHkRhKBajPvqWKUCRg5Ewg1VyJELH1COPl_WwiH5CSEU0gJGIuSW7KZwjcOxBdLkV37ZWDNhlXCJlsyHVX-cQEt_yB0xFUPyr6)](https://lh3.googleusercontent.com/5vwKFle5g0Jy4mNwIX9v5we5_hT3KufFSe3xoGuHkRhKBajPvqWKUCRg5Ewg1VyJELH1COPl_WwiH5CSEU0gJGIuSW7KZwjcOxBdLkV37ZWDNhlXCJlsyHVX-cQEt_yB0xFUPyr6)

The “Available Variables” section will list variables if system identifies the variables from the URL response, if it does not list any variables you may add your own variable

To add custom variable names, click on the **‘Add more variables’** option. 

\(You'll need to do this when using more than one special webhook\).  
  
Then, press on **‘Create’.**

Your inbound webhook is now ready!

### Outbound

Once you've configured an inbound webhook in another system, you’ll need to create a reference to it in Acquire. To create a new webhook, go to **Settings &gt; For Developers &gt; Webhooks** and click on the **‘Create Webhook’** button.  
  
[![3zk0ZP84f0U7G1sEpKw995NNpUU4cmAxrI6O-oiqEx0\_\_5AUxzUJ-BOG\_H3mhm28LLBMsZb5Rm7YvhhBYDDLd-YFdw6BHvUC6WNcdOa0i68gNdL7\_d5S7sfrnS4WQcK375uLJfCE](https://lh6.googleusercontent.com/3zk0ZP84f0U7G1sEpKw995NNpUU4cmAxrI6O-oiqEx0__5AUxzUJ-BOG_H3mhm28LLBMsZb5Rm7YvhhBYDDLd-YFdw6BHvUC6WNcdOa0i68gNdL7_d5S7sfrnS4WQcK375uLJfCE)](https://lh6.googleusercontent.com/3zk0ZP84f0U7G1sEpKw995NNpUU4cmAxrI6O-oiqEx0__5AUxzUJ-BOG_H3mhm28LLBMsZb5Rm7YvhhBYDDLd-YFdw6BHvUC6WNcdOa0i68gNdL7_d5S7sfrnS4WQcK375uLJfCE)

Provide a new name for your webhook in the ‘Webhook Name’ field. Then, select **Outbound** in the ‘Webhook Flow’ section. 

Next, set your format, status, and security preferences as well as an email address. Should your webhook fail, a notification will be sent to the email address provided.  
[![Y4HOdBdM5r5CyV2OzfcQD\_vxo3LzT1ukJ1iknqufwysDTTmHKJoavUweKcMQiJptWIm0tG0fAz\_gzCp-JxemrKBn\_uTI-qcruz9KCg82sGBWIGGJtVtZ2ciQKn2A4qfld9sXR1Wt](https://lh6.googleusercontent.com/Y4HOdBdM5r5CyV2OzfcQD_vxo3LzT1ukJ1iknqufwysDTTmHKJoavUweKcMQiJptWIm0tG0fAz_gzCp-JxemrKBn_uTI-qcruz9KCg82sGBWIGGJtVtZ2ciQKn2A4qfld9sXR1Wt)](https://lh6.googleusercontent.com/Y4HOdBdM5r5CyV2OzfcQD_vxo3LzT1ukJ1iknqufwysDTTmHKJoavUweKcMQiJptWIm0tG0fAz_gzCp-JxemrKBn_uTI-qcruz9KCg82sGBWIGGJtVtZ2ciQKn2A4qfld9sXR1Wt)

Paste the webhook URL. Once pasted, you’ll see a list of the available variables.   
[![ecbijG0r4UzXAbTUGeftAIhrngvTQQs7umWwPHVr4pQxazFN3wHSLsofRRJirwqDP9\_nBmFNQ7RWVQzbh8m7Wz-pPvkCoIOjA61HVAKd3\_i6up8jjgcXalb8whSuyewciZAgv8cD](https://lh4.googleusercontent.com/ecbijG0r4UzXAbTUGeftAIhrngvTQQs7umWwPHVr4pQxazFN3wHSLsofRRJirwqDP9_nBmFNQ7RWVQzbh8m7Wz-pPvkCoIOjA61HVAKd3_i6up8jjgcXalb8whSuyewciZAgv8cD)](https://lh4.googleusercontent.com/ecbijG0r4UzXAbTUGeftAIhrngvTQQs7umWwPHVr4pQxazFN3wHSLsofRRJirwqDP9_nBmFNQ7RWVQzbh8m7Wz-pPvkCoIOjA61HVAKd3_i6up8jjgcXalb8whSuyewciZAgv8cD)

