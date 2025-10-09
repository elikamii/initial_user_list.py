# initial_user_list.py

def fetch_initial_users():
    """Returns a list of core system administrators."""
    return ["Alice_Admin", "Bob_DevOps", "Charlie_Security"]

def check_service_status(service_name: str) -> str:
    if service_name.lower() == "auth_server":
        return "Status: UP (Health Check Passed)"
    else:
        return f"Status: DOWN or NOT_FOUND for {service_name}"

if __name__ == "__main__":
    print("Fetching initial setup users:")
    for user in fetch_initial_users():
        print(f"- {user}")
    
    # New check added
    print("\nChecking vital service status:")
    print(check_service_status("Auth_Server"))
