# Sentiment-Analysis-using-a-Lexicon-Approach for low resource language

Prerequisites
•	Python 3.x
•	Required Python packages: csv, pandas

Installation
No specific installation steps are required. Ensure that you have the necessary Python packages installed.

Usage
Here's an example of how to use the provided code:
python
# Load the lexicon
lexicon = load_lexicon('sentiment_lexicon.csv')

# Load test data
with open('test_tweets.csv', 'r') as test_file:
    reader = csv.reader(test_file)
    data = [['tweet'], ['Polarity']]
    for row in reader:
        MyPolarity = ' '
        tweet = row[0]
        MyPolarity = analyze_sentiment(row[0], lexicon)
        data.append([row[0], MyPolarity])

# Create a DataFrame
annotatedtweets = pd.DataFrame(data, columns=['tweet', 'Polarity'])

# Save the DataFrame to a CSV file
annotatedtweets.to_csv('my_annotated_tweets.csv')

Ensure that the lexicon file ('sentiment_lexicon.csv') and the test tweets file ('test_tweets.csv') are present in the current directory or provide the correct paths to the respective files.

