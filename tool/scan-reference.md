---
description: Screenshare Tool website scan reference
---

# Scan Reference

## Scan IDs `const READ-ONLY`

Scan IDs are our way to identify scans.\
They are 12 bytes long strings but often shortened to 4-6 bytes so the panel doesn't look clunky\
You **can not** modify them in any way and are permanently linked to your account unless you request a removal or we decide to remove them

## Versions `const READ-ONLY`

In order to offer backwards compatibility with older Companion versions we store a number _often _followed by a letter (`a`, `b` or `s`).\
Hotfixes are represented with an `f` at the end

| Letters | Meaning                                                                                                                                                                                                                                                      | Example     |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------- |
| a       | Alpha versions, not production ready. Should not be available to anyone but Developers                                                                                                                                                                       | 1.4.1**a**  |
| b       | Beta versions, somewhat production ready. They are available to users who are enrolled in our **Beta Testing program** (we announce on our Discord whenever your help is needed). This releases will most likely contain bugs, that is why we separate them. | 1.4.1**b**  |
| s       | Stable releases. Ready for production and available to everyone                                                                                                                                                                                              | 1.4.1**s**  |
| _none_  | When a version is not followed by any letter it usually means it is a Stable release                                                                                                                                                                         | 1.4.1       |
| (x)f    | Hotfixes. Whenever we need to urgently update the latest version usually due to bugs that only happen on certain machines we were not able to test                                                                                                           | 1.4.1s**f** |

## Status `READ-ONLY`

Status is pretty straightforward, it is modified by the server and reflects what your scan status is.\
The following table shows the possible statuses the website might display

| Icon                                                                                                                                                                                          | Status      | Meaning                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| ![](../.gitbook/assets/clock-solid.svg)                                                                                                                                                       | Unused      | PIN has not been used yet                                                                                                                 |
| ****![](https://gblobscdn.gitbook.com/assets%2F-MfAS_KdjpojWCPXDQMV%2F-MfFa4Xbsloh0nhZNRTT%2F-MfFcD9XpaMrQYsRAXB4%2Fdownload-solid.svg?alt=media\&token=04d03498-6176-4480-8b5e-bc5677da295c) | Downloaded  | PIN has been used to download Companion's executable through the website                                                                  |
| ![](../.gitbook/assets/search-solid.svg)                                                                                                                                                      | In progress | Handshake between the server and Companion's executable has been completed and it is scanning. At this point, the PIN is no longer usable |
| ![](../.gitbook/assets/check-solid.svg)                                                                                                                                                       | Completed   | The scan has been completed.                                                                                                              |
| ![](../.gitbook/assets/times-solid.svg)                                                                                                                                                       | Error       | There was an error while Companion scanned the user for cheats. You might be able to see the results anyway, depending on the error       |

