# Amazon Lex Bot

**Introduction**

Amazon Lex is a service that provides Automatic Speech Recognition \(ASR\) and Natural Language Understanding \(NLU\) to build conversational models. Acquire now supports ‘Amazon Lex’ chatbot along with many other 3rd party chatbots. Amazon Lex can be installed and used easily alongside the Acquire Chat Widget.

**Quick Setup**

Amazon Lex Provides functionality to create multiple bots. Each bots can have multiple intents to add utterance-response pairs \(question-answer pairs\). You need to provide a set of parameters to integrate your **“Amazon Lex bot”** with **“Acquire Chat Widget”**.

Follow the simple steps given below to install the “Acquire Chat Widget” integrated with “Amazon Lex”.

**1.** Go to [https://aws.amazon.com/lex/](https://aws.amazon.com/lex/) to access **“Amazon Lex”** platform. Click on **“Get Started with Amazon Lex”** and follow the Sign In procedure or Sign up procedure \(if you don't already have an AWS account\).

![](https://lh3.googleusercontent.com/MhREm3s_1SPCD7CZWkQQXoVBYHX1yUJcpT-HkwdpuvsUFRqsqDthq5ZQrz9QYMuGZd-JBiX53aO0abagVJWP1LUShs8HWBfNkXQ53hbjR_K9HdxghV-99RgB7REZwVjMh1UzZOmh)

**2.** After logging in, you will be taken to a screen similar to the one given below. Click on **“Get Started”** . This will lead you to the Bot Creation Module.

![](https://lh6.googleusercontent.com/96R7IrsyfZf4xy7lntkSxT_j7MBWAt8_GIX1oImrivrsxXJJhpn1RBdp6pMJZ5BUNNQg1Se_51_-iVVoHbBAZ8ykba53fp9vLeOj6SLE2AsWOLxkad2LqNbz1_ZlLYv_RXa8a5iv)

**3.** Here, you can choose to use an existing bot from the **“TRY A SAMPLE”** options or you can create a custom bot by choosing to **“CREATE YOUR OWN”**. Sample bots have an existing set of intents. We will create a custom bot to understand the whole procedure.

![](https://lh3.googleusercontent.com/upEhSqHkrF6aHbKkm9tp1zSGxQmUc3SXfF_W2z29PekRYfP8k3rRARIfwK-XvNJuBtr6wUFiBp9E3prbDKyC8oahbl4vn1EDgK1NgUcU90y6bYp4bgpuuZNgGKjpy0RXI7m4oRHW)

**4.** Click on **“Custom bot”** and fill the details required. Provide a new bot name. The **“Bot name”** is one of the parameters that will be used to connect our **“Acquire Chat widget”** with **“Amazon Lex Bot”**. Fill all the other required details as per your preference and then click on **“Create”**.

![](https://lh5.googleusercontent.com/K8h-7snnqUR8KREm0vzL2NuoatfQk-fkhse9Cln1qgm4etpDE7iYwec4fpt_PTzErvovML6-c-i33YTYkFxvCWgcPTgfldYDYxtw_wmJ759UdcitieiirHyC4pqE3FLEp9Sc0PkJ)

**5.** Now, you will have access to the Bot Editor as you have created your first bot. Create a new intent using **“Create Intent”**. Give your intent a name and click on **“ADD”**.

![](https://lh5.googleusercontent.com/wmPT1Q2mF8Zb1XF6umO4jlXxR256jJ92tYqa1axNFTWd1yUhYEafZCjkDBIycM2orj9uXUkPsYwoIj_03CYJlZuSq-nqNrf-qr0ySXTzyxa_mlNFlQc_Uw-CENoUDgFzyHLmWgIb)

![](https://lh4.googleusercontent.com/T_BUi2uZePsEhu1NV0XDGGbAX4fV59XqTyK4U70o4QTH4o2QyR8wirjKAy80nWC3XnQoU6T8-NJ6zNJRq_5cgQUA7tk9Riis9M-qBvZl6cBVHe4XmLkbihKcq2DA8GeR3qkhL2Up)

![](https://lh5.googleusercontent.com/nNDCVGCEW5IS4G6r82gmLdaJPYHLY8yoAcAB9r3QPj6JPxK4yKDLl_85WSMQ5OCmKbogBf1FW_mxfr0iYMGoJ421eijSQmUPVx8vwPixWrbrTA_SG5kZmWu-vy4jUlKfMroemCAF)

**6.** Now, you are inside the editor of your newly created intent. You can add multiple user inputs \(questions\) into **“Sample Utterances”** and bot response into the **“Response”** section. 

![](https://lh3.googleusercontent.com/piUfIIn1J_yXSVoltqirRKKpJbY9cavn4ia_qRBNAru57ma7P2-lCId9XrEqiTItE8AU7e40tWL3BWE-nigbJUgR5Ug-4f_belQ6ekpbP_Q-q5QPMmRvrn4gs8992jRuYgNzs5N5)

**7.** Response messages can be in 2 different formats. \(a\) **“Add Message”** helps to add simple text messages and \(b\) **“Enable response card”** provides a card format, where you can add images. You can also add buttons as quick replies in these response cards. At least one simple text response is mandatory in order to enable the response card. 

![](https://lh6.googleusercontent.com/dx6iAXfUFDVEumOPAjuMobQZkJpOGZFekgUGr5PpVHpLYIhIquEWfx6WSjNwgx9pBUTIOYco8g4lW5VeuY9mpzJycuFm0Kc9hChNhWVABxvddB3X_Ci6WwvlRtKkuRKUwCyTbAvy)

**8.** Under the **“Add Message”** section, you may also choose **“Custom Markup”**, here you can also use webhook variables provided by the **“Acquire Chat Widget”** \(i.e. visitor\_name, visitor\_email, visitor\_phone , premium\_amount, etc.\)

![](https://lh6.googleusercontent.com/N8aZiskKm0Mw3rGTuMJI3UcRXxtHv-aNJjkf_YEMrmnj19EVO4aFlQzqPLYgv0YSNRpXnBKfhmnkovW14HAwwT-13-6fZ_pXKO3OWtPugeoVkJCEYAzpRlnV4VPA4gPV70YO4KwI)

**9.** Amazon Lex also provides some further customizable options as follows:

**\(a\). Fulfillment :** Always select **“Return parameters to client”** in order to connect your Amazon Lex Bot with the **“Acquire Chat Widget”**.

![](https://lh6.googleusercontent.com/Yz89vYS5lBLN4VSQyJmV9PNkyhme0zIneAGM-QkKvFqMEnNUuV29_pbmwOBWwd5MVaYUKorCstwyHIuyagK-27OW38ifi7PHfdbRQ3MlFiQMUVoX4-KGN6DrNUBjvViQtPrfMp-U)

**\(b\). Slots :** You can also prompt questions to the users and store user responses in the form of slot values. You can utilise **“Built-in slot types”** to store user inputs or you can create your own **“Custom slot types”** from the left sidebar of the Editor.

![](https://lh3.googleusercontent.com/YEeufDlU8ztcMZWOhZj9qHHqfnPUeuyT-OprAStMrgBK8iDJJKPzrrx8W3kI4LAa95RmRuNah0-TxPeai7pJ_hzsuyyu7mQTtjTYflwHjww-ErCOxl7FRyZ_N8F_-ialY24esjLN)

![](https://lh4.googleusercontent.com/KsWh_mB39aQDFpYL5c1ytDM5vRIp6E_xVQ0TWbfexnn_xZWW4C58yRam0Y7Yu6YBjPACgfYcXoBGPk8354pRkO3fbSb5P9P5YRXw1qzvemXh1sBInGx5de7UTFzFPS08jRxZdUg1)

You can also use response cards with **“Slots”** to collect information from users, as response cards can provide quick replies.

![](https://lh3.googleusercontent.com/7z_dIW1z05Z1OGLPQoBguZ19cysOCjUJ68FECLTubtwpgaiOH1v3XASVhVMFnMUAE6jLz-_v9FbjBERpTr7-P60-ue2sbtiWIlHohkpwdv8wz6599dFllZWdH9Uv_5pFM0PnwGHl)

![](https://lh3.googleusercontent.com/OMUCH38CfArGFGx-7WBRl1YBqWVcGhxtKySGwHHUsyN4FdRUhSWJa1cjkE4fCBC7Kke4r6CH780xBRiTbIMOD3V_ma8YVNsfIyb_y_f8yVft_rgXvNvDz0up4xINkiTm6ZlHWH7R)

**\(c\). Confirmation Prompt :** Here you can confirm user inputs by asking an additional question to the user. You can also set a message prompt to display when users deny the confirmation.

![](https://lh5.googleusercontent.com/Ou9qkAgvforH8TZ_WYCjF4NxcchcGtN299_Sr-PmvoOlOPtBP4V-nUdmjFF_yxRQaWRxVFf66aY9-Hy3v0koj7X1mQE7FnHcvqkSLITKQcXWihVdlomtnuiLDKJgcCG31RejSxXn)

**10.** Once you have created your intent, you need to click **“Save Intent”** and then **“Build”** the bot.

**11.** If the build is successful, you can publish your bot to be used by the **“Acquire Chat Widget”**. You will be asked to create a new alias to publish your bot which is known as **“Bot alias”**. Then click on **“Publish”**.

![](https://lh4.googleusercontent.com/b0fO0tHdhqvhwRciR9fqWN8Nde0Ek0ypH0cQJw1hp-1et-mRLPsKJyzQZs0trklfvFLD4A6Bt6_i591BIGcUugji9q7HpIUd-vzkfNdIgBlXjFsyNSgk3hQrCR5uifAX3r3mY9vj)

![](https://lh3.googleusercontent.com/opgeZMBQ2wYG9yeDXmRrmGtJ3v7EJxkiuAjxhK8HaI4FeBZyrYM79jy8hN-Blh5sr0kzAkhxdF8TyIbCZBGbciYvt1l-zM-1GHJJJt0RIfpylVrWDXUG1CagEBIsC_Ntg6oyKhDR)

**12.** Now, you need to collect all the parameter values in order to integrate your "**Amazon Lex"** Bot with the "**Acquire Chat Widget**".

The **Bot Name** & **Alias** are ****displayed in step 11 \(highlighted in the red box\).

In order to get your **Secret Key** and **Access key**, you need to follow the procedure below:

**\(a\).** Go to **Amazon IAM service**.

![](https://lh6.googleusercontent.com/ABOT56wtHZAkQbSrggD4QyQVrx-SNNuVWNfkFtO2hL2yhHdC7ZxwVIs9SLUQPrh55BJ92Jdzb1PKaUcd3WXhNE95b5IorsUkJN7nCmN8yeKwlwpfoJukpSTJLr8IXW2amjqbZWpM)

**\(b\).** Go to **“Manage Security Credentials”** in **“Delete your access keys”** section.

![](https://lh5.googleusercontent.com/WS7ftn6nyMxkpfOrwPmE0a8h07A0nR_RmjwjZp0YK2PPBQ8C_TYbNmBQHlIEOSmdhpdhGmBUHGdaaSBnCIs6Zm1SRhbxY7NqWx7JaFW20GDnGpTlpIwa5c4zDSqG-MBCSp0CPQAj)

**\(c\).** Select **“Get Started with IAM users”**.

![](https://lh4.googleusercontent.com/6viX7hOcuyoLK9E45fibd-psDXz3VTrdU_QkVzUMn2FdG9leN3vVaMz8CtTC7ywBRpgm0Gl8OjfbJ8eXNVfH8OLW70430Du6Whzy59vd77HG_HDd1xcSchNRVhaZpjmYlnCFXr3f)

**\(d\).** Enter a new **“Username”** and check the box named **“Programming access”**.

![](https://lh5.googleusercontent.com/0fuX6I9p9L81irwQT0Rn8Hs_DU59SuG2qS-t5-aeLbpji2s41t3zjESLMhkMBbugsfFe-kQ0h1tiLIh4vXwvg2uEorKMXCmvfuhtZ-BdRH06ZIAlHTn9gJtB1lRuUf7TBSQxXUc1)

**\(e\).** Now, you can add the user to an existing group or create a new group. Click on **“Create Group”** to create a new group.

![](https://lh6.googleusercontent.com/TTO164VKEbrmHv-f_4Dzv39QfM7eCbR09iLaSysIM3wn-xHx9PgKwnmnPntTkwkbPJg-S0o5Dcofw7D95gkWz97OWP4HTKX0dJO8GknLy38xjtIbjwtHKaErFFRFweFYZ-uFPUKd)

**\(f\).** Give a new name to the group and add permissions of **“AmazonLexReadOnly”** and **“AmazonLexRunBotsOnly”** and then click on **“Create Group”**.

![](https://lh5.googleusercontent.com/mr0q2UxdvamnmxBp3gzLRZbYviJG51fDAoV9jfpN0LXv1Q1rhd7kUfqVwwIonY0VFt5qeQZCIm2WavOApPf4Kk16DFn-Ps7DZXDO0wPHEhDKIqjRIPqQzcaIRi5kAm1IDicH3-6f)

**\(g\).** Next **“Add tags”** section is optional. You can simply go to **“Next”**.

![](https://lh5.googleusercontent.com/8mL0LcnechltCw4fjEjJlt-YllPHoPFH2l8D8jl40wv2bhUxQq1qOpH__Q1-DJ8wKR-g2OQQPCPO6M1My9C_o81sppLAZeeBGHyZiBASS_H2ae81i6-A0S4civVLWLtR7eIPCbRz)

Review all the information and press **“Create User”**.

![](https://lh5.googleusercontent.com/UiM5cmdF0KP9ycvETMmJgykbFdEWBJ1GWSTyTR9Rei6dPv5Vu5g8uRgMmm7W7rp4ZTodB0vvFiOsgGCtAfN41UMSrLPXnb2CTrBKmX0Vqp2LFqaRJ7ASMnLGXAX0W39jPfB9T0Jw)

Here, you can obtain your **“Access key ID”** and **“Secret access key”**. You can also download a CSV file to save these credentials.

![](https://lh5.googleusercontent.com/Yuk5VU30dt2jhDi83Z4TqUGrAjvkpwGodBi99J2rPruZH8dYsNZLpz--Rshd2N5S9sEYFrDzN5E5az5gS-dtSsDCVir_cvjVPmQnpeMCi7EhTXDvtY1ajtU78bV5pPu9nEkHZlF_)

**13.** You can always access the value of region from the "**Amazon Lex"** homepage URL

**https://&lt;aws\_region&gt;.console.aws.amazon.com.**  


**14.** Now, we have all the parameters to connect our "**Amazon Lex"** bot with the **“Acquire Chat Widget”**. 

So, let us install the "**Amazon Lex** **Bot**" from the Bot Store.

![](../../.gitbook/assets/live1.png)

| **access\_key** | **Access key ID \(Step 12\)** |
| :--- | :--- |
| secret\_key | Secret access key \(Step 12\) |
| aws\_region | Step 13 |
| bot\_name | Bot name \(Step 11\) |
| bot\_alias | Alias \(Step 11\) |

![](../../.gitbook/assets/live2.png)

**15.** Go to **“Triggers”** and apply **“Amazon Lex Bot”** chatbot.

![](https://lh6.googleusercontent.com/VFrijx5e7fpNveJgbRQiRh4jcROeTTzhWh9l-01fHKhtt0KDas0_HGuYbXPuBp87BhgzKRQmVSWzFUReziWUFsppdGTY25Q-VGM6IfpdZHZJSFwj8ZmLuV7HFdkz2ZhNKzEZpNnM)

**16.** Finally, You can test the "**Acquire Chat Widget"** using the intents you have created with "**Amazon Lex"**.

![](../../.gitbook/assets/live3.png)

