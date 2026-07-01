# user_api_finder

import requests

response = requests.get("https://jsonplaceholder.typicode.com/users")
#Download all
users = response.json()
#print all users 
for user in users:
    print(user['name'])


user_id = int(input("Enter the user Id : "))

found=False
# it must have the int and user add to valid name
for user in users:
    if user["id"] == user_id:
        print(f"the user {user['name']}")
        found = True
        break
else:
     print('theres no mame valid -')
