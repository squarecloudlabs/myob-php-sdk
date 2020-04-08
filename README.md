# MYOB PHP SDK

[MYOB PHP SDK](https://github.com/squarecloudlabs/myob-php-sdk) is an Software Development Kit for accessing [MYOB](http://developer.myob.com/api/accountright/v2/)'s  AccountRight Live API.

## Installation

Add information about composer

    composer require  squarecloudlabs/myob-php-sdk

## Usage

### OAuth Authentication

If you've already got an OAuth access token, feel free to skip to API Client Setup.

The MYOB API uses 3 legged OAuth2. If you don't want to roll your own, or use the [OmniAuth strategy](https://github.com/davidlumley/omniauth-myob) you can authenticate using the `get_access_code_url` and `get_access_token` methods that [ghiculescu](https://github.com/ghiculescu) has provided like so:


### API Client Setup

Create an api_client:


If you have a refresh token (the Myob API returns one by default) you can use that too:

Or if you know which Company File you want to access too:


If you provide a company file, the gem will attempt to connect to MYOB to get the base API subdomain to use for future requests ([learn more](http://developer.myob.com/api/accountright/best-practice-guides/hypermedia-and-uris/)).

### API Methods

#### Company Files

Before using the majority of API methods you will need to have selected a Company File. If you've already selected one when creating the client, feel free to ignore this.

Return a list of company files:


####  Contacts

#### Customers

#### Employees

#### Invoices


## Todo

* Expand API methods
* Refactor client factory architecture
* Tests


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b feature/my-exciting-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/my-exciting-feature`)
5. Create new Pull Request
