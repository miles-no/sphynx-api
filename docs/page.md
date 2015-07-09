Example of a page object. Note that properties may vary

```js
{
  /**
   * Title of the page
   * @type String
   */
  "title": null,
  /**
   * Relative path of the page
   * @type String
   */
  "path": null,
  /**
   * Name of layout for the page
   *
   * @type String
   */
  "layoutName": null
  /**
   * HTML layout
   *
   * @type String
   */
  "layout": null
  /**
   * Date when the page was last edited
   * @type Date
   */
  "lastEdited": null,
  /**
   * Flag that determines whether or not the page has been published
   * @type Boolean
   */
  "published": null,
  /**
   * Content that will be injected in the head section of the page
   * Can be anything really, so be careful
   * @type String
   */
  "headFragment": null,
  /**
   * Content that will be injected at the end of the body section of the page
   * Can be anything really, so be careful
   * @type String
   */
  "footFragment": null,
  /**
   * Object containing various options for the page. Can be anything really
   * @type Object
   */
  "options": null
  /**
   * Dependencies to load for this page
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
   * Dependencies to load for this page when in admin or inline edit mode
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
   * Object describing the different sections in the page and which modules to load into each section
   * @type Object
   */
  "sections":{
    /**
     * Name of the section. Can be anything really
     * @type String
     */
    "<main>": {
      /**
       * Array of modules in the section
       * @type Array of bjects
       */
      "modules": [{
        /**
         * The key of the module definition
         * @type string
         */
        "key": null
        /**
         * Options specific to this instance of the module
         * @type Object
         */
        "options": null
      }]
    }
  }
}
```
