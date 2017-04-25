# Drip API Laravel Wrapper #
## A Laravel wrapper for Drip's PHP wrapper for their REST API ##

### Installation ###

1) Add the package as a dependency in your composer.json

```
composer require wouterNL/laravel-drip
```

2) publish the vendor config file
```
php artisan vendor:publish --provider="wouterNL\Drip\DripPhpServiceProvider"
```

3) Add your Drip API token to the config file located in app/config/drip.php. I recommend you add this key to your project .env file instead of directly adding it to your config file.
```
DRIP_API_TOKEN=your token here
```

4) Add your Drip Account ID  to the config file located in app/config/drip.php. I recommend you add this key to your project .env file instead of directly adding it to your config file.
```
DRIP_ACCOUNT_ID=Your Account ID here
```

5) Add the following line to your providers array in your config/app.php file
```
wouterNL\Drip\DripServiceProvider::class,
```

6) Add the following line to your aliases array in your config/app.php file
```
'Drip' => wouterNL\Drip\Facades\DripFacade::class,
```


### The following functions are available: ###

- Drip::getCampaigns($params)
- Drip::fetchCampaign($params)
- Drip::getAccounts()
- Drip::createOrUpdateSubscriber($params)
- Drip::fetchSubscriber($params)
- Drip::subscribeSubscriber($params)
- Drip::unsubscribeSubscriber($params)
- Drip::tagSubscriber($params)
- Drip::untagSubscriber($params)
- Drip::recordEvent($params)
- Drip::makeRequest($url, $params = array(), $req_method = self::GET)
- Drip::getRequestInfo()
- Drip::getErrorMessage()
- Drip::getErrorCode()
