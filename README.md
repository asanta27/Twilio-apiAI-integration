# Twilio-apiAI-integration

This is an integration between Twilio's API, Google Voice and API.ai.

This exploit allows the Google Voice UI to be used for Twilio's API.

Here's how:

1. SMS is received on Google Voice phone number.
2. Google Voice forwards SMS to Twilio phone number.
3. SMS is split on the delimiter. Google uses the delimeter to divide the author of the SMS from the message.
4. The author of the SMS is disregarded because Twilio's API automatically replies to the sender.
5. The body of the SMS is sent as a text-query to an API.ai agent with "Small Talk" preinstalled.
6. If agent recognizes the query, it will respond with "speech".
7. "speech" response is sent to Twilio phone number.
8. Twilio forwards SMS to appropriate Google Voice "Sender ID"
9. Google Voice recieves SMS and forwards it to sender's phone number.

