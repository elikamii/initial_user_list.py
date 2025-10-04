# initial_user_list.py
# initial_user_list.py

def fetch_initial_users():
    """Returns a list of core system administrators."""
This commit introduces the foundational Python script, `initial_user_list.py`. 
It serves as a simple utility to list the predefined core administrator accounts 
required for system setup.

Future updates will focus on connecting this to a secure configuration management 
system rather than hardcoding.
if __name__ == "__main__":
    print("Fetching initial setup users:")
    for user in fetch_initial_users():
        print(f"- {user}")
