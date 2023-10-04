# Frequently Asked Questions (FAQ)

#### How to compare two branches (or commits)?
Just select them (hold <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> for multiselection)

#### I accidentally lost some commits
Use reflog to see lost commits

#### Do you plan to support Linux
No, we don’t plan to support Linux until a decent UI library (comparable to WPF or Cocoa) appears on this platform.

#### How can I commit and push?
Hold <kbd>Ctrl</kbd>/<kbd>Alt</kbd> when commit

#### Git doesn’t recognize my file as a text and Fork doesn’t show the diff
This may happen when a file is relatively small or in UTF-16 LE encoding. You can fix this by creating a rule (e.g. `*.sql       text`) in `.gitattributes` file. (https://www.git-scm.com/docs/gitattributes)

#### How can I push multiple branches at once
Select them on the sidebar and call 'Push' from the context menu

#### Permission denied when accessing repos in my organization on GitHub
Ensure that Fork has access to your organization: https://github.com/settings/connections/applications/debde513eaa447b74d51

#### Receiving a "request requires higher privileges" error when trying to connect to GitLab with personal access token
Ensure the token provides access to the following scopes: `read_api`, and `user_api`

#### The main window is blank (Windows)
Most likely you are using VMWare which has a problem with hardware acceleration. You can disable it in Fork config: https://github.com/ForkIssues/TrackerWin/issues/491#issuecomment-546605221

#### I can't initialize Git-Flow (Mac)
Probably you removed SourceTree recently and it broke your environment. https://github.com/fork-dev/Tracker/issues/418#issuecomment-425818588

#### I have a large repo and Fork shows only 50000 commits
You can configure the limit.
On Mac run `$ defaults write com.danpristupov.fork maxCommitCount 150000` in Terminal.
On Windows edit the `MaxCommitCount` field in the `%localappdata%\fork\settings.json` file.
