import tweepy
import random

# Set up your Twitter API credentials here
CONSUMER_KEY = "tYOWUVfvVKPSpeW9btUMJOsPW"
CONSUMER_SECRET = "3tnReAO3XSVFDT1Ks8ef8ILhPvj5LxzuIV1L0SM6gnA4yuHq0H"
ACCESS_TOKEN = "1713623578795708416-0zYQP13XQSejR8Qt9C2rnXw4epVgKH"
ACCESS_TOKEN_SECRET = "0Av3AcDTDI7JVdk6odR6lTbSkOsJyaooTANso3k0RfUat"

# Authenticate with the Twitter API
auth = tweepy.OAuthHandler(CONSUMER_KEY, CONSUMER_SECRET)
auth.set_access_token(ACCESS_TOKEN, ACCESS_TOKEN_SECRET)
api = tweepy.API(auth)

# List of custom poses (add your own!)
custom_poses = [
    "The Digital Culi",
    "The Zen Debugger",
    "The Code Sphinx",
    "The Binary Lotus",
    "The Don Culi"
    # Add more custom poses here
]

# Choose a random custom pose
chosen_pose = random.choice(custom_poses)

# Tweet the pose (you are in charge!)
api.update_status(f"🌟 Pose of the Day (by @culichi): {chosen_pose} 🌟 #CulichiBot")
print(f"CulichiBot tweeted: {chosen_pose}")
