# SemanticScuttle

SemanticScuttle is a social bookmarking tool experimenting with new features like structured tags and collaborative descriptions of tags. Originally a fork of Scuttle, it has overtaken its ancestor in stability, features and usability.

## Features
  * LDAP/Active Directory authentication
  * RSS feed support: global feed, user feeds, per-tag feeds, private feeds
  * Public and private bookmarks
  * Delicious and Browser bookmark import
  * Theming support
  * Firefox plugin

## Origin

  * https://sourceforge.net/projects/semanticscuttle/
  * https://github.com/cweiske/SemanticScuttle

# Installation

Follow the [Standard installation
instructions](http://semanticscuttle.sourceforge.net/docs/INSTALL.html#standard-installation-instructions)
in the SemanticScuttle documentation.

### IMPORTANT!

The following SQL statements may be needed after installation to allow
creation of new bookmarks.  If applying after bookmarks have been added,
also manually reset both column values to NULL where value is zero.

```sql
ALTER TABLE `sc_bookmarks` CHANGE `bVoting` `bVoting` INT(11)  NULL  DEFAULT NULL;
ALTER TABLE `sc_bookmarks` CHANGE `bVotes` `bVotes` INT(11)  NULL  DEFAULT NULL;
```
