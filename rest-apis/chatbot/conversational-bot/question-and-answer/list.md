---
description: List the questions and answers in a group.
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna?type={{type}}&groupId={{groupId}}" path="" %}
{% api-method-summary %}
List all questions and answers
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of questions and answers for a group. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="type" type="string" required=true %}
Specify the type of question/answer: all, live, or suggested
{% endapi-method-parameter %}

{% api-method-parameter name="groupId" type="integer" required=true %}
Specify the group's ID
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "groupId": 1,
    "count": 5,
    "limit": 12,
    "page": 1,
    "rows": [
      {
        "id": 46,
        "type": "live",
        "subtype": "user_added",
        "status": "active",
        "language": "en",
        "answerType": "formatted",
        "actionEnabled": "disabled",
        "wantFeedback": "active",
        "askedCount": 3,
        "allowRelatedQue": "disabled",
        "relatedQueIds": "",
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2021-01-20T04:27:22.000Z",
        "dateUpdated": "2021-01-29T10:40:53.000Z",
        "qnaMainQuestions": [
          {
            "id": 46,
            "question": "Test with this Case of text"
          }
        ],
        "qnaMainAnswers": [
          {
            "id": 46,
            "answer": "Hello Everyone how do you do\n\n![video](https://www.youtube.com/embed/eqCkkC9A0Q4)\n\n",
            "answerJson": {
              "blocks": [
                {
                  "key": "b3hg7",
                  "data": {},
                  "text": "Hello Everyone how do you do",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                },
                {
                  "key": "27iik",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                },
                {
                  "key": "eeqol",
                  "data": {},
                  "text": " ",
                  "type": "atomic",
                  "depth": 0,
                  "entityRanges": [
                    {
                      "key": 0,
                      "length": 1,
                      "offset": 0
                    }
                  ],
                  "inlineStyleRanges": []
                },
                {
                  "key": "37fj6",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                }
              ],
              "entityMap": {
                "0": {
                  "data": {
                    "alt": "",
                    "src": "https://www.youtube.com/embed/eqCkkC9A0Q4"
                  },
                  "type": "VIDEO",
                  "mutability": "MUTABLE"
                }
              }
            }
          }
        ]
      },
      {
        "id": 45,
        "type": "live",
        "subtype": "user_added",
        "status": "active",
        "language": "en",
        "answerType": "formatted",
        "actionEnabled": "disabled",
        "wantFeedback": "active",
        "askedCount": 1,
        "allowRelatedQue": "disabled",
        "relatedQueIds": "",
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2021-01-15T13:14:21.000Z",
        "dateUpdated": "2021-01-19T05:17:31.000Z",
        "qnaMainQuestions": [
          {
            "id": 45,
            "question": "New Test Question Link Save"
          }
        ],
        "qnaMainAnswers": [
          {
            "id": 45,
            "answer": "chat ([[***Image]**[**https://xoht0l.acquire.io/)**](https://xoht0l.acquire.io/))** ])with text↵![image]**[**https://static.acquire.io/xoht0l/media/2021/1/chat-dc4a0b0ca20735b01f0aca1b.png)**](https://static.acquire.io/xoht0l/media/2021/1/chat-dc4a0b0ca20735b01f0aca1b.png))**↵New message with** bold text,  *_italic text *_and normal text.  **_boldItalic.  _******Note: warning text goes here***\n\n",
            "answerJson": {
              "blocks": [
                {
                  "key": "eoaj7",
                  "data": {},
                  "text": "chat ([[*Image](https://xoht0l.acquire.io/) ])with text↵![image](https://static.acquire.io/xoht0l/media/2021/1/chat-dc4a0b0ca20735b01f0aca1b.png)↵New message with bold text,  *_italic text *_and normal text.  _boldItalic.  _**Note: warning text goes here*",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [
                    {
                      "key": 0,
                      "length": 27,
                      "offset": 16
                    },
                    {
                      "key": 1,
                      "length": 80,
                      "offset": 65
                    }
                  ],
                  "inlineStyleRanges": [
                    {
                      "style": "color-rgb(23,43,77)",
                      "length": 9,
                      "offset": 0
                    },
                    {
                      "style": "color-rgb(23,43,77)",
                      "length": 47,
                      "offset": 162
                    },
                    {
                      "style": "color-rgb(23,43,77)",
                      "length": 2,
                      "offset": 224
                    },
                    {
                      "style": "color-rgb(23,43,77)",
                      "length": 1,
                      "offset": 254
                    },
                    {
                      "style": "bgcolor-rgb(235,236,240)",
                      "length": 9,
                      "offset": 0
                    },
                    {
                      "style": "bgcolor-rgb(235,236,240)",
                      "length": 27,
                      "offset": 16
                    },
                    {
                      "style": "bgcolor-rgb(235,236,240)",
                      "length": 80,
                      "offset": 65
                    },
                    {
                      "style": "bgcolor-rgb(235,236,240)",
                      "length": 47,
                      "offset": 162
                    },
                    {
                      "style": "bgcolor-rgb(235,236,240)",
                      "length": 2,
                      "offset": 224
                    },
                    {
                      "style": "bgcolor-rgb(235,236,240)",
                      "length": 1,
                      "offset": 254
                    },
                    {
                      "style": "fontsize-14",
                      "length": 9,
                      "offset": 0
                    },
                    {
                      "style": "fontsize-14",
                      "length": 27,
                      "offset": 16
                    },
                    {
                      "style": "fontsize-14",
                      "length": 80,
                      "offset": 65
                    },
                    {
                      "style": "fontsize-14",
                      "length": 47,
                      "offset": 162
                    },
                    {
                      "style": "fontsize-14",
                      "length": 2,
                      "offset": 224
                    },
                    {
                      "style": "fontsize-14",
                      "length": 1,
                      "offset": 254
                    },
                    {
                      "style": "fontfamily--apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Oxygen, Ubuntu, \"Fira Sans\", \"Droid Sans\", \"Helvetica Neue\", sans-serif",
                      "length": 9,
                      "offset": 0
                    },
                    {
                      "style": "fontfamily--apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Oxygen, Ubuntu, \"Fira Sans\", \"Droid Sans\", \"Helvetica Neue\", sans-serif",
                      "length": 27,
                      "offset": 16
                    },
                    {
                      "style": "fontfamily--apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Oxygen, Ubuntu, \"Fira Sans\", \"Droid Sans\", \"Helvetica Neue\", sans-serif",
                      "length": 80,
                      "offset": 65
                    },
                    {
                      "style": "fontfamily--apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Oxygen, Ubuntu, \"Fira Sans\", \"Droid Sans\", \"Helvetica Neue\", sans-serif",
                      "length": 47,
                      "offset": 162
                    },
                    {
                      "style": "fontfamily--apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Oxygen, Ubuntu, \"Fira Sans\", \"Droid Sans\", \"Helvetica Neue\", sans-serif",
                      "length": 2,
                      "offset": 224
                    },
                    {
                      "style": "fontfamily--apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Oxygen, Ubuntu, \"Fira Sans\", \"Droid Sans\", \"Helvetica Neue\", sans-serif",
                      "length": 1,
                      "offset": 254
                    },
                    {
                      "style": "BOLD",
                      "length": 153,
                      "offset": 9
                    },
                    {
                      "style": "BOLD",
                      "length": 15,
                      "offset": 209
                    },
                    {
                      "style": "BOLD",
                      "length": 28,
                      "offset": 226
                    },
                    {
                      "style": "color-rgb(0,82,204)",
                      "length": 27,
                      "offset": 16
                    },
                    {
                      "style": "color-rgb(0,82,204)",
                      "length": 80,
                      "offset": 65
                    }
                  ]
                },
                {
                  "key": "blb44",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                }
              ],
              "entityMap": {
                "0": {
                  "data": {
                    "url": "https://xoht0l.acquire.io/)",
                    "title": "<strong data-renderer-mark=\"true\">https://xoht0l.acquire.io/)</strong>",
                    "targetOption": ""
                  },
                  "type": "LINK",
                  "mutability": "MUTABLE"
                },
                "1": {
                  "data": {
                    "url": "https://static.acquire.io/xoht0l/media/2021/1/chat-dc4a0b0ca20735b01f0aca1b.png)",
                    "title": "<strong data-renderer-mark=\"true\">https://static.acquire.io/xoht0l/media/2021/1/chat-dc4a0b0ca20735b01f0aca1b.png)</strong>",
                    "targetOption": ""
                  },
                  "type": "LINK",
                  "mutability": "MUTABLE"
                }
              }
            }
          }
        ]
      },
      {
        "id": 41,
        "type": "live",
        "subtype": "user_added",
        "status": "active",
        "language": "en",
        "answerType": "formatted",
        "actionEnabled": "disabled",
        "wantFeedback": "active",
        "askedCount": 1,
        "allowRelatedQue": "disabled",
        "relatedQueIds": "",
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2020-12-24T05:46:00.000Z",
        "dateUpdated": "2021-01-04T11:49:16.000Z",
        "qnaMainQuestions": [
          {
            "id": 41,
            "question": "give me the emoji test results"
          }
        ],
        "qnaMainAnswers": [
          {
            "id": 41,
            "answer": "**_dsfdgdfgfgfgffhfgh_**\n\n![image](https://uat-drive.acquire.io/5mkg3t/media/2020/12/Screenshot-from-2020-12-22-16-35-48-ccdb7b6c416283758820d156.png)\n\n\\u{1f44b}\\u{1f60d}\\u{1f618}\\u{1f62d}\n",
            "answerJson": {
              "blocks": [
                {
                  "key": "9lghc",
                  "data": {},
                  "text": "dsfdgdfgfgfgffhfgh",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": [
                    {
                      "style": "BOLD",
                      "length": 18,
                      "offset": 0
                    },
                    {
                      "style": "ITALIC",
                      "length": 18,
                      "offset": 0
                    }
                  ]
                },
                {
                  "key": "30pcv",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                },
                {
                  "key": "fp9ha",
                  "data": {},
                  "text": " ",
                  "type": "atomic",
                  "depth": 0,
                  "entityRanges": [
                    {
                      "key": 0,
                      "length": 1,
                      "offset": 0
                    }
                  ],
                  "inlineStyleRanges": []
                },
                {
                  "key": "2td01",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                },
                {
                  "key": "ar0e8",
                  "data": {},
                  "text": "\\u{1f44b}\\u{1f60d}\\u{1f618}\\u{1f62d}",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                }
              ],
              "entityMap": {
                "0": {
                  "data": {
                    "alt": "",
                    "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/12/Screenshot-from-2020-12-22-16-35-48-ccdb7b6c416283758820d156.png",
                    "width": 100,
                    "height": 100,
                    "mediaKey": "WzIwODMsIm1lZGlhLzIwMjAvMTIvU2NyZWVuc2hvdC1mcm9tLTIwMjAtMTItMjItMTYtMzUtNDgtY2NkYjdiNmM0MTYyODM3NTg4MjBkMTU2LnBuZyIsIjVta2czdCIsIlNjcmVlbnNob3QgZnJvbSAyMDIwLTEyLTIyIDE2LTM1LTQ4LnBuZyIsNTIxOTEwXQ=="
                  },
                  "type": "IMAGE",
                  "mutability": "MUTABLE"
                }
              }
            }
          }
        ]
      },
      {
        "id": 22,
        "type": "live",
        "subtype": "user_added",
        "status": "active",
        "language": "en",
        "answerType": "formatted",
        "actionEnabled": "disabled",
        "wantFeedback": "active",
        "askedCount": 12,
        "allowRelatedQue": "disabled",
        "relatedQueIds": "",
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2020-10-13T10:52:13.000Z",
        "dateUpdated": "2020-10-21T18:45:16.000Z",
        "qnaMainQuestions": [
          {
            "id": 22,
            "question": "Sample Underline Test"
          }
        ],
        "qnaMainAnswers": [
          {
            "id": 22,
            "answer": "No matter which ++ESP or mail server you use++, the general setup for DKIM is the same. You need a private key stored somewhere safe, and you need to share a ++public key in your domain’s DNS records++. Similar to SPF, DKIM also uses DNS TXT records with a special format.\n\n![](https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-98d82f7209f9ea4436fa445c.png)\n\n\n\n",
            "answerJson": {
              "blocks": [
                {
                  "key": "86ehi",
                  "data": {},
                  "text": "No matter which ESP or mail server you use, the general setup for DKIM is the same. You need a private key stored somewhere safe, and you need to share a public key in your domain’s DNS records. Similar to SPF, DKIM also uses DNS TXT records with a special format.",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": [
                    {
                      "style": "UNDERLINE",
                      "length": 26,
                      "offset": 16
                    },
                    {
                      "style": "UNDERLINE",
                      "length": 39,
                      "offset": 154
                    }
                  ]
                },
                {
                  "key": "bakjt",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                },
                {
                  "key": "frbh0",
                  "data": {},
                  "text": " ",
                  "type": "atomic",
                  "depth": 0,
                  "entityRanges": [
                    {
                      "key": 0,
                      "length": 1,
                      "offset": 0
                    }
                  ],
                  "inlineStyleRanges": []
                },
                {
                  "key": "fpjqr",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                },
                {
                  "key": "ecbjt",
                  "data": {},
                  "text": " ",
                  "type": "atomic",
                  "depth": 0,
                  "entityRanges": [
                    {
                      "key": 1,
                      "length": 1,
                      "offset": 0
                    }
                  ],
                  "inlineStyleRanges": []
                },
                {
                  "key": "59scr",
                  "data": {},
                  "text": "",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": []
                }
              ],
              "entityMap": {
                "0": {
                  "data": {
                    "alt": "",
                    "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-98d82f7209f9ea4436fa445c.png",
                    "width": "10",
                    "height": "10",
                    "mediaKey": "Wzk4MSwibWVkaWEvMjAyMC8xMC83MWZmMzkzMDIzMWY1ZWNhOWQ2MmQ3MWU3ZDMxOTFlMS05OGQ4MmY3MjA5ZjllYTQ0MzZmYTQ0NWMucG5nIiwiNW1rZzN0IiwiNzFmZjM5MzAyMzFmNWVjYTlkNjJkNzFlN2QzMTkxZTEucG5nIiwzMDE2OF0="
                  },
                  "type": "IMAGE",
                  "mutability": "MUTABLE"
                },
                "1": {
                  "data": {
                    "alt": "",
                    "src": "https://www.youtube.com/watch?v=hoNb6HuNmU0"
                  },
                  "type": "draft-js-video-plugin-video",
                  "mutability": "MUTABLE"
                }
              }
            }
          }
        ]
      },
      {
        "id": 15,
        "type": "live",
        "subtype": "user_added",
        "status": "active",
        "language": "en",
        "answerType": "formatted",
        "actionEnabled": "disabled",
        "wantFeedback": "active",
        "askedCount": 3,
        "allowRelatedQue": "disabled",
        "relatedQueIds": "",
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2020-10-12T15:11:25.000Z",
        "dateUpdated": "2020-10-13T09:12:47.000Z",
        "qnaMainQuestions": [
          {
            "id": 15,
            "question": "Sample Test Question 1"
          }
        ],
        "qnaMainAnswers": [
          {
            "id": 15,
            "answer": "++Intelligent Virtual Assistants (IVA) have emerged over the last++ decade to address age-old pain points faced by people when interacting with businesses. From simple chatbots and voice bots to specialist domain-specific agents,IVAs have evolved from being just a feature –to becoming the products themselves.\\s\\s\nWhile metrics such as Customer Satisfaction (CSAT) and Net Promoter Score (NPS) have been leveraged by brands to assess IVA performance, they are solely focused on measuring Customer Experience (CX), which in reality is influenced by several other factors, thereby ignoring the core performance indicator of an IVA—its intelligence.\\s\\s\nSo, how exactly do you measure the intelligence of a Virtual Assistant?\\s\\s\nTo answer that question, Haptik has conceptualized the intelligenceSatisfaction Score (ISAT)– an industry-first framework to determine the “intelligence” of an IVA solution and ultimately measure its impact on customer experience at scale.\\s\\s\nThis whitepaper serves as a comprehensive guide to the ISAT framework.\\s\\s\nWho Should Read This?\\s\\s\nCustomer Experience leaders lookingto maximize customer convenience and delight\\s\\s\nDigital Transformation leaders lookingto leverage cutting-edge technology to optimize business operations and improve brand experience\\s\\s\nDigital Strategists and Innovation leads atorganizations seeking to deliver an online experience as seamless as offline\\s\\s\nHeads of Customer Service/Support tryingto enhance the efficiency and performance of their contact center operations\\s\\s\nProduct Ownerstech companies who are focused on building optimal user experiences\\s\\s\nBusiness Leaderswithin an organization aiming to improve brand affinity and profitability\\s\\s\nWhat you will learn:\\s\\s\nLimitations of existing CX metrics when it comes to measuring IVA performance\\s\\s\nThe science behind the ISAT framework, and how it works\\s\\s\nHow ISAT can derive actionable insights for your business\\s\\s\nHow ISAT can help you enhance your customer experience\n",
            "answerJson": {
              "blocks": [
                {
                  "key": "8j688",
                  "data": {},
                  "text": "Intelligent Virtual Assistants (IVA) have emerged over the last decade to address age-old pain points faced by people when interacting with businesses. From simple chatbots and voice bots to specialist domain-specific agents,IVAs have evolved from being just a feature –to becoming the products themselves.\nWhile metrics such as Customer Satisfaction (CSAT) and Net Promoter Score (NPS) have been leveraged by brands to assess IVA performance, they are solely focused on measuring Customer Experience (CX), which in reality is influenced by several other factors, thereby ignoring the core performance indicator of an IVA—its intelligence.\nSo, how exactly do you measure the intelligence of a Virtual Assistant?\nTo answer that question, Haptik has conceptualized the intelligenceSatisfaction Score (ISAT)– an industry-first framework to determine the “intelligence” of an IVA solution and ultimately measure its impact on customer experience at scale.\nThis whitepaper serves as a comprehensive guide to the ISAT framework.\nWho Should Read This?\nCustomer Experience leaders lookingto maximize customer convenience and delight\nDigital Transformation leaders lookingto leverage cutting-edge technology to optimize business operations and improve brand experience\nDigital Strategists and Innovation leads atorganizations seeking to deliver an online experience as seamless as offline\nHeads of Customer Service/Support tryingto enhance the efficiency and performance of their contact center operations\nProduct Ownerstech companies who are focused on building optimal user experiences\nBusiness Leaderswithin an organization aiming to improve brand affinity and profitability\nWhat you will learn:\nLimitations of existing CX metrics when it comes to measuring IVA performance\nThe science behind the ISAT framework, and how it works\nHow ISAT can derive actionable insights for your business\nHow ISAT can help you enhance your customer experience",
                  "type": "unstyled",
                  "depth": 0,
                  "entityRanges": [],
                  "inlineStyleRanges": [
                    {
                      "style": "UNDERLINE",
                      "length": 63,
                      "offset": 0
                    }
                  ]
                }
              ],
              "entityMap": {}
            }
          }
        ]
      }
    ],
    "search": "test",
    "language": "en",
    "countPairs": {
      "all": {
        "count": "19",
        "label": "All Questions"
      },
      "live": {
        "count": "16",
        "label": "Question in Use"
      },
      "draft": {
        "count": "03",
        "label": "Suggested List"
      }
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



