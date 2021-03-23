---
description: API to get the settings based on the module
---

# Get

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/account-setting?module=crm" path="" %}
{% api-method-summary %}
Get Settings
{% endapi-method-summary %}

{% api-method-description %}
API to get the settings based on the module
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_key}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="module" type="string" required=false %}
strings separated by comma {crm,voip,mail}
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
    "after_chat_notification_visible": "no",
    "agent_mentions_notification": "yes",
    "agent_mentions_sound": "yes",
    "agent_new_call_notification": "yes",
    "agent_new_call_sound": "yes",
    "agent_new_chat_notification": "yes",
    "agent_new_chat_sound": "yes",
    "agent_new_email_notification": "yes",
    "agent_new_email_sound": "no",
    "agent_new_form_notification": "yes",
    "agent_new_form_sound": "yes",
    "agent_new_msg_notification": "yes",
    "agent_new_msg_sound": "yes",
    "agent_new_sms_notification": "yes",
    "agent_new_sms_sound": "yes",
    "agent_snooze_notification": "yes",
    "agent_snooze_sound": "yes",
    "chat_wait_notified_title": "",
    "chat_window": "circular",
    "enable_file_upload_backend": "yes",
    "enable_file_upload_frontend": "yes",
    "force_single_thread": "no",
    "form_title": "",
    "hide_widget_in_mobiles": "no",
    "hide_widget_in_web": "no",
    "language_backend": "en",
    "language_frontend": "el",
    "offline_agent_invite_mail": "yes",
    "offline_data_collect_delay": "5",
    "offline_visitor_mail_body": "",
    "offline_visitor_mail_visibility": "no",
    "online_data_collect_delay": "5",
    "permissions": {
      "value": [
        "jpg",
        "png",
        "gif",
        "bmp",
        "jpeg",
        "txt",
        "doc",
        "docx",
        "xls",
        "xlsx",
        "avi",
        "mp3",
        "mp4",
        "7z",
        "rar",
        "ai",
        "csv",
        "ppt",
        "pdf",
        "ico",
        "psd",
        "zip"
      ],
      "selected": "default"
    },
    "primary_color": "#05eaea",
    "privacy_link_mode": "no",
    "privacy_link_url": "https://5mkg3t.uat.env.acquire.io/settings/messenger-setup/chat-widget",
    "show_agent_avatars_widget": "yes",
    "show_agent_picture_in_chat": "no",
    "show_agent_picture_in_launcher": "no",
    "show_company_logo": "yes",
    "specified_session_mode": "no",
    "transcript_visitor": "yes",
    "visitor_call_popup_alert": "no",
    "visitor_new_chat_notification": "no",
    "visitor_new_chat_sound": "no",
    "visitor_new_msg_notification": "no",
    "visitor_new_msg_sound": "no",
    "visitor_offline_enable_leave_message": "no",
    "web_spell_checker": "no",
    "widget_bottom_spacing": "0",
    "widget_dark_theme": "no",
    "widget_position": "br",
    "widget_side_spacing": "0",
    "widget_state_unsave": "no",
    "communication_enable": [
      "allow_audio_call",
      "allow_video_call"
    ],
    "custom_css": " ",
    "frame_css": " ",
    "max_active_chats": "0",
    "routing_chat_queue_limit": "0",
    "routing_chat_timeout": 40,
    "routing_chat_agent_limit": "0",
    "routing_chat_policy": "assigned",
    "shortcut_key": "/",
    "operating_hours": {
      "apply": false,
      "value": []
    },
    "special_holidays": [],
    "custom_launcher_icon": [],
    "email_piping": {
      "status": "disabled",
      "value": [
        ""
      ]
    },
    "capture_private_form": "yes",
    "exclude_in_private_form": {
      "type": "exclude",
      "value": ""
    },
    "webrtc_channel": "acquire",
    "conversation_unresponsive": {
      "status": "no",
      "timeInSeconds": 120
    },
    "conversation_session_timeout": {
      "status": "no",
      "timeInSeconds": 1800
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

