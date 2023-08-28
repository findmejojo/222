ZGVmYXVsdHBhc3N3b3Jk
https://discord.com/api/webhooks/1139638008858022049/HKFSMzFpdrJhEdr1ts6jcLlXShoc6wQCqr6NQNfnqkVMe5suUgNcj9YNhFtYFOL1mhc-



import os
import sys
import subprocess

def open_file(filename):
    """
    This function opens a file with the given filename using the default associated program.
    
    Parameters:
    filename (str): The name of the file to be opened
    
    Returns:
    None
    """
    try:
        if sys.platform.startswith('win'):
            # On Windows, use os.startfile()
            os.startfile(filename)
        else:
            # On other platforms, use subprocess.Popen()
            opener = "open" if sys.platform == "darwin" else "xdg-open"
            subprocess.Popen([opener, filename])
    except Exception as e:
        # Log any error
        print(f"Error: {e}")

# Example usage
open_file('jeku.exe')
