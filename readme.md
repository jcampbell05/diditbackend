# Did It
The API for the Did it app


# Create a user
1. POST to http://139.59.184.179/api/v1/users (IP will change to URI soon)
2. POST raw data as {"name":"Legend","phone":"00000000","proto":"gcm|apns"}. 
3. Provide header of "api-secret" = 75bf2f1b372ce11b1b082b6a5b64c504be56e00fa4cfd5c8cae29fa540a4c2ec
4. You will receive a 200 response with the user data.

# Check user exitst
1. POST to http://139.59.184.179/api/v1/check (IP will change to URI soon)
2. POST raw data as {"phone":"00000000"}. 
3. Provide header of "api-secret" = 75bf2f1b372ce11b1b082b6a5b64c504be56e00fa4cfd5c8cae29fa540a4c2ec
4. You will receive a 200 response with the user data.

# Get a user
1. GET to http://139.59.184.179/api/v1/users (IP will change to URI soon)
2. Pass api-key in header as user api-key
3. You will recieve a 200 response with user.

# Update a user
1. PUT to http://139.59.184.179/api/v1/users (IP will change to URI soon)
2. PUT raw data as {"name":"###","phone":"###","proto":"###","device_token":"###"}. 
3. Pass api-key in header as user api-key
4. You will receive a 200 response with the user data.

# Upload contacts and get friends
1. POST to http://139.59.184.179/api/v1/contacts (IP will change to URI soon)
2. Pass api-key in header as user api-key
3. Pass a list of phone numbers {"numbers":["+331234123123","(+44)1234233123","00449384123123","07384123123","019384123123"]}
4. A user is friended with those users who's numbers they have and the friendships are recipricol.
4. You will get the user back and the friends

# Send a dong
1. POST to http://139.59.184.179/api/v1/send (IP will change to URI soon)
2. Pass api-key in header as user api-key
3. You will receive a 200 response with the user data.

# Reply to a dong
1. POST to http://139.59.184.179/api/v1/reply (IP will change to URI soon)
2. Pass api-key in header as user api-key
3. Pass the {"replyToID":"###","message":"####","image":"###",'sound':###} - replyToID = the user you are replying to
4. You will receive a 200 response with the user data.
 
# TODO
1. Clean up pushd when a user updates device_token