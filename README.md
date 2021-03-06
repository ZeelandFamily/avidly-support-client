Avidly Support plugin
======================
Creates a REST API endpoint for monitoring core, plugin and theme updates in our client sites.

## Usage

Install and enable plugin. Set an unique key in site dashboard Settings > Avidly Support

Go to endpoint url and add the unique key to test functionality, for example: https://example.test/wp-json/avidly-support/v1/core/7immrMbgU9Qw62DcF7PizX$2LA

should return something like this:

```
{
	"wordpress_version": "4.9.9",
	"php_version": "7.0.3",
	"is_multisite": false,
	"site_count": 1,
	"wp_install": "http://example.test/",
}
```

## Endpoints

### Core

**Endpoint**: `/wp-json/avidly-support/v1/core/{unique_key}`

**Returns**: 
- WordPress version
- PHP version
- Is it multisite?
- Site count
- Site URL

### Updates

**Endpoint:** `/wp-json/avidly-support/v1/updates/{unique_key}`

**Returns** 
- Available plugin updates
- Available theme updates
- Available core updates

### Plugins

**Endpoint:** `/wp-json/avidly-support/v1/plugins/{unique_key}`

**Returns** a list of all plugins installed in site

### Themes

**Endpoint:** `/wp-json/avidly-support/v1/themes/{unique_key}`

**Returns** a list of all themes installed in site
