# 1 - Finding Membership ID and Membership Type

Most Bungie.net API calls require both Membership ID and Membership Type. Here's how to get them.

1. Head over to the amazing [Destiny Sets API site](https://data.destinysets.com/api/User.GetMembershipDataForCurrentUser).
1. You'll be prompted to auth with Bungie.
1. After authenticating, press "Send" and you'll see something like the following. You might have to click on the diamond next to `destinyMemberships` to see your memberships, and you may have several memberships. If you have more than one, choose the one that's the most obviously active one.

![CleanShot 2024-01-17 at 16 48 10@2x](https://github.com/rslifka/vault-zero/assets/231435/0e8b0f6a-3689-4f63-9948-815bd7e4af36)

# 2 - Finding Character IDs (OPTIONAL)

Some API calls also require a Character ID, which you can think of as uniquely identifying one of the maximum of three Guardians you can create. Now that you have your Membership ID and Membership Type, we can find our character IDs.

1. Head over to the `/GetProfile` [endpoint page](https://data.destinysets.com/api/Destiny2.GetProfile?components=200). Notice that "Characters" appears in the "components" section. This is the information that you're requesting about your profile.
1. Fill in the Membership ID and Membership Type.
1. Ensure the "OAuth access_token" checkbox is checked.
1. Press "Send".
1. You'll see something like the following, which contains all of your per-character information.

![CleanShot 2024-01-17 at 16 59 03@2x](https://github.com/rslifka/vault-zero/assets/231435/bd5c1438-b53f-4e55-ba43-92c24529ea45)

# 3 - Collecting Vault Zero Data

If we're debugging something together, I might ask for you to provide data that Vault Zero requests from Bungie on your behalf. Here is everything Vault Zero requests:

```Swift
let components = [
    102, // ProfileInventories    (Items in vault)
    200, // Characters            (Per-character data; last played, light level, etc.)
    201, // CharacterInventories  (Items on character; not equipped)
    202, // CharacterProgressions (Faction, experience, etc. "levels") relevant to each character
    204, // CharacterActivities
    205, // CharacterEquipment    (Items on character; equipped)
    300, // ItemInstances         (Light, damage type, etc.)
    301, // ItemObjectives        (For items that have objectives bound to them)
    305, // ItemSockets
    309, // ItemPlugObjectives
    900, // Records               (Status of Triumphs, Patterns, Lore, ...)
   1000, // Transitory            (Fireteam, current activity, ...)
   1200, // StringVariables       (Values substituted in to modifier text, etc.)
]
```

1. Head over to the `/GetProfile` endpoint page again, but you want to use [this link](https://data.destinysets.com/api/Destiny2.GetProfile?components=102,200,201,202,204,205,300,301,305,309,900,1000,1200), which has pre-filled all the above components.
1. Fill in the Membership ID and Membership Type.
1. Ensure the "OAuth access_token" checkbox is checked.
1. Open the Web Inspector (View > Developer > Developer Tools).
1. Click on the "Network" tab.
1. Press "Send".
1. Right-click on the network request that went out, and then save a HAR file for the request, as shown below. Then send it on over!

![CleanShot 2024-01-17 at 17 45 08@2x](https://github.com/rslifka/vault-zero/assets/231435/982f3afa-8c6b-44c4-9f78-6ccf00172b40)
