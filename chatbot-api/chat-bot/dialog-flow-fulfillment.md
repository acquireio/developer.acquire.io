# Dialog Flow Fulfillment & Custom Response

The following guide will help you build customised responses using the Dialog Flow dashboard. 

It may sometimes be necessary to capture visitor details such as the **name, email, hash value and browser details**. This helps information is only shared with “Acquire” and are accessible only by the  “**Fulfillment**” section. A web-hook can be created inside the Dialog Flow to help capture this information.

In Fulfillment, it is possible to create functions and then link them to a particular intent. In the event a particular question is raised, dialog flow assistant will trigger that Fulfillment function and provide a response accordingly.

### **Make An Intent**

First, create an intent such as “Get premium amount” with the question “What is my premium amount?”. Then under "Fulfillment" heading, select "**Enable the webhook call for this intent**".  

![](https://lh5.googleusercontent.com/kA1FCezBUn3QqAY8VIK14zt5zl8FWVj1SHTVUcTimUJgyIcK0ol9FYLyKuI-HFqplPhl30mqiWKy-g3_3ZXqj0-vBRb6z1EJUoLJOGPnVii-zimJxlCmR5h9Yw08M-4ZQOl9VUYF)

### **Fulfillment Code**

Here we can set the Bot responses as required. We can develop or write custom functions such as calling of a web-hook to perform any calculations, etc. 

First, create a function handler such as ‘**getPremiumAmount**’. 

Within this handler we can make use of the method **request.body.queryResult.outputContexts** to capture visitor details. 

Appropriate code can be written inside the function **getPremiumAmount**, as shown below, to calculate the premium amount for that client and the result can be passed to the Bot using the following method:

**`agent.add('Your premium amount is $' + premium_amount);`**

After creating this handler it can be mapped to an intent using the following method: 

**`intentMap.set('get premium amount', getPremiumAmount);`**

This allows you to manage your own customised responses as required.

![](https://lh5.googleusercontent.com/0r4ZPxzjmxfnz1c-55BFuLP3hz4oIENNqjKHiVZADlV0_kChzfhNASWeywDgplb_wyuDiLvSXqZ35Y3YCeP4iWRChKl_K6_y2xlt6w12aVL9884TA8vFeHw4SaWBfSSMCAwh8VmS)

The following shows how the conversation flows and triggers the appropriate fulfilment response using the custom function **getPremiumAmount**.   
****

![](https://lh4.googleusercontent.com/E4xGOpyCXoC5MEUQoHX6CDkmx6G42k3giO_iojIrhlpbQuP7t7UVPsVOOD-T6xNamEXCEt171Te1R8wTs0zQFJg1KxMFRwYN06_shUpKfcgFuw3rXFvSHYLpY-PrRXQvx6VKiqCT)

