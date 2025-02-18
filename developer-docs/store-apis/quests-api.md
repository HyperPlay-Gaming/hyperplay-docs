
# Active Quests

## Get Active Quests

{% swagger method="get" path="/api/v1/quests" baseUrl="https://developers.hyperplay.xyz" summary="Get Active Quests" expanded="true" %}
{% swagger-description %}
This endpoint retrieves a list of quests that are currently in the **ACTIVE** status. It returns detailed information such as quest ID, project ID, name, type, description, rewards, and other metadata.
{% endswagger-description %}

{% swagger-parameter in="query" name="questStatus" required="true" type="string" %}
Defines the quest status to retrieve. Use "ACTIVE" to fetch only active quests.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Returns a list of active quests." %}
```json
[
  {
    "id": 685,
    "project_id": "0xe7fac1fdeae6e3f93310f04b1892145019f624811c7b39224a9c55cc4fbb0831",
    "name": "Game7 Credits: Metacene",
    "type": "PLAYSTREAK",
    "status": "ACTIVE",
    "description": "Complete one play session to earn 5 Game7 Credits!",
    "num_of_times_repeatable": 1,
    "is_test": null,
    "rewards": [
      {
        "id": 234,
        "reward_type": "EXTERNAL-TASKS",
        "name": "G7 Credits",
        "image_url": "https://gateway-b3.valist.io/hyperplay/game7passport.png"
      }
    ]
  }
]
```
{% endswagger-response %}
{% endswagger %}

### Making the Request

{% tabs %}
{% tab title="Curl Request" %}
```bash
curl --location 'https://developers.hyperplay.xyz/api/v1/quests?questStatus=ACTIVE' --header 'Content-Type: application/json'
```
{% endtab %}

{% tab title="Response Type" %}
Here is the TypeScript type for the response:

```typescript
type Quest = {
  id: number;
  project_id: string;
  name: string;
  type: string;
  status: string;
  description: string;
  num_of_times_repeatable: number;
  is_test: boolean | null;
  rewards: Reward[];
}

type Reward = {
  id: number;
  reward_type: string;
  name: string;
  image_url: string;
}
```
{% endtab %}
{% endtabs %}
