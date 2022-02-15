
import tweepy

from credentials import *


authenticator = tweepy.OAuthHandler(api_key, api_key_secret)
authenticator.set_access_token(access_token, access_token_secret)
api = tweepy.API(authenticator,wait_on_rate_limit=True)
#
# # follow people
api.create_friendship(screen_name='Youtube')
#
# # sending twitter
api.update_status("I am using twitter")
#
#
# # find followers
user = api.get_user(screen_name="YouTube")
print(user.name)
print(user.description)

count=0
for follower in user.followers():
    print(f"{follower.name} follows {user.name}")
    count+=1
    if count==100:
        break


# search

tweets = tweepy.Cursor(api.search_tweets, q="iphone", lang="en").items(10)

for i in tweets:
    print(i.text)
