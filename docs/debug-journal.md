# Welcome to my Debug Journal
This journal will document the errors I encounter and how I approached fixing them.

## ERROR: User namespaces are not usable by BitBake, possibly due to AppArmor.  See https://discourse.ubuntu.com/t/ubuntu-24-04-lts-noble-numbat-release-notes/39890#unprivileged-user-namespace-restrictions for more information. 

This error was presented while working in the BitBake build environment. I was attempting to inspect all of the recipes assosciate with core-image-minimal and this error popped up. I read the message and gathered that BitBake lacked permissions for user namespaces on ubuntu and based on the documentation provided with the link in the message it sounds like you can fix that issue by utilizing AppArmor.

### Solution
Write an AppArmor profile that permits BitBakes Cooker function to work with user namespaces
