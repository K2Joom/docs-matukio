# Database Changelog

This is the Matukio database changelog, starting with version 5.3.0

###5.3.0

* Added TinyInt (bool) Parameter allday to Matukio table (Default 0)

```sql
ALTER TABLE `#__matukio` ADD `allday` TINYINT NOT NULL DEFAULT '0' AFTER `cancelled`;
```
