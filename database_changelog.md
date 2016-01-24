# Database Changelog

This is the Matukio database changelog, starting with version 5.3.0

###5.3.0

* Added TinyInt (bool) Parameter allday to Matukio table (Default 0)

```sql
ALTER TABLE `#__matukio` ADD `allday` TINYINT NOT NULL DEFAULT '0' AFTER `cancelled`;
```

* Added Detail image (varchar) to Matukio table


```sql
ALTER TABLE `#__matukio` ADD `image_detail` VARCHAR(255) NOT NULL DEFAULT '' AFTER `image`;
```