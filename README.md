# initial_user_list.py
# initial_user_list.py

def fetch_initial_users():
    """Returns a list of core system administrators."""
    return ["Alice_Admin", "Bob_DevOps", "Charlie_Security"]

if __name__ == "__main__":
    print("Fetching initial setup users:")
    for user in fetch_initial_users():
        print(f"- {user}")
