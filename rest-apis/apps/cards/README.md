# Cards

Custom cards allow data display of other systems to be shown within the unified view of the Acquire. Acquire cards appear within the middle and right-hand positions of the dashboard. Using this feature, custom apps can create a card to display data info on contact.  
Acquire has 2 types of cards [app-custom-cards](https://github.com/acquireio/custom-cards#app-custom-card) and [manual-cards](https://github.com/acquireio/custom-cards#manual-card). Once the Acquire card is configured correctly, your external system information will appear in the Acquire Agent's dashboard.

* [Interaction-cards](interaction-cards-middle/) \(Middle of agent dashboard\)
* [General-cards](general-cards-right-side.md) \(Right-side of agent dashboard\)

{% hint style="success" %}
**See the** [**Acquire card**](https://github.com/acquireio/custom-cards) **documentation for more details and setting up cards.**
{% endhint %}

### CARD JSON OBJECT SCHEMA:

| Key | Type | description |
| :--- | :--- | :--- |
| `type` | `string` | block - action - **tab** - The tab renders a card on the right side of the dashboard as part of the app. script\_tags - style - |
| `display_scope` | `string` | home - contact\_action - case\_action - message\_action - picker - main \(for other\) - |
| `config` | `json` | The config object is described in the table below. |
| `submit_sheet_url` | `json` | Success |
| `area` | `enum` | backend - frontend - |

### 

### CARD CONFIG JSON SCHEMA:

| Key | Type | description |
| :--- | :--- | :--- |
| `event` | `json` | desc goes here |
| `canvas` | `json` | label - canvas - action\_key - action\_type - iconImageUrl - |
| `action_key` | `string` | desc goes here |
| `action_type` | `string` | desc goes here |
| `iconImageUrl` | `string` | desc goes here |
| `appInfo` | `json` | Success |
| `availability` | `json` | Success |
| `can_edit` | `bool` | desc goes here |
| `can_initialize` | `bool` | desc goes here |
| `can_submit` | `bool` | desc goes here |
| `can_submit_sheet` | `bool` | desc goes here |
| `can_configure` | `bool` | desc goes here |
| `can_options` | `bool` | desc goes here |
| `order` | test | test |

