# Summary
I remember really liking [audioscrobbler](https://en.wikipedia.org/wiki/Last.fm) back when BBS & forum posting were popular. The premise was super neat:

> I want people to see what I'm listening to *right now* within the signature field of my post. It's not the song that *was* listening to when I replied to a post, it's advertising what I am listening to *at this moment* to anyone who see's that post.

This means that I may have made a post 6 days, months, or years ago, but it will show anyone who see's that post what I am listening to *right now* 6 days/months/years later -*at this very moment*!

It had a kind of neat side-effect of making the forum feel more "alive". It wasn't just purely static text or images, it was a (kind of) real-time update feed of what I am doing *right now*.
# Setup, configuration, and operation
From what I recall, it worked something like this:
1. You go to audioscrobblers website and sign up for an account. It gives you some kind of `account_id` + the software to download.
	1. The website also instructs you how to add various big/small/whatever signatures to different forums.
2. You install audioscrobbler software on your computer
3. You enter the `account_id` it gave you
4. Audioscrobbler software says something like "It looks like you have (WinAmp, iTunes, foobar player, etc.) installed. Is this correct? Do you want me to watch that program?"
5. You tell it yes/no
	1. Or specify other install locations for different software, if you did some kind of custom install thing.
6. When audioscrobbler detects a `song - artist` is being played, it "scrobbles" that information (sends it?) to the audioscrobbler website
7. The website updates info every n seconds/minutes/hours
8. The people who entered the correct `account_id` in the software and in their forum signature now have "real time" updates in their signatures
# What you would need to do this
## For local software install
- [ ] (Used to track what songs are being played at the moment)
	- [ ] Support for various audio players
		- [ ] audio player 1
		- [ ] audio player 2
		- [ ] [...]
		- [ ] audio player 300
	- [ ] Error correction for various things
		- [ ] Bad software install
		- [ ] Corrupt download
		- [ ] Incorrect audio player detection
		- [ ] Incorrect audio player install location (they installed somewhere other than the default location, or pointed to the wrong area)
		- [ ] Crashes in general
		- [ ] Antivirus
	- [ ] Support for
		- [ ] Windows
			- [ ] 7
			- [ ] 10
			- [ ] 11
		- [ ] OSX
			- [ ] I
			- [ ] Don't
			- [ ] Know
		- [ ] Linux
			- [ ] Fedora
			- [ ] Ubuntu
			- [ ] Arch
			- [ ] Debian(?)
			- [ ] Etc.
- [ ] Website that can handle
	- [ ] Account creation
		- [ ] Password reset
		- [ ] Some form of security
	- [ ] `account_id` generation
	- [ ] Provide software to download for users
		- [ ] Suggest based on detected OS
	- [ ] Receiving information from users sending software transmission info
		- [ ] Assuming you have more than 100(?) users, bandwidth becomes a concern
		- [ ] Error handling for bad info sent to the site (but genuine)
			- [ ] Do you say something in the local install?
			- [ ] Do you send an email?
			- [ ] Do you say something on the site?
			- [ ] Can failed transmissions be "corrected" after the fact? (...And would that even make sense - it's for real-time info, right? What use does it offer to the user if they correct the fact that they played XYZ instead of ABC two weeks prior?)
		- [ ] Error handling for bad info sent to the site (malicious)
			- [ ] Suppose you have bad actors who (for whatever reason) want to try and compromise the site, going through the open public area would be an obvious attack vector. How do you sanitize the data?
- [ ] Some kind of DB of music
	- [ ] Artists
	- [ ] Song names
	- [ ] Etc.
	- [ ] For unknown stuff what do you do?
		- [ ] Allow adds to the DB?
			- [ ] Threshold?
			- [ ] Manual review?
			- [ ] Outside confirmation?
			- [ ] What if it's an indie thing that has 6 fans, but is "real"?
	- [ ] What about stuff that is real, but labeled improperly? I.e. someone transposed artist name and album name for some weird reason?
		- [ ] Offer correction through (some message vector)?
		- [ ] Auto correct and cross your fingers?
		- [ ] Do nothing and let it through?
		- [ ] Do nothing and have it fail (with notice)?
		- [ ] Do nothing and have it fail (without notice)?
	- [ ] What if it's just niche + foreign?
		- [ ] Make exceptions?
		- [ ] Include foreign support?
		- [ ] Refuse foreign support?
		- [ ] Add more DBs to include that stuff?
		- [ ] Something else?
	- [ ] Do you include stuff like photos?
		- [ ] Album artwork?
		- [ ] PR photos?
		- [ ] Live show photos?
	- [ ] Music Videos?
	- [ ] Documentaries?
	- [ ] Audiobooks?