<img src='input/media/posts/1/favicon.png' style='height:5em;max-width:100%;' title='SLSIG Icon' />

# SLSIG Website Source

The source repo for the SLSIG site.


---


## CONTRIBUTING

The Publii static website editor is needed to edit/build the website.
Some familiarity with [Publii](https://getpublii.com) and basic web dev is assumed.

### Getting Started

For new contributors, perform a clone of the repository via your preferred Git client.
You want to clone it to your main publii folder: `~/Documents/Publii/sites/`.
`git clone https://github.com/SLSIG/slsig-src slsig`

Once the repository has successfully downloaded, open Publii and ignore any prompts to create a new site.
From the sites dropdown at the top of Publii, ensure SLSIG is the current site.
Click on "Preview your changes" at the bottom-left of Publii to build and show a local preview of the site in your Web Browser.
Ensure that the site is the latest version, then start modifying files.

Use a `.gitignore` file in the `~/Documents/Publii/sites/slsig/` folder to ignore specific files:
```
*.swp
output/*
preview/*
```

These files will be ignored when you commit changes via Git.
All changes should focus on the source material under `~/Documents/Publii/sites/slsig/input/`.
This is why you always press "Preview your changes" when downloading or refreshing the SLSIG site.
When the changes are to your satisfaction, press "Sync your website" at the bottom left of Publii.
The changes you've made will be rebuilt and sent to the web server.
Wait around 1-5 minutes for Github to apply the updates to the website.


### Updating to Latest Changes

Keep track of the latest site changes at `https://github.com/SLSIG/slsig-src`.
Before you make any new changes, always run a `git pull` in git to ensure it syncs any new changes with yours.
If git says you're already up to date, you can make changes without any worries or conflicts.
If there are conflicts (you and another updated the same file with different changes), coordinate with the other contributor and merge any changes.

Stage and commit all changes with a specific message detailing what changes you've made.
Messages like "Updated site images" is not descriptive enough.
Use messages like "Updated site background images", "Added new conference images to gallery", "Updated main/meeting pages with latest meeting information", etc.

Once all changes are successfully committed, use `git push` to push all changes to the website repository.


---


## GUIDELINES

To see detailed examples inside Publii of how to format the site and its many parts, look under the "Notes" page in Publii.


### Meeting Notes

All meeting notes are archived and stored in Publii's `sites/slsig/input/media/files/` folder.
Meeting agendas, previous meeting notes, and current meeting notes are all to be included inside a compressed `.zip` file folder.
The `.zip` format is the most compatible format across devices.
Name the notes with the following conventions: `SLSIG-agenda-<meeting-date>.zip` where `<meeting-date>` is a date formatted as `YYmmdd`.

If any new files surrounding the meeting circulate, add them to the archive and make sure to stage, commit, and push all changes via git.
Avoid storing audio, video, or any other large media files with git.
Only store text and documents.
Store larger media on a website such as Youtube, Spotify, Google Drive, or any other media platform of your choice.
Ensure that these media uploades are publicly accessbile for members and linked at the Events page.

When you move a meeting on the Events page from Upcoming to Previous, follow the existing conventions and create an "external" link from the date to `media/files/meeting-archive.zip` where `meeting-archive` is the proper `.zip` file name.
Also use external links for all links to social media and cloud storage sites.


### Contact Form

The contact form uses [`https://postmail.invotes.com/`](https://postmail.invotes.com/) which provides a key to use.
This allows 25 emails per day to be sent free.
Any attempts over 25 will not be allowed.
Postmail is used to send the simple, automated emails for the "Contact Us!" form.
If you are updating postmail, get the generated code and click on the `<script>` button in Publii.
The page will turn into HTML, find the Contact form and change the `access_token`'s `hidden` value to the key provided by Postmail.
All Contact form emails should forward to the new address after you properly commit and push the changes in git.


---


For a more detailed understanding of how to collaborate via git, check out the documentation at https://git-scm.com/
For a more in-depth guide on using Publii, check out https://getpublii.com/
