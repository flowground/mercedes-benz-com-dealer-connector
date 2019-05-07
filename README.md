# ![LOGO](logo.png) Dealer **flow**ground Connector

## Description

A generated **flow**ground connector for the Dealer API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/mercedes-benz.com/dealer/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:42:59+03:00

## API Description

The Dealer API provides Dealer search functions.

## Authorization

This API does not require authorization.

## Actions

### This request returns the countries supported by the Dealer API

*Tags:* `References`

#### Input Parameters
* `page` - _optional_ - The index of the page to be returned. If this parameter is omitted, the first page will be returned.

* `pageSize` - _optional_ - The index of the page to be returned. If this parameter is omitted, the first page will be returned.


### x_swagger_router_controller_countries

### This request returns dealers (dealer, garage, retailer, etc.) for given parameters

*Tags:* `Dealer search`

#### Input Parameters
* `dealerIds` - _optional_ - Array of dealer ids. The dealer id is dealer's business key, also known as GS Id. e.g. GS0000857,GS0017621

* `latitude` - _optional_ - The latitude geo coordinate.
* `longitude` - _optional_ - The longitude geo coordinate.
* `radiusValue` - _optional_ - The radius value of the search area. The center of the search area is defined by geo coordinates. (latitude, longitude properties) If radiusValue and radiusUnit parameters are missing, then the default radius is 10 km.
* `radiusUnit` - _optional_ - The radius unit of the search area. The center of the search area is defined by geo coordinates. (latitude, longitude properties) If radiusValue and radiusUnit parameters are missing, then the default radius is 10 km.
    Possible values: M, KM, MILE.
* `countryIsoCode` - _optional_ - The country of the dealer address defined as ISO two letter ID (e.g. DE, CH, CN, etc.)
* `city` - _optional_ - The city of the dealer address.
* `name` - _optional_ - A name of the dealer, the name filter will be applied to all Dealer names (e.g. legalName, nameAddition). You can also search for parts of Dealer names, e.g. the search term 'Niederlassung' will also match 'Niederlassung Stuttgart'.
* `brand` - _optional_ - Filter by brand, valid values are:
  * MB: Mercedes-Benz
  * SMT: Smart
    Possible values: MB, SMT.
* `productGroup` - _optional_ - Filter by a product group
    Possible values: PASSENGER-CAR, VAN.
* `activity` - _optional_ - Filter by activity, valid actitvity values are:
  * PARTS: Spare Parts Sales
  * SALES: Sales of new vehicles
  * SERVICE: Maintaining and repair
  * USED-VEHICLES-TRADE: Sales of used vehicles
    Possible values: PARTS, SALES, SERVICE, USED-VEHICLES-TRADE.
* `fields` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned. e.g. fields=dealers(dealerId,address(street,city))
* `page` - _optional_ - The index of the page to be returned. If this parameter is omitted, the first page will be returned.

* `pageSize` - _optional_ - The index of the page to be returned. If this parameter is omitted, the first page will be returned.


### x_swagger_router_controller_dealers

### This request returns dealers for given parameters

*Tags:* `Dealer search`

#### Input Parameters
* `dealerId` - _required_ - The dealer id is dealer's business key, also known as GS Id. e.g. GS0000857
* `fields` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned. e.g. fields=dealerId,address(street,city)

### x_swagger_router_controller_dealers__dealerId_

## License

**flow**ground :- Telekom iPaaS / mercedes-benz-com-dealer-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
