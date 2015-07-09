Example of a module definition object. Note that properties may vary

```js
{
  /**
   * Unique key of the module definition
   * @type String
   */
  "key": null,
  /**
   * Human readble name of the module definition
   * @type String
   */
  "friendlyName": null,
  /**
   * Short description of the module definition
   * @type String
   */
  "description": null,
  /**
   * URL where to fetch the widget
   * @type String
   */
  "url": null,
  /**
   * URL where to fetch the widget in admin or inline-edit mode
   * @type String
   */
  "adminUrl": null,
  /**
   * URL to fetch the settings form for the module definition
   * @type String
   */
  "settingsUrl": null,
  /**
   * Dependencies to load
   * @type Object
   */
  "dependencies": {
    /**
     * List of stylesheets
     * @type Array of strings
     */
    "css": null,
    /**
     * List of JavaScript files
     * @type Array of strings
     */
    "js": null
  },
  /**
   * Dependencies to load when in admin or inline-edit mode
   * @type Object
   */
  "adminDependencies": {
    /**
     * List of stylesheets
     * @type Array of strings
     */
    "css": null,
    /**
     * List of JavaScript files
     * @type Array of strings
     */
    "js": null
  },
  /**
   * Object containing various default options for the module definition
   * @type Object
   */
  "defaultOptions": null,
  /**
   * Boolean determining whether this module renders some UI or if it's faceless (e.g. meta tags)
   * @type Boolean
   */
  "faceless": null,
  /**
   * Boolean determining whether or not this module can be edited
   * @type Boolean
   */
  "readOnly": null
}
```
