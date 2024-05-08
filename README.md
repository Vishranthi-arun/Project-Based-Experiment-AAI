<H3>ENTER YOUR NAME : VISHRANTHI A</H3>
<H3>ENTER YOUR REGISTER NO : 212221230124</H3>
<H3>DATE:06.05.2024</H3>
<H1 Align="center">Project Based Experiment<H1>

### Objective:

Perform sentiment analysis using your Facebook data and filter the data that has only neutral feedback for the code given in the following link.
  
### Program:
```
import pandas as pd
from textblob import TextBlob

# Load your Facebook data from CSV into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Filter the DataFrame to include only rows with neutral sentiment
neutral_feedback = df[df['Sentiment'] == 0]  # Sentiment polarity of 0 indicates neutral sentiment

# Output the neutral feedback
print("Neutral Feedback:")
print(neutral_feedback)

```
### Output: 
![image](https://github.com/Lakshmipriya-P-AI/Project-Based-Experiment-AAI/assets/93427923/69ff179a-46b3-428e-95b1-044a0d1502d6)
![image](https://github.com/Lakshmipriya-P-AI/Project-Based-Experiment-AAI/assets/93427923/e678c0f7-3ab8-43b5-b9ca-ca4bf2975248)

### Inference:
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only neutral feedback for the code is done.
