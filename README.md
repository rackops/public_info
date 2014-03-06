public_info
===========

Ohai plugin that uses whoami.rackops.org to return public IP and geoip data for a node
This will fill a data structure named public_info with the following info using maxminds free geoip databases.

```
knife node show whoami-prod-01 -a public_info
whoami-prod-01:
  public_info:
    X_Forwarded: 128.66.0.1, 10.189.254.6
    asn:
      asn:    Example ASN
      number: AS5737
    city:
      area_code:        210
      city_name:        San Antonio
      continent_code:   NA
      country_code2:    US
      country_code3:    USA
      country_name:     United States
      dma_code:         641
      ip:               128.66.0.1
      latitude:         29.4889
      longitude:        -98.3987
      postal_code:      78218
      real_region_name: Texas
      region_name:      TX
      request:          128.66.0.1
      timezone:         America/Chicago
    country:
      continent_code: NA
      country_code:   225
      country_code2:  US
      country_code3:  USA
      country_name:   United States
      ip:             162.242.217.12
      request:        162.242.217.12
    remote_ip:   128.66.0.1
```    

This is useful for situations where the public IP address is not easily determinatable from within the server itself.
For example, rackconnected servers in Rackspace's environment.
