# ![LOGO](logo.png) Buy Marketing **flow**ground Connector

## Description

A generated **flow**ground connector for the Buy Marketing API (version v1_beta.1.0).

Generated from: https://api.apis.guru/v2/specs/ebay.com/buy-marketing/v1_beta.1.0/swagger.json<br/>
Generated at: 2019-05-07T17:40:19+03:00

## API Description

The Marketing API retrieves eBay products based on a metric, such as Best Selling, as well as products that were also bought and also viewed.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### This call returns an array of products based on the category and metric specified. This includes details of the product, such as the eBay product Id (EPID), title, and user reviews and ratings for the product. You can use the epid returned by this call in the Browse API search call to retrieve items for this product. Restrictions For a list of supported sites and other restrictions, see API Restrictions.

*Tags:* `merchandised_product`

#### Input Parameters
* `aspect_filter` - _optional_ - The aspect name/value pairs used to further refine product results. For example: &nbsp;&nbsp;&nbsp;/buy/marketing/v1_beta/merchandised_product?category_id=31388&amp;metric_name=BEST_SELLING&amp;aspect_filter=Brand:Canon You can use the Browse API search call with the fieldgroups=ASPECT_REFINEMENTS field to return the aspects of a product. For implementation help, refer to eBay API documentation at https://developer.ebay.com/devzone/rest/api-ref/marketing/types/MarketingAspectFilter.html
* `category_id` - _required_ - This query parameter limits the products returned to a specific eBay category. The list of eBay category Ids is not published and category Ids are not all the same across all the eBay maketplace. You can use the following techniques to find a category by site. Use the Category Changes page. Use the Taxonomy API. For details see Categories for Buy API Calls. Use the Browse API and submit the following call to get the dominantCategoryId for an item. /buy/browse/v1/item_summary/search?q=keyword&amp;fieldgroups=ASPECT_REFINEMENTS Maximum: 1 Required: 1
* `limit` - _optional_ - This value specifies the maximum number of products to return in a result set. Note: Maximum value means the call will return up to that many products per set, but it can be less than this value. If the number of products found is less than this value, the call will return all of the products matching the criteria. Default: 8 Maximum: 100
* `metric_name` - _required_ - This value filters the result set by the specified metric. Only products in this metric are returned. Currently, the only metric supported is BEST_SELLING. Default: BEST_SELLING Maximum: 1 Required: 1

### This call returns products that were also bought when shoppers bought the product specified in the request. Showing 'also bought' products inspires up-selling and cross-selling. You specify the product by one of the following. epid (eBay Product Id) gtin (Global Trade Item Number) brand (brand name such as Nike) plus mpn (Manufacturer's Part Number) Restrictions For a list of supported sites and other restrictions, see API Restrictions. Maximum: A maximum of 12 products are returned. The call will return up to 12 products, but it can be less than 12. If the number of products found is less than 12, the call will return all of the products matching the criteria.

*Tags:* `merchandised_product`

#### Input Parameters
* `brand` - _optional_ - The brand of the product. Restriction: This must be used along with mpn. Required: You must specify one epid, or one gtin, or one brand plus mpn pair.
* `epid` - _optional_ - The eBay product identifier of a product. Required: You must specify one epid, or one gtin, or one brand plus mpn pair.
* `gtin` - _optional_ - The unique Global Trade Item Number of the item as defined by http://www.gtin.info. This can be a UPC (Universal Product Code), EAN (European Article Number), or an ISBN (International Standard Book Number value. Required: You must specify one epid, or one gtin, or one brand plus mpn pair.
* `mpn` - _optional_ - The manufacturer part number of the product. Restriction: This must be used along with brand. Required: You must specify one epid, or one gtin, or one brand plus mpn pair.

### This call returns products that were also viewed when shoppers viewed the product specified in the request. Showing 'also viewed' products encourages up-selling and cross-selling. You specify the product by one of the following. epid (eBay Product Id) gtin (Global Trade Item Number) brand (brand name such as Nike) plus mpn (Manufacturer's Part Number) Restrictions For a list of supported sites and other restrictions, see API Restrictions. Maximum: A maximum of 12 products are returned. The call will return up to 12 products, but it can be less than 12. If the number of products found is less than 12, the call will return all of the products matching the criteria.

*Tags:* `merchandised_product`

#### Input Parameters
* `brand` - _optional_ - The brand of the product. Restriction: This must be used along with mpn. Required: You must specify one epid, or one gtin, or one brand plus mpn pair.
* `epid` - _optional_ - The eBay product identifier of a product. Required: You must specify one epid, or one gtin, or one brand plus mpn pair.
* `gtin` - _optional_ - The unique Global Trade Item Number of the item as defined by http://www.gtin.info. This can be a UPC (Universal Product Code), EAN (European Article Number), or an ISBN (International Standard Book Number value. Required: You must specify one epid, or one gtin, or one brand plus mpn pair.
* `mpn` - _optional_ - The manufacturer part number of the product. Restriction: This must be used along with brand.

## License

**flow**ground :- Telekom iPaaS / ebay-com-buy-marketing-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
