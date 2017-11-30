---
title: Local Setup
taxonomy:
    category: docs
---

If want to setup the RWDocs project locally please follow these steps:
1. Download Grav skeleton [here](https://github.com/hibbitts-design/grav-skeleton-learn2-with-git-sync/archive/master.zip)
2. Extract it in your root folder
3. Go to _project root > user_ folder
4. `git clone https://github.com/rocketweb-fed/rwdocs.git`
5. Create a new admin account using:
	1. Grav CLI: `bin/plugin login new-user` or
	2. manually in _user/accounts/your_username.yaml_
	```
	password: 'password'
	email: 'youremail@mail.com'
	fullname: 'Johnny Appleseed'
	title: 'Site Administrator'
	access:
	  admin:
	    login: true
	    super: true
	```
	>>> After logging in to admin, your plaintext password will be removed and replaced by an encrypted one.
6. Setup your vhosts 
7. Log in to admin by going to _http://yourlocaladdress.com/admin_
8. Sync your repo with GitHub to make sure everything is working correctly. You can do that by clicking on a **git** link in the sidebar.  
	![Git link](git_sync.png)
	Once synced you should get a notification message in the top right corner saying:  
	> GitSync has successfully synchronized with the repository.
9. You're all set!