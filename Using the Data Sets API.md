# 1 - Finding Membership ID and Membership Type

Most Bungie.net API calls require both Membership ID and Membership Type. Here's how to get them.

1. Head over to the amazing [Destiny Sets API site](https://data.destinysets.com/api/User.GetMembershipDataForCurrentUser).
1. You'll be prompted to auth with Bungie.
1. After authenticating, press "Send" and you'll see something like the following. You might have to click on the diamond next to `destinyMemberships` to see your memberships, and you may have several memberships. If you have more than one, choose the one that's the most obviously active one.

![CleanShot 2024-01-17 at 16 48 10@2x](https://github.com/rslifka/vault-zero/assets/231435/0e8b0f6a-3689-4f63-9948-815bd7e4af36)

# 2 - Finding Character IDs

Some API calls also require a Character ID, which you can think of as uniquely identifying one of the maximum of three Guardians you can create. Now that you have your Membership ID and Membership Type, we can find our character IDs.

1. Head over to the `/GetProfile` [endpoint page](https://data.destinysets.com/api/Destiny2.GetProfile?components=200). Notice that "Characters" appears in the "components" section. This is the information that you're requesting about your profile.
1. Press "Send".
1. You'll see something like the following, which contains all of your per-character information.

![CleanShot 2024-01-17 at 16 59 03@2x](https://github.com/rslifka/vault-zero/assets/231435/bd5c1438-b53f-4e55-ba43-92c24529ea45)
