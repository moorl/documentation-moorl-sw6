# documentation-moorl-sw6
Documentation of Shopware 6 Plugins and Themes by Moorleiche

SELECT `product`.`id` as `product.id`, `product`.`version_id` as `product.versionId`, `product`.`parent_id` as `product.parentId`, `product`.`parent_version_id` as `product.parentVersionId`, `product`.`child_count` as `product.childCount`, `product`.`blacklist_ids` as `product.blacklistIds`, `product`.`whitelist_ids` as `product.whitelistIds`, `product`.`auto_increment` as `product.autoIncrement`, `product`.`active` as `product.active`, `product`.`stock` as `product.stock`, `product`.`available_stock` as `product.availableStock`, `product`.`available` as `product.available`, `product`.`variant_restrictions` as `product.variantRestrictions`, `product`.`display_group` as `product.displayGroup`, `product`.`configurator_group_config` as `product.configuratorGroupConfig`, `product`.`product_manufacturer_id` as `product.manufacturerId`, `product`.`product_manufacturer_version_id` as `product.productManufacturerVersionId`, `product`.`unit_id` as `product.unitId`, `product`.`tax_id` as `product.taxId`, `product`.`product_media_id` as `product.coverId`, `product`.`product_media_version_id` as `product.productMediaVersionId`, `product`.`price` as `product.price`, `product`.`manufacturer_number` as `product.manufacturerNumber`, `product`.`ean` as `product.ean`, `product`.`product_number` as `product.productNumber`, `product`.`is_closeout` as `product.isCloseout`, `product`.`purchase_steps` as `product.purchaseSteps`, `product`.`max_purchase` as `product.maxPurchase`, `product`.`min_purchase` as `product.minPurchase`, `product`.`purchase_unit` as `product.purchaseUnit`, `product`.`reference_unit` as `product.referenceUnit`, `product`.`shipping_free` as `product.shippingFree`, `product`.`purchase_price` as `product.purchasePrice`, `product`.`mark_as_topseller` as `product.markAsTopseller`, `product`.`weight` as `product.weight`, `product`.`width` as `product.width`, `product`.`height` as `product.height`, `product`.`length` as `product.length`, `product`.`release_date` as `product.releaseDate`, `product`.`category_tree` as `product.categoryTree`, `product`.`property_ids` as `product.propertyIds`, `product`.`option_ids` as `product.optionIds`, `product`.`tag_ids` as `product.tagIds`, `product`.`listing_prices` as `product.listingPrices`, `product`.`rating_average` as `product.ratingAverage`, `product`.`delivery_time_id` as `product.deliveryTimeId`, `product`.`restock_time` as `product.restockTime`, `product.tax`.`id` as `product.tax.id`, `product.tax`.`tax_rate` as `product.tax.taxRate`, `product.tax`.`name` as `product.tax.name`, `product.tax`.`custom_fields` as `product.tax.customFields`, `product.tax`.`created_at` as `product.tax.createdAt`, `product.tax`.`updated_at` as `product.tax.updatedAt`, `product`.`created_at` as `product.createdAt`, `product`.`updated_at` as `product.updatedAt`, (SELECT GROUP_CONCAT(HEX(`product.categories.mapping`.`category_id`) SEPARATOR '||')↵                  FROM `product_category` `product.categories.mapping`↵                  WHERE `product.categories.mapping`.`product_id` = `product`.`id` AND `product.categories.mapping`.product_version_id = `product`.version_id ) as `product.categories.id_mapping`, (SELECT GROUP_CONCAT(HEX(`product.options.mapping`.`property_group_option_id`) SEPARATOR '||')↵                  FROM `product_option` `product.options.mapping`↵                  WHERE `product.options.mapping`.`product_id` = `product`.`id` ) as `product.options.id_mapping`, `product.unit`.`id` as `product.unit.id`, `product.unit`.`created_at` as `product.unit.createdAt`, `product.unit`.`updated_at` as `product.unit.updatedAt`, `product.unit.translation`.`short_code` as `product.unit.translation.shortCode`, `product.unit.translation`.`short_code` as `product.unit.shortCode`, `product.unit.translation`.`name` as `product.unit.translation.name`, `product.unit.translation`.`name` as `product.unit.name`, `product.unit.translation`.`custom_fields` as `product.unit.translation.customFields`, `product.unit.translation`.`custom_fields` as `product.unit.customFields`, `product.unit.translation`.`created_at` as `product.unit.translation.createdAt`, `product.unit.translation`.`updated_at` as `product.unit.translation.updatedAt`, `product.unit.translation`.`unit_id` as `product.unit.translation.unitId`, `product.unit.translation`.`language_id` as `product.unit.translation.languageId`, (SELECT GROUP_CONCAT(HEX(`product.forms.mapping`.`moorl_form_id`) SEPARATOR '||')↵                  FROM `product` `product.forms.mapping`↵                  WHERE `product.forms.mapping`.`product_id` = `product`.`id` ) as `product.forms.id_mapping`, `product.translation`.`meta_description` as `product.translation.metaDescription`, `product.translation`.`meta_description` as `product.metaDescription`, `product.translation`.`name` as `product.translation.name`, `product.translation`.`name` as `product.name`, `product.translation`.`keywords` as `product.translation.keywords`, `product.translation`.`keywords` as `product.keywords`, `product.translation`.`description` as `product.translation.description`, `product.translation`.`description` as `product.description`, `product.translation`.`meta_title` as `product.translation.metaTitle`, `product.translation`.`meta_title` as `product.metaTitle`, `product.translation`.`pack_unit` as `product.translation.packUnit`, `product.translation`.`pack_unit` as `product.packUnit`, `product.translation`.`custom_fields` as `product.translation.customFields`, `product.translation`.`custom_fields` as `product.customFields`, `product.translation`.`created_at` as `product.translation.createdAt`, `product.translation`.`updated_at` as `product.translation.updatedAt`, `product.translation`.`product_id` as `product.translation.productId`, `product.translation`.`language_id` as `product.translation.languageId`, `product.translation`.`product_version_id` as `product.translation.productVersionId` FROM `product` LEFT JOIN `product_translation` `product.translation` ON `product.translation`.`product_id` = `product`.`id` AND `product.translation`.`language_id` = ? AND `product.translation`.`product_version_id` = `product`.`version_id` LEFT JOIN `tax` `product.tax` ON `product`.`tax_id` = `product.tax`.`id` LEFT JOIN `unit` `product.unit` ON `product`.`unit_id` = `product.unit`.`id` LEFT JOIN `unit_translation` `product.unit.translation` ON `product.unit.translation`.`unit_id` = `product.unit`.`id` AND `product.unit.translation`.`language_id` = ? WHERE (`product`.`version_id` = ?) AND (`product`.`whitelist_ids` IS NULL) AND (`product`.`id` IN (?))' with params ["\x2f\xbb\x5f\xe2\xe2\x9a\x4d\x70\xaa\x58\x54\xce\x7c\xe3\xe2\x0b", "\x2f\xbb\x5f\xe2\xe2\x9a\x4d\x70\xaa\x58\x54\xce\x7c\xe3\xe2\x0b", "\x0f\xa9\x1c\xe3\xe9\x6a\x4b\xc2\xbe\x4b\xd9\xce\x75\x2c\x34\x25", "\x32\x86\xcc\x3d\xf1\x30\x43\x4c\xbe\xbe\x26\xf5\xa3\x5b\x70\x6f"]
