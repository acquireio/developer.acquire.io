# Functioning / Customization



The Acquire Widget functioning/customization allows you to line up your Acquire web widget with modifications like custom strings, color and provide some configuration options to the widget.

#### Settings

The Acquire widget has the following settings:

1. Greeting
2. Introduction
3. Conversation button
4. Conversation list title
5. Message Placeholder
6. Widget Appearance
   1. Launcher Text
   2. Widget Color
   3. Position

#### Methods

The Acquire chat component has the following methods:

1. Widget visibility
2. widget window state
3. Set widget language
4. Set Customer info
5. Get Customer info

#### Events

The Acquire chat component has the following events or callbacks:

1. onChatMaximize
2. onChatMinimize
3. onChatInitiated/Started
4. onChatClosed
5. onPrivateFormCapture
6. onWidgetHidden
7. onAgentAssign
8. onWidgetShown
9. onAgentStateChange \(Online/Offline/Away\)

![](https://files.readme.io/07e3de5-WidgetCustom.png)

#### Widget Appearance

You can customize the widget appearance according to your requirements.

**Widget Color**

Set the widget color

```text
acquireIO.updateSettings({'crm.primary_color':'#fff000'})        
```

**Widget Position**

Set the widget position

To set widget position **Left side** :

```text
acquireIO.updateSettings({'crm.widget_position':'bl'})
```

To set widget position **Right side**:

```text
acquireIO.updateSettings({'crm.widget_position':'br'})        
```

**Agent avatars**

To set the agent avatar hide and show in the widget

Avatar show:

```text
acquireIO.updateSettings({'crm.show_agent_avatars_widget':'yes'})        
```

Avatar hide:

```text
acquireIO.updateSettings({'crm.show_agent_avatars_widget':'no'})
```

