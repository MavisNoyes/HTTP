import requests

# Define the URL
url = 'https://jsonplaceholder.typicode.com/posts/1'

# Define the headers
headers = {'Content-Type': 'application/json'}

# Define the payload
payload = {'title': 'Updated Title', 'body': 'Updated Body'}

# Send a PUT request to update the resource
response = requests.put(url, json=payload, headers=headers)

# Check if the request was successful
if response.status_code == 200:
    print("Resource updated successfully.")
    print("Response:")
    print(response.json())
else:
    print(f"Failed to update resource. Status code: {response.status_code}")
