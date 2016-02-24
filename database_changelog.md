# Database Changelog

This is the Matukio database changelog, starting with version 5.3.0

### Matukio 5.3.0

* Added TinyInt (bool) Parameter allday to Matukio table (Default 0)

```sql
ALTER TABLE `#__matukio` ADD `allday` TINYINT NOT NULL DEFAULT '0' AFTER `cancelled`;
```

* Added Detail image (varchar) to Matukio table


```sql
ALTER TABLE `#__matukio` ADD `image_detail` VARCHAR(255) NOT NULL DEFAULT '' AFTER `image`;
```

* Added currency_id field to Matukio table

```sql
ALTER TABLE `#__matukio` ADD `currency_id` INT(11) NOT NULL DEFAULT '1' AFTER `tax_id`;
```

* Added additional_dates to Matukio table

```sql
ALTER TABLE `#__matukio` ADD `additional_dates` TEXT AFTER `recurring_created`;
```

* Added extra_fee_options to Matukio table

```sql
ALTER TABLE #__matukio ADD extra_fee_options TEXT AFTER different_fees_override;
```

* Added extra_fee column to Matukio Booking table

```sql
ALTER TABLE #__matukio_bookings ADD extra_fees VARCHAR(1000) DEFAULT '' NOT NULL AFTER different_fees;
```

* Added override options for Matukio recurring events
* 

```sql
ALTER TABLE `#__matukio_recurring` ADD `override_title` VARCHAR(500) NULL DEFAULT NULL AFTER `semnum`,
	ADD `override_maxpupil` INT NULL DEFAULT NULL AFTER `title`;
```

