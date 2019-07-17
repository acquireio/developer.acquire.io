# Dialog Flow Fulfillment & Custom Response

Sometimes we have to call web-hook on Dialog Flow, where we want details of visitor, like: **name, email, hash value, browser details** etc.  so these details shared by “Acquire”, are accessible only in “**Fulfillment**” section.

In Fulfillment, we write our code as we want it to function and then link our function into a particular intent. So whenever we ask particular question, dialog flow assistant will hit that Fulfillment function and give us response accordingly.

Let's build a function and link it with an intent. 

### **Make An Intent**

First of all we have to make an intent like “get premium amount” with the question “what is my premium amount”. Now we enable the “Fulfillment” for it.  

![](https://lh5.googleusercontent.com/kA1FCezBUn3QqAY8VIK14zt5zl8FWVj1SHTVUcTimUJgyIcK0ol9FYLyKuI-HFqplPhl30mqiWKy-g3_3ZXqj0-vBRb6z1EJUoLJOGPnVii-zimJxlCmR5h9Yw08M-4ZQOl9VUYF)

### **Fulfillment Code**

Here we set Bot responses as we want. We can develop or write our custom code here, like calling of a web-hook, make a calculation, etc. First of all, we make a function handler here named as ‘**getPremiumAmount**’. 

In this handler, by use of **request.body.queryResult.outputContexts**, we get all the details of visitor. then we do our code and get premium amount of that client. and pass this resultant output to the Bot by putting **agent.add\('Your premium amount is $' + premium\_amount\);**. 

After creating this handler we map this function with a intent like: **intentMap.set\('get premium amount', getPremiumAmount\);**.   By this way we can manage intent response by our own.

![](https://lh5.googleusercontent.com/0r4ZPxzjmxfnz1c-55BFuLP3hz4oIENNqjKHiVZADlV0_kChzfhNASWeywDgplb_wyuDiLvSXqZ35Y3YCeP4iWRChKl_K6_y2xlt6w12aVL9884TA8vFeHw4SaWBfSSMCAwh8VmS)

 Now let we check it by asking to Bot this question.  
****

![](https://lh4.googleusercontent.com/E4xGOpyCXoC5MEUQoHX6CDkmx6G42k3giO_iojIrhlpbQuP7t7UVPsVOOD-T6xNamEXCEt171Te1R8wTs0zQFJg1KxMFRwYN06_shUpKfcgFuw3rXFvSHYLpY-PrRXQvx6VKiqCT)

