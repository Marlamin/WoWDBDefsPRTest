# Contributing 

These definitions rely on the community to keep them updated. We've made the format as easy as possible for humans to edit/understand. Here's some guidelines to keep in mind when contributing:

## Column definitions (```COLUMNS```)
### Adding
#### Unverified
Are you adding new column names that you made up a name for based on an educated guess? Make sure to tag your column definition (on top) as unverified by adding a question mark after the column's name. 

#### Valid characters
Column names should only have the following characters: ```Aa```-```Zz```, ```0```-```9``` and ```_```. 
They should not contain spaces or any special character except for ```_```.

### Changing
#### Names
Column names should only be changed if the existing column name is unverified and you have a significantly better/official column name. Be sure to change the column name in the version definitions as well! If the column is verified and you're certain it is wrong, please open an issue for someone else to verify.
#### Foreign keys
Only add a foreign key if you are certain it is valid. Always check the foreign database file to see if the referenced IDs exist. When adding a foreign key reference to a filedataID, map it to FileData::ID and make sure the referenced filedataIDs exist in [root](https://wowdev.wiki/CASC#Root).
### Removing
Columns should **only** be removed from column definitions when they're not used in any of the version definitions.

### Comments
Comments shouldn't be too long. If they are better suited for spanning multiple lines, add some docs to the [wiki](https://wowdev.wiki/Main_Page) instead.
## Versions (```BUILD```/```LAYOUT```)
### Adding
Are there no changes to the structure compared to a different version? Add the build to the existing structure instead of adding a new structure.

When adding a build to an existing build range, make sure to only increase the build number x.x.x.**the number that goes here**. If the expansion, major patch or minor patch number are different add a new range. If there's no multiple builds yet, you can specify just one build.

### Changing
Changing an existing version definition should only be required in the following cases:
- Incorrect column names/order for the specified versions
- Missing primary key (no ```$id$``` on ```ID```)

### Removing
Removing a version definition should only be done when it is identical to an existing version definition. Don't forget to merge the referenced builds/layouts.

