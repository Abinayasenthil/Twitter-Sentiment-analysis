# Twitter-Sentiment-analysis
import tweepy
import codecs
from tweepy import OAuthHandler
from tweepy import Stream
from tweepy.streaming import StreamListener
consumer_key = 'nilmP0UP9GgSfp3S2J0pX3h0F'
consumer_secret = 'NfaGfmBED3XuiL0XOBaLPv4n3thUe8WGPIVOErMs8eLBBGxZTD'
access_token = '1440796061413429250-546WHsFUtFf8w3jczsUo7lOKiWsryD'
access_secret = 'EJoV2RtAmiY1Zhx3BVrqcPHmTJaAwoHzIEOXgxHmUVH1c'
auth = OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_secret)

api = tweepy.API(auth)
hashtag = input("Enter the name")
f = codecs.open('file.txt','w',encoding='utf-8')

for tweet in tweepy.Cursor(api.search, q=hashtag,count=10,\
                           lang="en",\
                           since_id=2021-10-26).items():
    print(tweet.created_at, tweet.text)
    f.write("%s,%s\ufeff" %(tweet.created_at, tweet.text))
f.close()
