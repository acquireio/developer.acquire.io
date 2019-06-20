# Webhook For Reset Password

### **Webhook Creation:**

To resetting the password, first of all we create a webhook API. Whenever we call this webhook API, we will get huge data about visitor in body of that particular API. Like: hash, visitor\_id, chat\_id, visitor’s name, visitor’s email, lead details, browser details, custom fields value, other misc details.

![](https://lh3.googleusercontent.com/IMA5tM_pHmczLuDlnA-iYIWdDF-L3O1NIXJCJkfyCThDkZ3T72NqXnbA5-jFU_dLV1X4nJxl3_lz7QiIpqiG7vj7SE4dG9kz_gqKEy7b1GwPdGhOFecl4qREtAZxaG-HwQoMLwIb)

So by the use of visitor’s email we can call our internal Endpoint of Resetting the password, by the use of this Webhook API.  

 First of all we fetch visitor’s Email from this huge data, then after we call our endpoint by the use of cURL\(in PHP\) and then webhook will reply based on the cURL response. Bot will use that Webhook response and replace it with webhook variable in Sales-Bot’s Lead.

 In Code, We do like this:

![](https://lh6.googleusercontent.com/0drzjXGF2rMy_MR8-1uUbjZRKJ1KcvIstudg4KcVLsjOxd0mrCYyU0JfQE2Fixj2x3LA5726HKgB0cVvwv594aak4Co_Q6oW6dnDwYixcjYqBYdQYqhnf8HClH7KNx5otQBaRuIW)

**I**n cURL Code, we call our endpoint, where we pass **$email** value on **&lt;SYSTEM\_DOMAIN&gt;/api/auth/forget-password** endpoint. Then after according to response we setup our webhook. Keep this mind that, If you create webhook variable as **reset\_password\_status** then response of this webhook must be **{“reset\_password\_status”: “&lt;MESSSAGE HERE&gt;”}**. So Bot can easily understand it and replace it with webhook variable.

 After creating this webhook API, we add this in Webhook APIs Section in Acquire **\(Chat Bot &gt; Setting &gt; Webhook APIs\)**.

![](https://lh5.googleusercontent.com/_rjhNql9xG6tSPw7pcaqDtNXgLOsLs0snt9dHO5C3AwDjsbt_doOrvwHKMJ2VXG1W84bMkbfg5MDNn-dMxLALxyfSVFIGSnZAJyNGTmSp2DN8xlBodsLsnSz1CvH_19rILgW5mxf)

### **Lead creation with webhook variable:**

Now we make a Lead in Sales-Bot, where we make various branches. In branches, somewhere we use that webhook variable **{{reset\_password\_status}}**. Create lead branch like:

![](https://lh6.googleusercontent.com/szrhdeu81dd840CZVT-ODXstFZmBH44B9q3FRiDQCoEEyUR0Ux8-yZtwNxVVFzPWBLe7VA1xU9AohTLA9d3onljurnGM9g6XTKFYWuaN5PL6OT3beutFoSTrC2jTRkJOKZLDq_CL)

Now, we call this Lead either from Trigger section or from Support-Bot. In Support-Bot we make a Question/Answer as “I forgot my password” then Support-Bot will redirect us to Sales-Bot. See Example:

![](https://lh3.googleusercontent.com/XGmIOpcii-IXkaZSKVOGmBmDW0o2gxnOaxxYKFtTV2MuHRtTond8ELtNkmK6IBSRVm45s_I1n8u-kdW-YDwKXP1G3PjieFcbxk-reQiPkw_O4F01Fe459aQC9ehdOLAgddy7bM-q)

