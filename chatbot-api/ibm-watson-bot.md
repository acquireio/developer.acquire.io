# IBM Watson Bot

## **Getting started tutorial**

This guide will allow you to integrate the Acquire platform with IBM Watson

### **Before you begin**

A Watson service instance must be started first.

1. [Sign up](https://cloud.ibm.com/catalog/services/watson-assistant) for a free IBM Cloud account or [log in](https://cloud.ibm.com/catalog/services/watson-assistant) with your existing account.
2. Load the [Watson Assistant](https://cloud.ibm.com/catalog/services/watson-assistant) page in the IBM Cloud catalog.
3. The Watson service instance will be created in the default resource group. Please note if you wish to change the resource group change it at this stage as it cannot be changed later. However, this group is sufficient for the purposes of exploring the Acquire chat bot integration.
4. If you're creating an instance for production use, which is more robust, then learn more about [resource groups](https://cloud.ibm.com/docs/resources/bestpractice_rgs#bp_resourcegroups).
5. Choose an appropriate region/location to deploy your instance in.
5. Click Create.

![](https://lh3.googleusercontent.com/Aua6808g3upgWlAw2BULxzvMLrD2SBRh4-gvQjym2cLe4nuIx3ljhnSIDFjmpTd1wW30Svw7dCd1ebBbQn0Iz0fRzc6f9otXn3HUccm6sLDhPIQkCqqb19VSCd6XTpzQ-IaW8MCd5Uwmov_0SWBTpbZnPEsMz0apO93bjqAQ-bCwDaPb-2RkmG7T1bdhI5OsGAUmKqbf0-jiZ7kgOEp4iBcQ78juzn-8CHeOxo6uGqnVlPbUqF8jMETLIEin2e4_sCzg45xcTHIDrCYzCJWRHuIWAY11dwKKrPjJajtrT0qGjv31w5lpmXgmtW_McWBBuCJodnuH7uT6euAoKNBTlkYb4f6j-8hdWfTNGT8XUvkjcMh7v4ou4Use52EdqbrBMRHKfthlgqw-jpiLEu9-qpKgToWBCyt8cHzOaVjNg6owIMWBlzIBFFzmcOtHHkEZ2hkLfiR5vvLs49iEurwyt9xqLdUgHuYMT7yUj7ds7PyT0hOD146t9JXpZntIcfdth7msyzjjQzwhzewTNLKqz-9zdHE-22D3trwtmGH14zQD4xvAiTzMcQjHTs45_3hxUHrbCtvlFGERtEBdYAzIgmbWh_YqZVeefznaryiBqZTzD6kwDwHq4NhO1-jKYdIPQAN0NVaYi29d-Zypf1J211qz3QK2UXE=w850-h700-no)

### **Step 1: Open Watson Assistant**

After creating a Watson Assistant service instance, the Watson Assistant dashboard will appear and allow you to manage it.

1. Click Launch Watson Assistant. If you're prompted to log in, provide your IBM Cloud credentials.

![](https://lh4.googleusercontent.com/V2cnR7LPsdxdsKX1sYV3-X37nDGBx1UW6z-z3LOR2pZJN_imo4IKxu4YKgplFOiDBLfdAuSfiNaBngu1b1fonlB6XtT58NKmw0F-b4-vGARCSmRCC1k_7aAzbbhtvXiFFWpDM0-Y)

### **Step 2: Create an assistant**

1. Click Create assistant to add an assistant.

![](https://lh5.googleusercontent.com/GEN_2PrCwEr0pZP-NUL9Pce-cEZiSJ46n_u2SNh8955OrbXJjFE5D4uPn8Jrp4V9UK4qbJqnZZE3UL0D8Vdq_DYCqriAL2X8ezjr9iyebLK_FZrmx5aiMsY1Kn1IQCRKaECjrx1B)

   2. Click Create assistant.

![](https://lh3.googleusercontent.com/hyXA7Kd_RR2PFC-_rRQlcrxH1VdNYLCY9eTVtkzruNCxb95RgmNfoaDcZ8moziwSKCJGCpD28DaJyFbcJKQXbdKXiM2vO4jQ7uzRL38ApOxeg174_5f3plyEGcnuUn5-EN14yCu2)

### **Step 3: Create a dialog skill**

A dialog skill is a container for the artifacts that define the conversation flow that your assistant make use of to engage with your customers.

1. Click on your assistant tile to open the assistant.
2. Click **Add dialog** skill and **Create dialog skill**.

![](https://lh3.googleusercontent.com/kYeIrKz8stOHsPzHxFTkREKZo-1Dr0cVvMnjEEAmglnAwOc94_6Yiauzfhf8hYjJ6l2Nniq30HcW7YjsNadgkB_gcncljrzIOE7163ldLrLy5cne2t4SD4PUVFY6jKccSt0n5N1o)

You will then land on the Intents page.

### **Step 4: Add intents from a content catalog**

Add training data that was built by IBM to your skill by adding intents from a contents catalog. In particular, you will give your assistant access to the Generalcontent catalog so your dialog can greet users, and end conversations with them appropriately.

1. Click the Content Catalog tab.
2. Search for the General option from the list, and then click Add to this skill.

![](https://lh4.googleusercontent.com/NIR_ENHcUklUoq66x8G1UPYvx5TONSJbvJGksZ7gpJ4BGeyXHvKDo789mCSxuemUGMzIzSBu9w5zmmv5oFrprOoil4EoCDE2wkVkRhszXMQ6Rl82d1hM8PV-y-LwuSPoHbHGDXeL)

You successfully started to build your training data by adding prebuilt content from IBM.

### **Step 5: Build a dialog**

A [dialog](https://cloud.ibm.com/docs/services/assistant?topic=assistant-dialog-overview) defines your conversation flow in the form of a logic tree. It matches intents \(what users say\) to responses \(what the bot says back\). Each node of the tree has a condition that triggers it, based on the user's input.

We'll create a simple dialog that handles the greeting and ending intents, each with a single node.

#### Adding nodes to handle intents

Now let's add nodes between the Welcome node and the Anything else node that handle our intents.

1. Click the More icon on the Welcome node, and then select Add node below.

2. In the If assistant recognizes field of this node, start to type \#General\_Greetings. Then, select the \#General\_Greetings option.

3. Add the response text, "Good day to you!"

4. Click ![](https://lh3.googleusercontent.com/OaAmaCA_hbERAAb-dqAgDKTOT31NiCqxSBuLYh_MBWmNJ407RJUGEjlQ1_tRIirsQW_Li6nlx2GF0m9rdE2GmnI-lM5m--Vryo6zqNwJ_8QFc9PSd3Oca93Z6vyQndxg_E9xNY-1)to close the edit view.

![](https://lh5.googleusercontent.com/eP5oIzSpg_Si18lBTmU_olFeVusb3F9-3Xv2hQyOMAe41I4C5jS2oTTFQEDXKTDerSq92NnPVUiJe28_up42_L6Oj9Eh4f-y4eIs70TNObCcbkYMHzO_Rd89LyjYrz5sV-jlz0B4)

5. Click the More icon on this node, and then select Add node below to create a peer node. In the peer node, specify \#General\_Ending in the If assistant recognizes field, and OK. See you later. as the response text.

![](https://lh5.googleusercontent.com/goHV-FhUVeaCvpcFBEbmpg7qAcoqaW9FBUTgShYcHIAtPR8yPgtWk825JSRHg-GsmEqCu4Lmu5k8vITp5v7ouTt75Rt4t9BBQl8KZiXl-LWahu7czPjyIYS0tK_J_8x16gsAfola)

  ****6. Click ![](https://lh3.googleusercontent.com/we3BBvivTN5ACVkhGuDHA_0ywiV_LFclRdlsEGqm7RbopbsTd_ALd8TAqrcUvBMqPBBLmMxVnmIiQRk5W5f53pAtHZflsFWqNQoB_p01d9UmETO1wTytxZgoDbCSqo7O1aeHoS-Y)to close the edit view.

### **Step 6: Integrate with Acquire**

Go to Acquire’s Bot Section, here you can see all the third-party chat-bots along with “IBM Watson Bot” in this list.

![](https://lh3.googleusercontent.com/FTjDYSfnHQ2JQEvVgD0dR5rpcDeEMLQ0zggE2pm60Cdlj2sJ4F7YsVCnMeitnet1jSeMMnpocSex8zAtP8YB-ihOX0U7cStQA-cg3-VULlT7hnHKCpG_jFospC1_7poeIxE_WfWa)

1. ****Click on that and a popup will be displayed. You need a few parameters \(i.e. “apikey” , “url” and “assistant\_id”\) to bind it with chat widget.

![](https://lh6.googleusercontent.com/VPNsKibjkyh3DooP_xZRdEfDWC8-U4r8sD54FafpY3ZLK1QKO0TIv5BossA3q9JZtwt_7SFXNwGEhp4iN_8s5dnDceAPYnDOEKBxicPFGAccbQWGetPxXSai5vZlNhDFiWm4wnKG)

 2. To get your “apikey” and “url”, go to Dashboard of [IBM Cloud](https://cloud.ibm.com/) and press on Services that is displayed. Click on Watson service,  It’ll navigate to IBM Watson Service Page. Copy your “apikey” and “url” and paste it to “Acquire” popup.

![](https://lh5.googleusercontent.com/jyefvpdFtE_LufCznEMb-9hqcg5VmQkfMlBgG4lSrpuqgjbsIoNdkds0yMyoSfldLfV69-LrmvLdQLcHBPSsQWOJgD3V-l3RSD3toBJxjOHhVWeTuVNJbkgG9xd_UhGDIhRGMaaQ)

3. To get your “assistant\_id”,  Click on Launch Watson assistant button. It’ll give you list of assistants.

4. Select More icon of your assistant and click on setting.

![](https://lh4.googleusercontent.com/bLYo1WX8z04O8YMduqYEmZQnNwh7fLV94EKMbBOmMLFxYaHmYp1vZgXSE6tDXT79FoqFDFsf2bvI9fzrJgapaBPbiayWzvnYTu7QithL50cHZrATu4tO9pnDIrowhHm-IfRzgV4J)

5. Click on API Details tab, Copy  “assistant\_id” and paste it to “Acquire” popup.

![](https://lh3.googleusercontent.com/a1wrJYQ3P6RU2elc-9wbfL1fSYGZntIWPkWYldvXN9t8EPUDAtImRGIwkOogc0QGGrSHCBnXUrx6XvK4lENrvqAk1VDIOrl9O7-LSgRFpUSgfT9KntBiG2TPDFy4-I2POaIQH-Ww)

6. All are set up, now we are good to go and press the install button.

![](https://lh5.googleusercontent.com/_Hi4m_6bUzhjRy-P1KfxexLc2IQWYUievKgG8beqAqPbIZzLVqCLabRbjnIdfmmfYDj4RdXb_oHkqwHinfKpKDuqgoErCQZkSGSYuOaka6RrYlbylSAVJBydVqOFd_9CE2k_7Gdf)

7. From “Trigger” section, apply it where you want. It will answer all your visitors’ queries.

![](https://lh5.googleusercontent.com/aCAiySLaqnZuF6YOF1oox8fxEM2YLy1uYEMRdXSxbZ5YFKKMSh-0l50qYkpdp9k6P37MPSvEBpCvVDIX7NzGWGZgq-RoRYtyq1bswYz6B-VxTNUky-lmE2VZa4Ky3sqcflFFWD__)

8. Finally, now you can navigate to your simulation page to test the new and improved Chatbot by entering the different types of questions that the system has been configured with.

![](https://lh6.googleusercontent.com/ldqqsEWZhoMwtgdSP9hAW4PIC9mxN_8Ec88TgWMXo4NDAUi1oy3ZKQnDQifK-7Niq9O8clARvHZ_7i7S90JJ1KPcrZJjF6vAKlk66I1bty8XFaO_HW50DxEG1dzku9cIoR8659P7)

