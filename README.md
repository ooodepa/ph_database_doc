## Database

| Table                         | Key | Column                      | JavaScript type | MySQL type    | NULL | DEFAULT        |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_SitemapChangefreq      | PK  | ph_code                     | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_CTL_SitemapChangefreq      |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_CTL_SitemapChangefreq      |     | ph_value                    | string          | VARCHAR(16)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_Languages              | PK  | ph_code                     | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_CTL_Languages              |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_CTL_Languages              |     | ph_htmlLangValue            | string          | VARCHAR(4)    |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_ItemCharacteristics    | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_CTL_ItemCharacteristics    |     | ph_description              | string          | VARCHAR(32)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_ItemCharactTranslates  | PK  | ph_id                       | string          | VARCHAR(73)   |      | FK + "_" + FK  |
| PH_LST_ItemCharactTranslates  | FK  | ph_itemCharacteristicCode   | string          | VARCHAR(36)   |      |                |
| PH_LST_ItemCharactTranslates  | FK  | ph_languageCode             | number          | INT UNSIGNED  |      |                |
| PH_LST_ItemCharactTranslates  |     | ph_translateName            | string          | VARCHAR(64)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_SEOPages               | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_CTL_SEOPages               |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_CTL_SEOPages               |     | ph_htmlTitle                | string          | VARCHAR(256)  |      |                |
| PH_CTL_SEOPages               |     | ph_htmlDescription          | string          | VARCHAR(512)  |      |                |
| PH_CTL_SEOPages               |     | ph_htmlKeywords             | string          | VARCHAR(1024) |      |                |
| PH_CTL_SEOPages               |     | ph_htmlLang                 | string          | VARCHAR(16)   |      |                |
| PH_CTL_SEOPages               |     | ph_languageCode             | number          | INT UNSIGNED  |      |                |
| PH_CTL_SEOPages               |     | ph_sitemapChangefreqCode    | number          | INT UNSIGNED  |      |                |
| PH_CTL_SEOPages               |     | ph_sitemapPriority          | number          | FLOAT         |      |                |
| PH_CTL_SEOPages               |     | ph_sitemapLoc               | string          | VARCHAR(2000) |      |                |
| PH_CTL_SEOPages               |     | ph_sitemapLastmod           | string          | DATETIME      |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_SEOPagesGalery         | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_SEOPagesGalery         | FK  | ph_seoPageCode              | string          | VARCHAR(36)   |      |                |
| PH_LST_SEOPagesGalery         |     | ph_photoUrl                 | string          | VARCHAR(2000) |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_Brands                 | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_CTL_Brands                 |     | ph_description              | string          | VARCHAR(32)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_BrandGalery            | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_BrandGalery            | FK  | ph_brandCode                | string          | VARCHAR(36)   |      |                |
| PH_LST_BrandGalery            |     | ph_photoUrl                 | string          | VARCHAR(2000) |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_BrandSEOPages          | PK  | ph_id                       | string          | VARCHAR(73)   |      | UUID()         |
| PH_LST_BrandSEOPages          | FK  | ph_brandCode                | string          | VARCHAR(36)   |      |                |
| PH_LST_BrandSEOPages          | FK  | ph_SEOPageCode              | string          | VARCHAR(36)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_ItemCategories         | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_CTL_ItemCategories         |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_CTL_ItemCategories         | FK  | ph_parentItemCategoryCode   | number          | INT UNSIGNED  | NULL |                |
| PH_CTL_ItemCategories         | FK  | ph_brandCode                | string          | VARCHAR(36)   | NULL |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_ItemCategoryGalery     | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_ItemCategoryGalery     | FK  | ph_itemCategoryCode         | string          | VARCHAR(36)   |      |                |
| PH_LST_ItemCategoryGalery     |     | ph_photoUrl                 | string          | VARCHAR(2000) |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_ItemCategorySEOPages   | PK  | ph_id                       | string          | VARCHAR(73)   |      | FK + "_" + FK  |
| PH_LST_ItemCategorySEOPages   | FK  | ph_itemCategoryCode         | string          | VARCHAR(36)   |      |                |
| PH_LST_ItemCategorySEOPages   | FK  | ph_SEOPageCode              | string          | VARCHAR(36)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_PortalCategories       | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_CTL_PortalCategories       |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_CTL_PortalCategories       | FK  | ph_parentPortalCategoryCode | number          | INT UNSIGNED  | NULL |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_PortalCategoryGalery   | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_PortalCategoryGalery   | FK  | ph_itemCategoryCode         | string          | VARCHAR(36)   |      |                |
| PH_LST_PortalCategoryGalery   |     | ph_photoUrl                 | string          | VARCHAR(2000) |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_PortalCategorySEOPages | PK  | ph_id                       | string          | VARCHAR(73)   |      | FK + "_" + FK  |
| PH_LST_PortalCategorySEOPages | FK  | ph_itemCategoryCode         | string          | VARCHAR(36)   |      |                |
| PH_LST_PortalCategorySEOPages | FK  | ph_SEOPageCode              | string          | VARCHAR(36)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_Items                  | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_CTL_Items                  |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_CTL_Items                  |     | ph_description              | string          | VARCHAR(32)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_ItemGalery             | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_ItemGalery             | FK  | ph_itemCode                 | string          | VARCHAR(36)   |      |                |
| PH_LST_ItemGalery             |     | ph_photoUrl                 | string          | VARCHAR(2000) |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_ItemSEOPages           | PK  | ph_id                       | string          | VARCHAR(73)   |      | FK + "_" + FK  |
| PH_LST_ItemSEOPages           | FK  | ph_itemCode                 | string          | VARCHAR(36)   |      |                |
| PH_LST_ItemSEOPages           | FK  | ph_SEOPageCode              | string          | VARCHAR(36)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_ItemCharacteristics    | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_ItemCharacteristics    | FK  | ph_itemCode                 | string          | VARCHAR(36)   |      |                |
| PH_LST_ItemCharacteristics    | FK  | ph_itemCharacteristicCode   | string          | VARCHAR(36)   |      |                |
| PH_LST_ItemCharacteristics    |     | ph_value                    | string          | VARCHAR(256)  |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_CTL_Currency               | PK  | ph_code                     | number          | INT UNSIGNED  |      | AUTO_INCREMEN  |
| PH_CTL_Currency               |     | ph_description              | string          | VARCHAR(3)    |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_DOC_CurrencyConverter      | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_DOC_CurrencyConverter      |     | ph_description              | string          | VARCHAR(64)   |      |                |
| PH_DOC_CurrencyConverter      |     | ph_date                     | string          | DATETIME      |      |                |
| PH_DOC_CurrencyConverter      |     | ph_currancy1                | number          | INT UNSIGNED  |      |                |
| PH_DOC_CurrencyConverter      |     | ph_currancy2                | number          | INT UNSIGNED  |      |                |
| PH_DOC_CurrencyConverter      |     | ph_mulX (* x)               | number          | FLOAT         |      | 1              |
| PH_DOC_CurrencyConverter      |     | ph_divX (/ x)               | number          | FLOAT         |      | 1              |
| PH_DOC_CurrencyConverter      |     | ph_plusX (+ x)              | number          | FLOAT         |      | 0              |
| PH_DOC_CurrencyConverter      |     | ph_minusX (- x)             | number          | FLOAT         |      | 0              |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_DOC_Prices                 | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_DOC_Prices                 |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_DOC_Prices                 |     | ph_number                   | string          | VARCHAR(32)   |      |                |
| PH_DOC_Prices                 |     | ph_date                     | string          | DATETIME      |      |                |
| PH_DOC_Prices                 |     | ph_brandCode                | string          | VARCHAR(36)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_PriceItems             | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_PriceItems             | FK  | ph_itemCode                 | string          | VARCHAR(36)   |      |                |
| PH_LST_PriceItems             |     | ph_priceCode                | string          | VARCHAR(36)   |      |                |
| PH_LST_PriceItems             |     | ph_cost                     | number          | FLOAT         |      |                |
| PH_LST_PriceItems             |     | ph_currencyCode             | number          | INT UNSIGNED  |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_PriceGalery            | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_PriceGalery            | FK  | ph_priceCode                | string          | VARCHAR(36)   |      |                |
| PH_LST_PriceGalery            |     | ph_photoUrl                 | string          | VARCHAR(2000) |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_DOC_Certificates           | PK  | ph_code                     | string          | VARCHAR(36)   |      | UUID()         |
| PH_DOC_Certificates           |     | ph_description              | string          | VARCHAR(32)   |      |                |
| PH_DOC_Certificates           |     | ph_number                   | string          | VARCHAR(32)   |      |                |
| PH_DOC_Certificates           |     | ph_date                     | string          | DATETIME      |      |                |
| PH_DOC_Certificates           |     | ph_brandCode                | string          | VARCHAR(36)   |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_CertificateItems       | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_CertificateItems       | FK  | ph_itemCode                 | string          | VARCHAR(36)   |      |                |
| PH_LST_CertificateItems       |     | ph_certificateCode          | string          | VARCHAR(36)   |      |                |
| PH_LST_CertificateItems       |     | ph_index                    | number          | INT UNSIGNED  |      |                |
| ----------------------------- | --- | --------------------------- | --------------- | ------------- | ---- | -------------- |
| PH_LST_CertificateGalery      | PK  | ph_id                       | number          | INT UNSIGNED  |      | AUTO_INCREMENT |
| PH_LST_CertificateGalery      | FK  | ph_certificateCode          | string          | VARCHAR(36)   |      |                |
| PH_LST_CertificateGalery      |     | ph_photoUrl                 | string          | VARCHAR(2000) |      |                | 


## Example PH_CTL_SitemapChangefreq

| ph_code | ph_description            | ph_value |
| ------- | ------------------------- | -------- |
| 1       | Always update             | always   |
| 2       | Update after 1 h          | hourly   |
| 3       | Update after 24 h         | daily    |
| 4       | Update after 168 h (7d)   | weekly   |
| 5       | Update after ~5208 h (1m) | monthly  |
| 6       | Update after 1 year       | yearly   |
| 7       | Never update              | never    |

## Example PH_CTL_Languages

| ph_code | ph_description  | ph_htmlLangValue |
| ------- | --------------- | ---------------- |
| 1       | English         | en               |
| 2       | Türkçe          | tr               |
| 3       | Беларуская мова | by               |
| 4       | Русский язык    | ru               |

## Example PH_CTL_ItemCharacteristics

| ph_code | ph_description            |
| ------- | ------------------------- |
| 1       | Wholesale - on box        |
| 2       | Wholesale - net KG        |
| 3       | Wholesale - gross KG      |
| 4       | Wholesale - package X     |
| 4       | Wholesale - package Y     |
| 4       | Wholesale - package Z     |
| 4       | Wholesale - package M3    |
| 5       | Update after ~5208 h (1m) |
| 6       | Update after 1 year       |
| 7       | Never update              |


## Example PH_LST_ItemCharactTranslates

| ph_id | ph_itemCharactsCode | ph_languageCode | ph_translateName  |
| ----- | ------------------- | --------------- | ----------------- |
| 1     | 1                   | 1               | In wholesale box  |
| 2     | 1                   | 2               | Toptan kutuda     |
| 3     | 1                   | 3               | У аптовай скрынцы |
| 4     | 1                   | 4               | В оптовой коробке |
| 5     | 2                   | 1               | Net weight        |
| 6     | 2                   | 2               | Net ağırlığı      |
| 7     | 2                   | 3               | Маса нета         |
| 8     | 2                   | 4               | Масса нетто       |
| 9     | 3                   | 1               | Gross weight      |
| 10    | 3                   | 2               | Brüt ağırlık      |
| 11    | 3                   | 3               | Маса брута        |
| 12    | 3                   | 4               | Масса брутто      |
| 13    | 3                   | 1               | Length            |
| 14    | 3                   | 2               | Uzunluk           |
| 15    | 3                   | 3               | Даўжыня           |
| 16    | 3                   | 4               | Длина             |

## Example PH_CTL_Currency

| ph_code | ph_description |
| ------- | ------------   |
| 1       | USD            |
| 2       | EUR            |
| 3       | BYN            |
| 4       | RUB            |
| 4       | GEL            |
| 4       | AMD            |
