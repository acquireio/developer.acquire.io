---
description: API to get mail messages
---

# Mail Messages

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/mail/messages?threadId=1196" path="" %}
{% api-method-summary %}
Mail Messages
{% endapi-method-summary %}

{% api-method-description %}
API to get mail messages
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="threadId" type="integer" required=true %}
Id of the thread to get the mail message
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "previous": "LTU4Mg==",
    "next": "KzU4Mg==",
    "messages": [
      {
        "id": 582,
        "caseMessageId": null,
        "channelId": null,
        "caseId": 1196,
        "inboxId": 2,
        "mailId": 2,
        "type": "message",
        "senderType": "contact",
        "senderId": 597323,
        "to": [
          {
            "Name": "",
            "Email": "viswanath.sarma@acquire.io",
            "MailboxHash": ""
          }
        ],
        "from": {
          "Name": "Sentry",
          "Email": "noreply@md.getsentry.com",
          "MailboxHash": ""
        },
        "cc": [],
        "bcc": [
          {
            "Name": "",
            "Email": "viswanath.sarma1@5mkg3t.uat.env.acquire.io",
            "MailboxHash": ""
          }
        ],
        "reply_to": null,
        "subject": "FRONTEND-APP-75R - TypeError: Cannot read property 'toString' of null",
        "textBody": "Details\r\n-------\r\n\r\nhttps://sentry.io/organizations/acquire-new/issues/2266850648/?referrer=alert_email\r\n\r\n\r\n\r\nTags\r\n----\r\n\r\n* browser = Chrome 88.0.4324\r\n* browser.name = Chrome\r\n* device = Mac\r\n* device.family = Mac\r\n* handled = yes\r\n* level = error\r\n* mechanism = instrument\r\n* os = Mac OS X 11.0.0\r\n* os.name = Mac OS X\r\n* sentry:user = ip:157.38.85.37\r\n* url = https://f0luvw.uat.env.acquire.io/settings/audit-log\r\n\r\n\r\nException\r\n-----------\r\n\r\nTypeError: Cannot read property 'toString' of null\r\n  at s.value (/dist/42.95d17cc99572.bundle.min.js:1:145202)\r\n  at None (/dist/42.95d17cc99572.bundle.min.js:1:146119)\r\n  at Array.map (<anonymous>)\r\n  at None (/dist/42.95d17cc99572.bundle.min.js:1:146091)\r\n  at Array.map (<anonymous>)\r\n...\r\n(39 additional frame(s) were not displayed)\r\n\r\n\r\nRequest\r\n-----------\r\n\r\n\r\n\r\n\r\nUser\r\n-----------\r\n\r\n\r\n\r\n\r\n\r\n\r\nUnsubscribe: https://sentry.io/account/notifications/unsubscribe/5196197/?_=G5N9:1lKKQI:IFhQsoZTWVJpM5IptbMv6YT8b9w&referrer=alert_email",
        "htmlBody": "<!DOCTYPE html>\r\n<html style=\"font-weight: 300\">\r\n<head style=\"font-weight: 300\">\r\n  <meta charset=\"utf-8\" style=\"font-weight: 300\">\r\n  <meta name=\"viewport\" content=\"width=device-width, initial-scale=1\" style=\"font-weight: 300\">\r\n\r\n  \r\n\r\n<style type=\"text/css\" style=\"font-weight: 300\">\r\n  @import url(https://fonts.googleapis.com/css?family=Lato:400,700);\r\n</style>\r\n\r\n\r\n  \r\n\r\n</head>\r\n<body class=\"\" style='font-weight: 300; background-image: url(https://s1.sentry-cdn.com/_static/624cf2bb5104f4122f08292bd17f4c1d/sentry/images/email/sentry-pattern.png); width: 100%; font-size: 16px; font-family: \"Lato\", \"Helvetica Neue\", helvetica, sans-serif; background-color: #fff; color: #2f2936; -webkit-font-smoothing: antialiased; margin: 0; padding: 0'>\r\n<div class=\"preheader\" style=\"font-weight: 300; display: none; font-size: 0; max-height: 0; line-height: 0; mso-hide: all; padding: 0\">\r\n  New alert from frontend-app.\r\n</div>\r\n<table class=\"main\" style='font-weight: 300; width: 100%; border-collapse: separate; font-size: 16px; font-family: \"Lato\", \"Helvetica Neue\", helvetica, sans-serif; background-color: #fff; color: #2f2936; -webkit-font-smoothing: antialiased; max-width: 700px; box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1); border-radius: 4px; border: 1px solid #c7d0d4; border-spacing: 0; margin: 15px auto; padding: 0'>\r\n  <tr style=\"font-weight: 300\">\r\n    <td style=\"font-weight: 300; text-align: center; margin: 0; padding: 0\">\r\n      <div class=\"header\" style=\"font-weight: 300; font-size: 14px; border-bottom: 1px solid #dee7eb; padding: 23px 0\">\r\n        <div class=\"container\" style=\"font-weight: 300; max-width: 600px; text-align: left; margin: 0 auto; padding: 0 20px\">\r\n          \r\n    <a href=\"https://sentry.io/organizations/acquire-new/issues/2266850648/?referrer=alert_email\" class=\"btn\" style=\"font-weight: 600; color: #fff; text-decoration: none; background-color: #6C5FC7; border: 1px solid #413496; box-shadow: 0 2px 0 rgba(0, 0, 0, 0.08); line-height: 18px; border-radius: 4px; display: inline-block; font-size: 16px; float: right; margin: -3px 0 0; padding: 8px 15px\">View on Sentry</a>\r\n    \r\n          <h1 style=\"font-weight: normal; font-size: 38px; line-height: 42px; color: #000; letter-spacing: -1px; margin: 0; padding: 0\">\r\n            <a href=\"https://sentry.io\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\"><img src=\"https://s1.sentry-cdn.com/_static/624cf2bb5104f4122f08292bd17f4c1d/sentry/images/email/sentry_logo_full.png\" width=\"125px\" height=\"29px\" alt=\"Sentry\" style=\"font-weight: 300\"></a>\r\n          </h1>\r\n          \r\n\r\n        </div>\r\n      </div>\r\n    </td>\r\n  </tr>\r\n  <tr style=\"font-weight: 300\">\r\n    <td style=\"font-weight: 300; text-align: center; margin: 0; padding: 0\">\r\n      \r\n      <div class=\"container\" style=\"font-weight: 300; max-width: 600px; text-align: left; margin: 0 auto; padding: 0 20px\">\r\n        <div class=\"inner\" style=\"font-weight: 300; background-color: #fff; padding: 30px 0 20px\">\r\n          \r\n    <h2 style=\"font-weight: 700; font-size: 22px; margin: 0 0 15px\">\r\n        New alert from <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197\" style=\"font-weight: inherit; color: #4674ca; text-decoration: none\">frontend-app</a>\r\n        \r\n    </h2>\r\n\r\n    \r\n      <table class=\"event-list\" style=\"font-weight: 300; width: 100%; border-collapse: collapse; text-align: left; margin: 0 0 15px\">\r\n        <tr style=\"font-weight: 300\">\r\n            <th colspan=\"2\" style=\"font-weight: bold; text-align: left; min-width: 60px; color: #9CA3AD; text-transform: uppercase; font-size: 12px; border-bottom: 2px solid #E7EBEE; margin: 0 0 5px; padding: 10px 0\">Issue</th>\r\n        </tr>\r\n        <tr style=\"font-weight: 300\">\r\n          <td class=\"error-level\" style=\"font-weight: 300; text-align: left; border-top: 1px solid #E7EBEE; width: 70px; margin: 0; padding: 10px 0\">\r\n              <span class=\"level level-error\" style=\"font-weight: 300; color: #fff; border-radius: 3px; font-size: 16px; text-transform: capitalize; background-color: #ec5e44; padding: 0 6px 2px\">error</span>\r\n          </td>\r\n          <td class=\"event-detail\" style=\"font-weight: 300; text-align: left; border-top: 1px solid #E7EBEE; line-height: 22px; width: 400px; margin: 0; padding: 10px 0\">\r\n            <div class=\"issue\" style=\"font-weight: 300; line-height: 22px\">\r\n              \r\n                \r\n                  <div class=\"event-type error\" style=\"font-weight: 300\">\r\n                    <h3 style=\"font-weight: 700; font-size: 18px; line-height: 22px; margin: 0\">\r\n                      \r\n                        <a href=\"https://sentry.io/organizations/acquire-new/issues/2266850648/?referrer=alert_email\" style=\"font-weight: 600; color: #4674ca; text-decoration: none; font-size: 16px; margin-right: 10px\">TypeError</a>\r\n                        \r\n                        <br style=\"font-weight: 300\">\r\n                        \r\n                          <small style=\"font-weight: 300; font-size: 14px; color: #968ba0\">Cannot read property 'toString' of null</small>\r\n                        \r\n                      \r\n                    </h3>\r\n                  </div>\r\n                \r\n              \r\n            </div>\r\n          </td>\r\n        </tr>\r\n      </table>\r\n\r\n      <div class=\"event\" style=\"font-weight: 300; margin-bottom: 30px\">\r\n        <div class=\"event-id\" style=\"font-weight: 300; color: #889092; float: right\">ID: 079217f57911408c8e663cd30dc1d065</div>\r\n        <div class=\"event-date\" style=\"font-weight: 300; color: #889092\">March 11, 2021, 12:27:56 p.m. UTC</div>\r\n      </div>\r\n\r\n      \r\n\r\n      \r\n      <div class=\"interface\" style=\"font-weight: 300; margin-bottom: 30px\">\r\n          <h3 class=\"title\" style=\"font-weight: 700; font-size: 18px; margin: 0 0 15px\">Exception</h3>\r\n          <pre style='font-weight: normal; font-family: Menlo, Monaco, \"Courier New\", monospace; font-size: 14px; white-space: pre-wrap; background-color: #F4F5F6; color: #3D4649; border-radius: 4px; overflow-wrap: break-word; word-wrap: break-word; margin: 0 0 15px; padding: 15px'>TypeError: Cannot read property 'toString' of null\r\n  at s.value (/dist/42.95d17cc99572.bundle.min.js:1:145202)\r\n  at None (/dist/42.95d17cc99572.bundle.min.js:1:146119)\r\n  at Array.map (&lt;anonymous&gt;)\r\n  at None (/dist/42.95d17cc99572.bundle.min.js:1:146091)\r\n  at Array.map (&lt;anonymous&gt;)\r\n...\r\n(39 additional frame(s) were not displayed)</pre>\r\n      </div>\r\n      \r\n      <div class=\"interface\" style=\"font-weight: 300; margin-bottom: 30px\">\r\n          <h3 class=\"title\" style=\"font-weight: 700; font-size: 18px; margin: 0 0 15px\">Request</h3>\r\n          \r\n<table style=\"font-weight: 300; width: 100%; border-collapse: separate; border-spacing: 5px; margin: 0 -5px\">\r\n    <colgroup style=\"font-weight: 300\">\r\n      <col style=\"font-weight: 300; width: 130px\">\r\n    </colgroup>\r\n    <tbody style=\"font-weight: 300\">\r\n        \r\n        <tr style=\"font-weight: 300\">\r\n            <th style=\"font-weight: 500; text-align: left; min-width: 60px; color: #968ba0; padding: 10px 0 0\">URL</th>\r\n            <td style=\"font-weight: 400; text-align: left; background-color: #f4f5f6; border-radius: 3px; margin: 0 0 5px; padding: 5px 10px\"><a href=\"https://f0luvw.uat.env.acquire.io/settings/audit-log\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">https://f0luvw.uat.env.acquire.io/settings/audit-log</a></td>\r\n        </tr>\r\n        \r\n        \r\n        \r\n        \r\n    </tbody>\r\n</table>\r\n\r\n      </div>\r\n      \r\n      <div class=\"interface\" style=\"font-weight: 300; margin-bottom: 30px\">\r\n          <h3 class=\"title\" style=\"font-weight: 700; font-size: 18px; margin: 0 0 15px\">User</h3>\r\n          \r\n\r\n\r\n<table class=\"reset\" style=\"font-weight: 300; width: 100%; border-collapse: collapse; border-spacing: 0; margin: 0 -5px\">\r\n  <tr style=\"font-weight: 300\">\r\n    <td style=\"font-weight: 400; text-align: left; background-color: #fff; border-radius: 3px; margin: 0 0 5px; padding: 0\">\r\n      <table style=\"font-weight: 300; width: 100%; border-collapse: separate; border-spacing: 5px; margin: 0\">\r\n        <colgroup style=\"font-weight: 300\">\r\n          <col style=\"font-weight: 300; width: 130px\">\r\n        </colgroup>\r\n        <tbody style=\"font-weight: 300\">\r\n          \r\n          \r\n            <tr style=\"font-weight: 300\">\r\n              <th style=\"font-weight: 500; text-align: left; min-width: 60px; color: #968ba0; padding: 10px 0 0\">IP Address:</th>\r\n              <td class=\"code\" style=\"font-weight: 400; text-align: left; background-color: #f4f5f6; border-radius: 3px; margin: 0 0 5px; padding: 5px 10px\">157.38.85.37</td>\r\n            </tr>\r\n          \r\n          \r\n          \r\n          \r\n        </tbody>\r\n      </table>\r\n    </td>\r\n    \r\n  </tr>\r\n</table>\r\n\r\n      </div>\r\n      \r\n\r\n      \r\n        <h3 style=\"font-weight: 700; font-size: 18px; margin: 0 0 20px\">Tags</h3>\r\n\r\n        <ul class=\"tag-list\" style=\"font-weight: 300; list-style: none; margin: 0 0 20px; padding: 0\">\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">browser</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=browser%3A%22Chrome%2088.0.4324%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">Chrome 88.0.4324</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">browser.name</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=browser.name%3A%22Chrome%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">Chrome</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">device</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=device%3A%22Mac%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">Mac</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">device.family</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=device.family%3A%22Mac%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">Mac</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">handled</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=handled%3A%22yes%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">yes</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">level</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=level%3A%22error%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">error</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">mechanism</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=mechanism%3A%22instrument%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">instrument</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">os</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=os%3A%22Mac%20OS%20X%2011.0.0%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">Mac OS X 11.0.0</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">os.name</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=os.name%3A%22Mac%20OS%20X%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">Mac OS X</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">user</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=user%3A%22ip%3A157.38.85.37%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">ip:157.38.85.37</a> \r\n              \r\n              </span>\r\n          </li>\r\n        \r\n          <li style=\"font-weight: 300; display: inline-block; margin-right: 5px; margin-bottom: 10px; border-radius: 3px; background-color: #F4F5F6; padding: 5px 10px 6px\">\r\n              <strong style=\"font-weight: 200\">url</strong>\r\n              <em style=\"font-weight: 300\">=</em>\r\n              <span style=\"font-weight: 300\">\r\n              \r\n                <a href=\"https://sentry.io/organizations/acquire-new/issues/?project=5196197&amp;query=url%3A%22https%3A//f0luvw.uat.env.acquire.io/settings/audit-log%22\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">https://f0luvw.uat.env.acquire.io/settings/audi...</a> <a href=\"https://f0luvw.uat.env.acquire.io/settings/audit-log\" class=\"icon-share\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\"></a>\r\n              \r\n              </span>\r\n          </li>\r\n        \r\n        </ul>\r\n      \r\n    \r\n\r\n    \r\n        <p class=\"via\" style=\"font-weight: 300; font-size: 14px; line-height: 24px; background-color: #f7f8f9; text-align: center; border-radius: 3px; margin: 15px 0; padding: 15px\">\r\n            You are receiving this email due to matching rules:\r\n            \r\n                <a href=\"https://sentry.io/organizations/acquire-new/alerts/rules/frontend-app/1057792/\" style=\"font-weight: 500; color: #4674ca; text-decoration: none\">Send a notification for new issues</a>\r\n            \r\n        </p>\r\n    \r\n\r\n    \r\n\r\n    \r\n    <div itemscope itemtype=\"http://schema.org/EmailMessage\" style=\"font-weight: 300\">\r\n      <meta itemprop=\"description\" content=\"View Issue Details in Sentry\" style=\"font-weight: 300\">\r\n      <div itemprop=\"action\" itemscope itemtype=\"http://schema.org/ViewAction\" style=\"font-weight: 300\">\r\n        <link itemprop=\"url\" href=\"https://sentry.io/organizations/acquire-new/issues/2266850648/?referrer=alert_email\" style=\"font-weight: 300\">\r\n        <meta itemprop=\"name\" content=\"View in Sentry\" style=\"font-weight: 300\">\r\n      </div>\r\n      <div itemprop=\"publisher\" itemscope itemtype=\"http://schema.org/Organization\" style=\"font-weight: 300\">\r\n        <meta itemprop=\"name\" content=\"GetSentry\" style=\"font-weight: 300\">\r\n        <link itemprop=\"url\" href=\"https://sentry.io/\" style=\"font-weight: 300\">\r\n      </div>\r\n    </div>\r\n\r\n        </div>\r\n      </div>\r\n      \r\n      <div class=\"container\" style=\"font-weight: 300; max-width: 600px; text-align: left; margin: 0 auto; padding: 0 20px\">\r\n        <div class=\"footer\" style=\"font-weight: 300; border-top: 1px solid #E7EBEE; padding: 35px 0\">\r\n          \r\n          <a href=\"https://sentry.io\" style=\"font-weight: 500; color: #687276; text-decoration: none; float: right\">Home</a>\r\n          \r\n          <a href=\"https://sentry.io/settings/account/notifications/\" style=\"font-weight: 500; color: #687276; text-decoration: none\">Notification Settings</a>\r\n          \r\n            &#183; <a href=\"https://sentry.io/account/notifications/unsubscribe/5196197/?_=G5N9:1lKKQI:IFhQsoZTWVJpM5IptbMv6YT8b9w&amp;referrer=alert_email\" style=\"font-weight: 500; color: #687276; text-decoration: none\">Unsubscribe</a>\r\n          \r\n          \r\n        </div>\r\n      </div>\r\n    </td>\r\n  </tr>\r\n</table>\r\n\r\n<img src=\"https://u2307627.ct.sendgrid.net/wf/open?upn=bL1w6lLA-2BUCR44J5JzesZeQsK4eRk0A1c4CRqTc4-2BFDf6UjTW3LUkYqJVAsuSpCxYgOHnNYhAYWB3irQfRLQriPyNXQ3XtW6mtZMxfXkqmJyIxoLgJAiW9sv89Xk8mxGTF0LMllEN3t7ifZTzlPKZPhn7Jfxe7QJwB7VGlJUqWzvKfP52pvNBARhECw-2F64SqjXRUyVumYysSRSrb40OUFsxMm6HO2FTfDtsvhOYSQ-2BeL1jAHveZGLMGBI8-2BHVzPjGbXEPei-2BH7ltVsB0joW9Ng-3D-3D\" alt=\"\" width=\"1\" height=\"1\" border=\"0\" style=\"height:1px !important;width:1px !important;border-width:0 !important;margin-top:0 !important;margin-bottom:0 !important;margin-right:0 !important;margin-left:0 !important;padding-top:0 !important;padding-bottom:0 !important;padding-right:0 !important;padding-left:0 !important;\"/>\r\n</body>\r\n</html>",
        "mailboxMessageId": null,
        "messageId": "ab91965a-fa6a-4482-882d-7387b7d60db5",
        "mailboxInReplyTo": null,
        "originalRecipient": "viswanath.sarma1@5mkg3t.uat.env.acquire.io",
        "parentId": null,
        "attachments": [],
        "dateCreated": "2021-03-11T12:28:23.000Z",
        "dateSeen": null,
        "dateBounce": null,
        "dateFailed": null,
        "dateDelivery": null,
        "seen": "no",
        "isDraft": "no",
        "scheduleAt": null,
        "meta": null,
        "clickedDate": null,
        "unsubscribeDate": null,
        "appMessageId": null,
        "appThreadId": null,
        "sender": {
          "type": "contact",
          "id": 597323,
          "name": "Sentry",
          "email": "noreply@md.getsentry.com",
          "photo": ""
        }
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "ids": [
    53,
    52
  ]
}
```

