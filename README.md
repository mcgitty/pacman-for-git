# pacman-for-git
Facilitate installing pacman in [Git for Windows](https://github.com/git-for-windows/git/releases), started from this [StackOverflow answer](https://stackoverflow.com/a/65204171).

## How to Update version-tags.txt

Each release adds a new *package-versions-X.YY.Z.txt* file in the [versions](https://github.com/git-for-windows/build-extra/tree/main/versions) folder of the *build-extra* project. Open that version file and copy the line starts with "mingw-w64-x86_64-git " (a space immediately after the 't'). For example,

    mingw-w64-x86_64-git 2.39.1.1.b03dafd9c2-1

Paste that as a new line in the *version-tags.txt* file. Paste it to another new line for the 32-bit version and replace 'x65_64' with 'i686'. For example,

    mingw-w64-i686-git 2.39.1.1.b03dafd9c2-1

Click and open this [release](https://github.com/git-for-windows/git/releases) page and find that version. Hover on the release date on the left hand column (above the git-for-windows-ci icon) to get the exact date and time of the release. For example,

    Jan 17, 2023, 10:05 AM PST

Open this [64-bit SDK commit history](https://github.com/git-for-windows/git-sdk-64/commits/main) page. Find the commit ID with a date and time closest to but before the release time. Hover on the date after the word "committed" or "committed on" to get the exact date and time. For example, a commit on 'Jan 17, 2023, 7:07 PM PST' is the wrong one for the above release date. Copy the commit ID and append it with a space to the new 'x86_64' line in *version-tags.txt*.

Open this [32-bit SDK commit history](https://github.com/git-for-windows/git-sdk-32/commits/main) page. Find the commit ID with a date and time closest to but before the release time. Copy the commit ID and append it with a space to the new 'i686' line in *version-tags.txt*.
