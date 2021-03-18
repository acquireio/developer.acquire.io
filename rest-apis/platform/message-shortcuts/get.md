---
description: API to get all the shortcuts available
---

# Get

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/message-shortcut?search=acquire" path="" %}
{% api-method-summary %}
List Message Shortcuts
{% endapi-method-summary %}

{% api-method-description %}
API to get list of available message shortcuts
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API KEY
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="filterByDepartment" type="boolean" required=false %}
Specify to true/false
{% endapi-method-parameter %}

{% api-method-parameter name="select" type="array" required=false %}
List of fields to get
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="object" required=false %}
Specify the relations
{% endapi-method-parameter %}

{% api-method-parameter name="Order" type="object" required=false %}
Object specifying field name to sort followed by value. eg: {"id":"DESC"}
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
    "count": 7,
    "data": [
      {
        "id": 1,
        "shortcut_name": "Demo",
        "type": null,
        "message": "\n![](https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-2831b0ef05cfa3bb2e0ff113.png)\n**_Hello_**\n",
        "messageJson": {
          "blocks": [
            {
              "key": "7gdrt",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "7j1dl",
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
              "key": "9qdi9",
              "data": {},
              "text": "Hello",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": [
                {
                  "style": "BOLD",
                  "length": 5,
                  "offset": 0
                },
                {
                  "style": "ITALIC",
                  "length": 5,
                  "offset": 0
                }
              ]
            }
          ],
          "entityMap": {
            "0": {
              "data": {
                "alt": "",
                "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-2831b0ef05cfa3bb2e0ff113.png",
                "width": "100px",
                "height": "100px",
                "mediaKey": "WzQ3MCwibWVkaWEvMjAyMC8xMC83MWZmMzkzMDIzMWY1ZWNhOWQ2MmQ3MWU3ZDMxOTFlMS0yODMxYjBlZjA1Y2ZhM2JiMmUwZmYxMTMucG5nIiwiNW1rZzN0IiwiNzFmZjM5MzAyMzFmNWVjYTlkNjJkNzFlN2QzMTkxZTEucG5nIiwzMDE2OF0="
              },
              "type": "IMAGE",
              "mutability": "MUTABLE"
            }
          }
        },
        "messageHtml": "<p></p>\n<img src=\"https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-2831b0ef05cfa3bb2e0ff113.png\" alt=\"\" width=100px% height=\"auto\"/>\n<p><b><i>Hello</i></b></p>\n",
        "department": [],
        "groupName": ""
      },
      {
        "id": 8,
        "shortcut_name": "Saaaaa",
        "type": null,
        "message": "\n![](https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-a2693cfc36d7ecae8188b7ac.png)\n\n",
        "messageJson": {
          "blocks": [
            {
              "key": "2d5p9",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "3uejg",
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
              "key": "rtlu",
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
                "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-a2693cfc36d7ecae8188b7ac.png",
                "width": "10",
                "height": "10",
                "mediaKey": "Wzk5NSwibWVkaWEvMjAyMC8xMC83MWZmMzkzMDIzMWY1ZWNhOWQ2MmQ3MWU3ZDMxOTFlMS1hMjY5M2NmYzM2ZDdlY2FlODE4OGI3YWMucG5nIiwiNW1rZzN0IiwiNzFmZjM5MzAyMzFmNWVjYTlkNjJkNzFlN2QzMTkxZTEucG5nIiwzMDE2OF0="
              },
              "type": "IMAGE",
              "mutability": "MUTABLE"
            }
          }
        },
        "messageHtml": "<p></p>\n<img src=\"https://uat-drive.acquire.io/5mkg3t/media/2020/10/71ff3930231f5eca9d62d71e7d3191e1-a2693cfc36d7ecae8188b7ac.png\" alt=\"\" width=10% height=\"auto\"/>\n<p></p>\n",
        "department": [],
        "groupName": ""
      },
      {
        "id": 15,
        "shortcut_name": "Sample check",
        "type": null,
        "message": "Hello **_Guys_**\n\n![image](https://uat-drive.acquire.io/5mkg3t/media/2020/11/71ff3930231f5eca9d62d71e7d3191e1-3f3ddd2e5d2b0948d1c261bd.png)\n\n",
        "messageJson": {
          "blocks": [
            {
              "key": "5851b",
              "data": {},
              "text": "Hello Guys",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": [
                {
                  "style": "BOLD",
                  "length": 4,
                  "offset": 6
                },
                {
                  "style": "ITALIC",
                  "length": 4,
                  "offset": 6
                }
              ]
            },
            {
              "key": "edkih",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "ludn",
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
              "key": "8pr7u",
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
                "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/11/71ff3930231f5eca9d62d71e7d3191e1-3f3ddd2e5d2b0948d1c261bd.png",
                "width": "10",
                "height": "10",
                "mediaKey": "WzExNDIsIm1lZGlhLzIwMjAvMTEvNzFmZjM5MzAyMzFmNWVjYTlkNjJkNzFlN2QzMTkxZTEtM2YzZGRkMmU1ZDJiMDk0OGQxYzI2MWJkLnBuZyIsIjVta2czdCIsIjcxZmYzOTMwMjMxZjVlY2E5ZDYyZDcxZTdkMzE5MWUxLnBuZyIsMzAxNjhd"
              },
              "type": "IMAGE",
              "mutability": "MUTABLE"
            }
          }
        },
        "messageHtml": "<p>Hello <b><i>Guys</i></b></p>\n<p></p>\n<img src=\"https://uat-drive.acquire.io/5mkg3t/media/2020/11/71ff3930231f5eca9d62d71e7d3191e1-3f3ddd2e5d2b0948d1c261bd.png\" alt=\"\" width=10% height=\"auto\"/>\n<p></p>\n",
        "department": [],
        "groupName": ""
      },
      {
        "id": 22,
        "shortcut_name": "Only Image",
        "type": null,
        "message": "\n![image](https://uat-drive.acquire.io/5mkg3t/media/2020/11/71ff3930231f5eca9d62d71e7d3191e1-007e1c1bd68e76a4f023a31c.png)\n\n",
        "messageJson": {
          "blocks": [
            {
              "key": "96d4f",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "8i3dp",
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
              "key": "c0t9a",
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
                "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/11/71ff3930231f5eca9d62d71e7d3191e1-007e1c1bd68e76a4f023a31c.png",
                "width": "10",
                "height": "10",
                "mediaKey": "WzExNzcsIm1lZGlhLzIwMjAvMTEvNzFmZjM5MzAyMzFmNWVjYTlkNjJkNzFlN2QzMTkxZTEtMDA3ZTFjMWJkNjhlNzZhNGYwMjNhMzFjLnBuZyIsIjVta2czdCIsIjcxZmYzOTMwMjMxZjVlY2E5ZDYyZDcxZTdkMzE5MWUxLnBuZyIsMzAxNjhd"
              },
              "type": "IMAGE",
              "mutability": "MUTABLE"
            }
          }
        },
        "messageHtml": "<p></p>\n<img src=\"https://uat-drive.acquire.io/5mkg3t/media/2020/11/71ff3930231f5eca9d62d71e7d3191e1-007e1c1bd68e76a4f023a31c.png\" alt=\"\" width=10% height=\"auto\"/>\n<p></p>\n",
        "department": [],
        "groupName": "TYUYUY"
      },
      {
        "id": 28,
        "shortcut_name": "Chekssssssssss",
        "type": null,
        "message": "**This is Bold **\n\n_This is Italic_\n\n<ins>This is Underline</ins>\n\n~~This is strikethrough~~\n\n\n![image](https://uat-drive.acquire.io/5mkg3t/media/2020/12/image012-50214266604a77605fff2061-99a6f19eba7c9f1aa6bf2b9a.png)\n\n",
        "messageJson": {
          "blocks": [
            {
              "key": "fooe1",
              "data": {},
              "text": "This is Bold ",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": [
                {
                  "style": "BOLD",
                  "length": 13,
                  "offset": 0
                }
              ]
            },
            {
              "key": "2p5cr",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "1rs41",
              "data": {},
              "text": "This is Italic",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": [
                {
                  "style": "ITALIC",
                  "length": 14,
                  "offset": 0
                }
              ]
            },
            {
              "key": "cngr5",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "4s5vm",
              "data": {},
              "text": "This is Underline",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": [
                {
                  "style": "UNDERLINE",
                  "length": 17,
                  "offset": 0
                }
              ]
            },
            {
              "key": "efiug",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "8ljt0",
              "data": {},
              "text": "This is strikethrough",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": [
                {
                  "style": "STRIKETHROUGH",
                  "length": 21,
                  "offset": 0
                }
              ]
            },
            {
              "key": "3825d",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "45iu5",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "6pmic",
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
              "key": "613lm",
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
                "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/12/image012-50214266604a77605fff2061-99a6f19eba7c9f1aa6bf2b9a.png",
                "width": "25",
                "height": "25",
                "mediaKey": "WzIwMzAsIm1lZGlhLzIwMjAvMTIvaW1hZ2UwMTItNTAyMTQyNjY2MDRhNzc2MDVmZmYyMDYxLTk5YTZmMTllYmE3YzlmMWFhNmJmMmI5YS5wbmciLCI1bWtnM3QiLCJpbWFnZTAxMi01MDIxNDI2NjYwNGE3NzYwNWZmZjIwNjEucG5nIiw3MjUxXQ=="
              },
              "type": "IMAGE",
              "mutability": "MUTABLE"
            }
          }
        },
        "messageHtml": "<p><b>This is Bold </b></p>\n<br/>\n<p><i>This is Italic</i></p>\n<br/>\n<p><u>This is Underline</u></p>\n<br/>\n<p><del>This is strikethrough</del></p>\n<br/>\n<br/>\n<img src=\"https://uat-drive.acquire.io/5mkg3t/media/2020/12/image012-50214266604a77605fff2061-99a6f19eba7c9f1aa6bf2b9a.png\" alt=\"image012-50214266604a77605fff2061-99a6f19eba7c9f1aa6bf2b9a.png\" title=\"image012-50214266604a77605fff2061-99a6f19eba7c9f1aa6bf2b9a.png\" width=25% height=\"auto\"/>\n<br/>\n",
        "department": [],
        "groupName": ""
      },
      {
        "id": 29,
        "shortcut_name": "Alignments checks for this",
        "type": null,
        "message": "Irrilevant symbols\n\nGood One\n\n\n![image](https://uat-drive.acquire.io/5mkg3t/media/2020/12/0-1-07e396d1da41866e4e890a0d.jpeg)\n\n\n**One of this**\n",
        "messageJson": {
          "blocks": [
            {
              "key": "6d2nu",
              "data": {},
              "text": "Irrilevant symbols",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "34d1v",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "ai55t",
              "data": {},
              "text": "Good One",
              "type": "right",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "7dbtp",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "6h01g",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "vqsp",
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
              "key": "9ubum",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "5mb9q",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "7iqeb",
              "data": {},
              "text": "One of this",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": [
                {
                  "style": "BOLD",
                  "length": 11,
                  "offset": 0
                }
              ]
            }
          ],
          "entityMap": {
            "0": {
              "data": {
                "alt": "",
                "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/12/0-1-07e396d1da41866e4e890a0d.jpeg",
                "width": "50",
                "height": "50",
                "mediaKey": "WzIwMzMsIm1lZGlhLzIwMjAvMTIvMC0xLTA3ZTM5NmQxZGE0MTg2NmU0ZTg5MGEwZC5qcGVnIiwiNW1rZzN0IiwiMCAoMSkuanBlZyIsMzg3MTNd"
              },
              "type": "IMAGE",
              "mutability": "MUTABLE"
            }
          }
        },
        "messageHtml": "<p>Irrilevant symbols</p>\n<br/>\n\n<br/>\n<br/>\n<img src=\"https://uat-drive.acquire.io/5mkg3t/media/2020/12/0-1-07e396d1da41866e4e890a0d.jpeg\" alt=\"0-1-07e396d1da41866e4e890a0d.jpeg\" title=\"0-1-07e396d1da41866e4e890a0d.jpeg\" width=50% height=\"auto\"/>\n<br/>\n<br/>\n<p><b>One of this</b></p>\n",
        "department": [],
        "groupName": ""
      },
      {
        "id": 30,
        "shortcut_name": "sdgdg",
        "type": null,
        "message": "\\u{1f44b}\\u{1f60d}\n\n\\u{1f602}\n![image](https://uat-drive.acquire.io/5mkg3t/media/2020/12/image012-50214266604a77605fff2061-f65367479f265f80e0dbacd6.png)\n\n",
        "messageJson": {
          "blocks": [
            {
              "key": "aa8qg",
              "data": {},
              "text": "\\u{1f44b}\\u{1f60d}",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "6nrqv",
              "data": {},
              "text": "",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "8fp9k",
              "data": {},
              "text": "\\u{1f602}",
              "type": "unstyled",
              "depth": 0,
              "entityRanges": [],
              "inlineStyleRanges": []
            },
            {
              "key": "b4fs2",
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
              "key": "dpvti",
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
                "src": "https://uat-drive.acquire.io/5mkg3t/media/2020/12/image012-50214266604a77605fff2061-f65367479f265f80e0dbacd6.png",
                "width": 100,
                "height": 100,
                "mediaKey": "WzIwODAsIm1lZGlhLzIwMjAvMTIvaW1hZ2UwMTItNTAyMTQyNjY2MDRhNzc2MDVmZmYyMDYxLWY2NTM2NzQ3OWYyNjVmODBlMGRiYWNkNi5wbmciLCI1bWtnM3QiLCJpbWFnZTAxMi01MDIxNDI2NjYwNGE3NzYwNWZmZjIwNjEucG5nIiw3MjUxXQ=="
              },
              "type": "IMAGE",
              "mutability": "MUTABLE"
            }
          }
        },
        "messageHtml": "<p>\\u{1f44b}\\u{1f60d}</p>\n<br/>\n<p>\\u{1f602}</p>\n<img src=\"https://uat-drive.acquire.io/5mkg3t/media/2020/12/image012-50214266604a77605fff2061-f65367479f265f80e0dbacd6.png\" alt=\"image012-50214266604a77605fff2061-f65367479f265f80e0dbacd6.png\" title=\"image012-50214266604a77605fff2061-f65367479f265f80e0dbacd6.png\" width=100% height=\"auto\"/>\n<br/>\n",
        "department": [
          "6"
        ],
        "groupName": ""
      }
    ],
    "departmentList": {
      "list": [
        {
          "id": 6,
          "name": "eswweew "
        },
        {
          "id": 7,
          "name": "fdhfthnfgg"
        },
        {
          "id": 8,
          "name": "Youpps"
        },
        {
          "id": 9,
          "name": "robust"
        },
        {
          "id": 10,
          "name": "qwe"
        },
        {
          "id": 11,
          "name": "moi"
        },
        {
          "id": 12,
          "name": "roi"
        },
        {
          "id": 13,
          "name": "eoi"
        }
      ],
      "success": "true"
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



