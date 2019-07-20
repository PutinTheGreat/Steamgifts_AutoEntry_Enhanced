# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

- N/A

## [1.0.0] - 2017.04.21-0400

### Added

- Added a button by each giveaway to open the Auto Entry settings window and fill in the game name. All that has to be clicked is the "add" button then save. Also added code to allow it to work with ESG script with infinite page scrolling. (so much easier then copy pasting)
- Added a checkbox to "Enter free giveaways". (cause why not)
- Added a checkbox to "Enable Auto Entry on page load". This only applies to the homepage for steamgifts, https://www.steamgifts.com/, this way other steamgifts pages can be tabbed to without issue.
- Added input box for "Default Max Entries". So if you want to set 5 it only needs to be entered once.
- Added input box for "Max Page Number". This one already existed in the code but i just made an input to easily change it.
- Added input box for "Min Point Increase Page". This overrides the "Max Page Number" if you have more points then whats entered in this one. ex. You have "Max Page Number"=8 and you have "Min Point Increase Page"=200 and you have 250 points this will allow it to search above the 8 pages so you don't hit the 300 point cap. Can be turned off by setting to 300 points.

### Changed

- Fixed "Enter featured giveaways", it appeared to do nothing for me. So i made the checkbox when check enter every featured giveaway.
- Stops searching pages if no giveaways but featured ones are on it.
- Fixed the settings and other div windows, for me at least they were not loading in center of window as i scrolled down page. They would move downward so i wouldn't even be able to see them unless i was at top of page.
- Fixed a log entry saying reached entry limit when set to 0. Using 0 as a blacklist for featured giveaways in case you already won them. Just add to gamelist and set max entries to 0, this works for other games you have won as well.
- Also a little work is needed to make the checkboxes look/fit nicely in the settings div window.

## [2.0.0] - 2017.07.21-0506

### Changed

- Updated donations link.

## [3.0.0] - 2017.07.26-0000

### Changed

- Minor text change and version correction and adding additional info.

## [4.0.0] - 2017.07.26-1619

### Added

- Added button to enter giveaway next to add to game list.
- Added giveaway time checking, will remove enter giveaway button if giveaway ended and mark it as ended.
- Added some error handling.

### Changed

- Changed page check for autoenable running to regex.
- Fixed blacklisting a giveaway if wishlist or group entering is checked. (I believe)
- Fixed level checking for some giveaways.
- Fixed clickable area for restore/close buttons, now only button is clickable not whole width of window.

### Base Update

- Updated base code version from v19 to v24 below features added due to update. v21 Should prevent ever having 300 points unless max points is set to 300 in settings by entering random giveaways.
- v20 Added error catching when game name isn't a valid Regular Expression. My previous code fixed most issues.
- v21 Added some more settings. If points are available, enter giveaways with the best chance of winning. Added watchdog timer to restart auto entry if anything goes wrong. (No Change to setting max page as i already had in my previous version.)
- v22 Added option to determine the order to enter giveaways.
- v23 Added option to enter giveaways ending soonest first.
- v24 Fixed watchdog timer.

## [5.0.0] - 2017.07.31-0200

### Changed

- Fixed bug when Entering Group Giveaways was enabled it wouldn't check for normal giveaways.

## [6.0.0] - 2017.08.10-0935

### Changed

- Fixed bug, hopefully, where it would search endlessly and never find anything. This issue occured frequently if max page count was overridden. Bug was introduced in v4.

## [7.0.0] - 2017.08.12-0935

### Changed

- Fixed output from v6 fix where everytime no giveaways were found it would mark as if the issue was found, just added a counter to make sure its found once.
- Changed fix code from v6 to work on pages before the maximum pages as well, only useful really if maxpagenum is large.

## [8.0.0] - 2017.08.16-1951

### Added

- Added css to affect enter giveaway button size and fix menu to top of screen as scroll down the page. Had in external css style sheet so now its integrated. Works with ESG, however, i'd recommend turning off ESG Enter Giveaway buttons.

### Changed

- Fixed regular expression pattern on setting page, error shouldn't pop up in log now.
- Fixed Add Game To List button functionality.

## [9.0.0] - 2019.07.18-0511

### Added

- Added currently owned games to game blacklist, to prevent winning an owned game.

### Changed

- Fixed settings div position on page window resize.
- Fixed watchdogtimer check.
- Changed default enabled when viewing page to false.
- Changed addgametolist timer do to issue.

## [10.0.0] - 2019.07.18-0535

### Changed

- Replaced element sensor for use with ESG to work in new Firefox versions

### Base Update

- Updated base code version from v24 to v26. This removes the xframe dependency and allow it to run on new browser versions better.

## [10.0.1] - 2019.07.19-2247

### Changed

- Stop/Start timer depending on if you are currently viewing the giveaway page.
- Stopped timers from running on non giveaway pages.

## [10.0.2] - 2019.07.20-1109

### Changed

- Updated SteamGifts site max points settings from 300 to 500, old site change but got missed.
- Updated default max points to reflect the site max points change.
