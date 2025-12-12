# initial_user_list.py
import requests

# Define a URL for a dummy API (JSON Placeholder)
API_URL = "https://jsonplaceholder.typicode.com/posts/1"

try:
    # Perform the GET request
    response = requests.get(API_URL)

    # Raise an HTTPError for bad responses (4xx or 5xx)
    response.raise_for_status()

    # If successful, print the status and the start of the content
    data = response.json()
    print(f"API Call Successful. HTTP Status: {response.status_code}")
    print(f"Title: {data.get('title')}")

except requests.exceptions.HTTPError as err_http:
    # Handle HTTP errors (e.g., 404 Not Found)
    print(f"HTTP Error Occurred: {err_http}")

except requests.exceptions.ConnectionError as err_conn:
    # Handle connection errors (e.g., no internet connection)
    print(f"Connection Error Occurred: {err_conn}")

except Exception as err:
    # Handle other unexpected errors
    print(f"An Unexpected Error Occurred: {err}")
