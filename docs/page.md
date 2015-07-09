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
  "options": {

  }
  "dependencies": {
    "css": [],
    "js": []
  },
  "adminDependencies": {
    "css": [],
    "js": []
  },
  "sections":{
    "<main>": {
      "modules": [{
        "key": null
        "options": {}
        }]
    }
  }
}
```
