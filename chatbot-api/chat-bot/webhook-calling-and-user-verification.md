# Webhook Calling & User Verification

### **Widget Installation**

First of all we have to setup our site with **“Acquire”** chat widget. You can get the **“chat widget code”** from **“Installation”** option under **“Settings”** menu.

![](https://lh3.googleusercontent.com/WuJYbb-IJHldRmedvcJ-40kMsP3Zo5XImwws3QCMJcBN2cjUE7--IaKrsbhh_2ZQFhojsYX86FM2IgLsf2_OC9dJ57f4__xE3K1saZCruDFDbNNIqm7VuazbWjvBkk_0RQ)

To identify every visitor, we have to put Visitor Authentication functionality with widget code. Authentication code will produce **HMAC** Code, that verify the identity of that visitor i.e. visitor\_id. **HMAC** code will be assigned with an attribute, named as **user\_hash**. Find more details on this link: [https://developer.acquire.io/js-api/js-live-chat-api/user-verification](https://developer.acquire.io/js-api/js-live-chat-api/user-verification.).

### **Additional Setup**

First of all, we create a hidden field in **“chat form”**, it will store visitor’s information, that will be helpful to identify that user. In screenshot we setup hidden field with name **v\_id**.

![](https://lh3.googleusercontent.com/Ah6vzATYPuwj5n-Bs7dfy7_tF3l3_G6SSetXq-k8AIgYEyYdHdPULaUMFtXMauVOQOQrLYueKoAqnK1rEYagrdp_daxFuKcNWo-WA1h6FfKiCLj6VwAaTzMajwi8eYX8_w)

Then after we open our website where Acquire’s chat widget is enabled, and provide visitor’s info with it. We made a blank php page and provide visitor’s id along with URL.

**URL: /chat\_widget.php?id=35**

We use this **id** and build a **hash\_hmac** value from this id. Then resultant value will be push to acquire object. Like: user\_hash: **‘&lt;?php echo $hashVal ?&gt;’**

Important : Use **HMAC** only Server side not use client side and Keep your secret key safe!

![](https://lh6.googleusercontent.com/9Pmsr0lqVGkxHxCZ5zFdSQTwGOU0LoO4K6v7SlzGXVNce740L-NuhZara_QYaz21pRhYDKjQ5YNugpd6vznRemwl5PMVm1S6D6lUVo5LFNpGojxG9bv5I8tegbGJQ0IxkQ)

Now our chat widget is fully set up. Let's make a webhook now.

### **Webhook Creation**

Now we make a webhook API, i.e. Get premium amount, Get expiry date & etc. Whenever we call this webhook API, we will get huge data about visitor in body of that particular API. Like: hash, visitor\_id, chat\_id, visitor’s name, visitor’s email, browser details, custom fields value, other misc details.

![](https://lh5.googleusercontent.com/IbNYRdlFgX8gv87G9tBE9eV3T-PVA4jy7yPnYmwpVPS3Ui_Nk0_0bfz7y3wxqQj1HJpF6SkLMDGrr0MocKUY5NSa1jzDY9kZMEyd64hUKFahWvoohpoVWMzdytYEIEGxaw)



![](https://lh3.googleusercontent.com/_jYkDLa7d3IatxZs7hcPAc9C5OcDIsPHsxYtmca5J7c2A_k2D7j2UG8jI9o5BuXCdpXQkHCAu5KnK0FweWLI87UeOZK8Syt8bStFieMn4vr5OfOrB8N-0JfsuZAoE-Du5w)

We can use **v\_id** and **hash** in our webhook. Again we can make hash value **$new\_hash** from **$v\_id** by use of your **secret key** and match it with **$init\_hash** . If it matched with it then we able to know that this visitor is authenticated.

![](https://lh5.googleusercontent.com/keQmSLGD3gKbXoqkH3N1H67_QU4usAE5owIRqkcNO5Pmbtnh9swBYRt6hc2hmmwyxRitpfbIy3Iy5IgfpxeFhTvrNKEMNAL_nNaq1pSLJT9ZxRg6CXQJcWomhiGwJg16mQ)

Now we add link of this webhook in Bot’s Webhook APIs Library with a variable name. Make sure you make variable name as you used in webhook. For example: we create a webhook API with response **{ ‘premium\_amount’ : ’Your premium amount is 5410 rs.’ }** then in below popup box, we have to make variable name as **premium\_amount**. You can find this at **“Chatbot &gt; Setting &gt; Webhook APIs”**.

![](https://lh5.googleusercontent.com/ctDANQhemeCYsFEQGweYI0Cnmhxktwg4KcCEfftj_p5kPx6gofn7D8H47yI5Lp9SN81PNirAVQyTRabh741jJBapHPenbo3P5vLuiI5hVsZpkqFQmeFy4KDpyIIofgZNUA)

Now our webhook variable is set up.

### **Use of Webhook**

Now we add a question in Support Bot like:

![](https://lh3.googleusercontent.com/NgBPAf_T70NY2WZyUwB8XHdZUWaSQ5E63nMSX1Ip7oV7-gmrgEephTSHwpUOen3xixZ3VB_aIbNengkquWErt-Ky0CMJfSvVIhAcikdhz4w5FzqZ0QVcFuPZYy-ej8vpbg)

We will use webhook variable as answer of bot. So whenever we ask this question to bot then bot call that webhook and replace this variable with API response. See widget image on next page.

![](https://lh5.googleusercontent.com/2B_zyD-pQTwUDmGlZU80-A97jIvj1ay8QEgOvfQLQ3EgzV4NKys8bV5042C8He8elnR7cu5MGbp5rxI6QuOeMYhxlJIyjBQADojE8OYPmb_VYkU3XNJ8x4En-FO7ROXpeA)





  


