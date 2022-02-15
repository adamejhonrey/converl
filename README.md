
# Converl - (ver 1.0)

A new repository to be used as a dependency library in your project via **Android Studio**. To start, add the implementation below to your project's gradle:
`Note: The dependency is not a full-holder of all the Converl dependencies. It is only a part of the Converl library.`

```
implementation 'com.converl.dependencyrepo:database-control:1.0'
```
Don't add the implementation in your build.gradle that's outside `app` folder.

## What is database-control?

Converl database-control can be used to track, read, and write files within the users permission inside the repository itself.
Only the Converl repository admin can change a users' permission. `You can request to be able to have permission on a group folder.`

### Group Folder (GF)

It is a repository folder within Converl that manages more than 1 folder that contains other users' information. *For example:*

```
Converl-U05 (can contain an infinite user folders data)
--- User001
--- User002 !manager
--- User003
```
!manager or !mod = managing the parent folder and all other users within it

### Managing Parent Folder

As you saw on the GF's appendix above, the user that have `!manager` or `!mod` in its `perm.dat` file inside its folder can manage all users within the parent folder only.

### Changing Permission

Users that have `!manager` and `!mod` can also change a users `perm.dat` that is only limited to the following permissions:

- **!mod-lite** - rewrite files and commit with the approval of a manager
- **!tracker** - monitor behavior and logs within the parent folder
- **!read-only** - read files and see logs
- **!reporter** - giving warnings through `perm.dat` and reporting toxic files
- (or a custom one that can be made by requesting)

### database-control Support

To get coded support or help within **Android Studio**, a user can use the following code:

```
DatabaseControl.support(int, case, number)

DatabaseControl.getsupport(case, int, string)
```
Other optional code for the task follow the following:

- **.go()** - to start the task
- **.flash()** - to start the task and get logs within the repository
- **.pause()** - to pause the task
- **.kill()** - to destroy task
