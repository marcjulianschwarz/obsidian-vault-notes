How do I stop processes running on my external SSD? What is stopping my SSD from being ejected?

Use 

```bash
diskutil unmount
```

to find out which processes are blocking the ejection of the SSD.

Or use 

```bash
sudo lsof | grep /Volumes/WD
```

to list all processes currently running on the specified volume.

Also maybe one can force close finder and reopen it however this did not work for me. 

Seems like Spotlight and StoreKitAgent are the troublemakers. You can disable Spotlight indexing by adding the volume under settings -> spotlight -> privacy. However it somehow got removed by macOS sometimes.

Here is some info on a [reddit post](https://www.reddit.com/r/MacOS/comments/14qhrfy/why_cant_macos_just_tell_me_which_program_is/).

And something about metadata_never_index files:
https://www.google.com/search?q=metadata_never_index&ie=UTF-8
