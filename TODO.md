# Todo List

This list was generated by a conversation with ChatGPT before being tweaked & updated

## Initialization
- [X] Define the required libraries and modules
  - __selenium__ for signing in/automating browsing
  - __sqlite3__ for managing the database
  - __re__ for helping to parse the scraped data
- [X] Set up the directory structure for your application
  - __bcdl_new.py__ the script
  - __bcdl_new.db__ the album database
  - __bcdl.py__ the old script (for reference)
  - __user_pass__ file to read user/pass from for debug
  - __debug_log__ debug information is printed to it
  - __./downloads/__ where the zip files end up
  - __README.md__ simple readme
  - __TODO.md__ this file
- [X] Initialize the database where you will store the purchased music information
  - __create_db()__ function does this

## Login
- [X] Implement the functionality to sign into Bandcamp
- [ ] Store the user's login credentials in a secure way
  - Currently only uses debug login

## Scrape Information
- [X] Scrape the information about the purchased music from the user's Bandcamp account
  - Currently scrapes *Artist*, *Album*, *Download Page*, *Popularity*, and whether or not the album is listed as *Private*
  - [ ] Explore what other information can be scraped
- [X] Store this information in the database
  - __add_to_db(...)__ and __dl_page_in_db(download_page)__ both implemented

## Search Functionality
- [ ] Implement the search functionality that allows the user to search for albums based on certain criteria
- [ ] Return the search results to the user

## Download & Unzip Functionality
- [ ] Implement the functionality to download one or several albums
- [ ] Implement the functionality to unzip the zip files
- [ ] Store the zip files in a designated folder
  - Either in the working directory, or in a user-supplied location (ie: /mnt/Music/Artist/Album)

## User Interface
- [ ] Create a user interface that allows the user to interact with the application
  - The plan is for pacman-like interaction
- [ ] Implement the functionality to perform each step of the process through the user interface
  - In other words, implement all of the command-line arguments