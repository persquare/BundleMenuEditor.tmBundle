# BundleMenuEditor.tmBundle

Edit TextMate tmBundles' menu entries using a simple text representation

## Quickstart

The `BundleMenuEditor -> Read Menu Definition` will let you select a tmBundle, and from it will 
generate a simple text representation of the menu, e.g.:

```
@/Users/persquare/Source/TextTasks.tmbundle
# Don't change the previous line
# Rearrange lines below to rearrange menu
New Task
Toggle Status
Open Project
Archive Completed
New Project with Selection
Move Selection to Project…
List MITs
Create Reminders Entries
Help
New line
```

Now the items can be arranged and grouped into submenus. Additionally, items can be excluded from 
the menu by preceeding it with an exclamation mark (!). 

```
@/Users/persquare/Source/TextTasks.tmbundle
# Don't change the previous line
# Rearrange lines below to rearrange menu
New Task
Toggle Status
> Projects
  Open Project
  New Project with Selection
  Move Selection to Project…
<
------------------------------------
Archive Completed
List MITs
Create Reminders Entries
------------------------------------
Help
! New line
```

Choosing `BundleMenuEditor -> Write Menu Definition` will update the menu immediately 
(after creating a backup copy of the Info.plist file). 

## Caveats

Works for my purposes, no guarantees for other uses.

Only works for full source bundles, not delta-bundles. I wouldn't use it on the built-in bundles.
Menu entries starting with `#`, `!`, and `----` will misbehave unless you use the bundle settings 
to change the representation of the tokens (`MDEF_COMMENT`, `MDEF_EXCLUDE`, `MDEF_DIVIDER`).

Read the source...



