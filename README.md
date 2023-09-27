# plex-playlist-chatgpt
I used Plex solely for music, and I wanted a way to add in playlists generated by ChatGPT. This script does that. And BTW, 95% of this script was generated by ChatGPT itself, all I really had to do was figure out what URLs to use to put the list of tracks into a playlist. That's underselling it a little bit, because it took a few hours of sleuthing and nudging ChatGPT in the right direction by feeding it XML responses from the server and training it how to extract the proper track IDs and such. But in the end, the script is legit.

It also prompts which Plex user account you want to put the script into, because using the Plex "share playlist" feature is buggy. With this script there's need to share the playlist, just put it where you want it to go. By doing it this way, the playlist is owned by the specified user, they can edit it, and it shows up in Plexamp (for some weird reason, Plexamp has no ability to show shared playlists). If you don't want that ability, see the file `alternate-main-func-for-noprompt.py` to substitute a main() function that removes the prompt and defaults to adding the playlist to the admin account.

Here's how I use it:

1) Go to https://chat.openai.com and ask ChatGPT to generate a list of songs, e.g. _Make a playlist of 5 songs from the early 2000s which are influenced by 80s synthpop. Output as ARTIST - TRACK. Don't include any "" quote marks_
2) Copy and paste this list into a text file called  `playlist.txt`
3) Run the script in the same directory as the .txt file

All you have to do is edit the top of the script to reflect the correct variables for your Plex server, and make sure all relevant Python dependencies are installed. Enjoy!
