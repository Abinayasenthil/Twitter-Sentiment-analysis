# Twitter-Sentiment-analysis
import tweepy
import codecs
from tweepy import OAuthHandler
from tweepy import Stream
from tweepy.streaming import StreamListener
consumer_key = ''
consumer_secret = ''
access_token = ''
access_secret = ''
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

# Result 
'Enter the file' = Covid
Enter the nameCovid
2021-09-26 16:49:02 @BivinsJoslyn @Carrie4901 @JamesWhitaker78 @EricTopol @CDCMMWR What's the (genuine question) view in USA about how… https://t.co/E88gtAH26K
2021-09-26 16:49:02 RT @Michigan_Noah: If this is surprising, we are still thinking mild. Mild illness seems at worst unpleasant. 

Viruses are worse than that…
2021-09-26 16:49:02 RT @JCCFCanada: Vermont, with the highest vaccination rate in the country — 69% of adults fully vaccinated — has set a new record high numb…
2021-09-26 16:49:02 Children Disease Services and Network Objectives - https://t.co/L1xkBYBNG7  - ABOUT COVID - 19 to 24 (The Coronavir… https://t.co/wcGa7RTEWt
2021-09-26 16:49:02 @darrengrimes_ Middle-class layabouts always use the word "actually".  

How many people have died of covid today?… https://t.co/P3oateyd25
2021-09-26 16:49:01 #Breakingnews: Strictly Come Dancing contestant Tom Fletcher and his professional partner Amy Dowden have tested po… https://t.co/R24m06shp2
2021-09-26 16:49:01 RT @GetSprunk: Nobody had a better COVID glow up than QR codes.
2021-09-26 16:49:01 RT @Ayjchan: Both #OriginsOfCovid study committees with strong ties to EcoHealth Alliance &amp; WIV have finally been disbanded.

As many are a…
2021-09-26 16:49:01 RT @OccupyDemocrats: BREAKING: Ana Navarro destroys Trump Jr. for calling her “obese” after she tested positive for COVID,
telling him, “If…
2021-09-26 16:49:01 @ShillinNFTs 'Covid havoc' 1 of 1 only on #OpenSeaNFT  
Depicting how Covid-19 flooding over the World. Lockdown ar… https://t.co/RS68k19FxD
2021-09-26 16:49:00 RT @SeeFisch: COVID Treatment
*Asymptomatic or mild symptoms. Not hypoxic= Monoclonal antibodies
*Mildly hypoxic- Nasal Canula = Remdesivi…
2021-09-26 16:49:00 RT @Depheruk: This winter we are expecting the  EWD to be between 23,000 &amp; 52,000 due to a mixture of Fuel poverty &amp; the Cold/Covid-19 cris…
2021-09-26 16:49:00 Opinion: Misinformation about COVID-19 is a crime that should have consequences #SmartNews  https://t.co/tJETG9IyCO
2021-09-26 16:49:00 RT @JenniferNuzzo: Wow, scathing rebuke by @nytopinion editors of the Biden Administration's handling of the process around boosters and la…
2021-09-26 16:48:55 RT @erikmal: kareem has never missed https://t.co/9aUSSER1uT https://t.co/6liUgWrwIW
2021-09-26 16:48:55 RT @Bartleby_Kamoi: feel like it should be a bigger story that counties and municipalities straight up do not have control of the armed age…
2021-09-26 16:48:55 RT @oregon_mom_: I find it fascinating that the overwhelming number of people scared of COVID right now are the vaccinated. This holds true…
2021-09-26 16:48:55 RT @TDIllustration: Both our daughters caught Covid in their 2nd week of term at secondary school. One is still not well after 10 days. Why…
2021-09-26 16:48:55 Tonight at 10pm @UAERAUg P.R.O Mr. @MukundaneRonnie will be on  Radio Simba  97.3FM discussing about  Ethical Recru… https://t.co/FBIUZSgR2q
2021-09-26 16:48:55 RT @Parsleybear2010: What has the government done for us?

136k Covid deaths
Letting it into care homes
Not shutting borders on time
