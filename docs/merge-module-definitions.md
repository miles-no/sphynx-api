Code example for merging module definition into page

``` js
'use strict';

var merge = require('merge'),
    api = require('../api');

function mergeModuleDefinitions(config, moduleDefinitions) {
  var instanceMap = {};
  Object.keys(config.sections).forEach(function (section) {
    config.sections[section].modules = config.sections[section].modules
      .filter(function (module) {
        // Remove modules with missing definition
        return moduleDefinitions.filter(function (definition) {
          return module.key === definition.key;
        }).length;
      })
      .map(function (module) {
        var moduleDefinition = moduleDefinitions.filter(function (definition) {
          return module.key === definition.key;
        })[0];

        if(!instanceMap[module.key]){
          instanceMap[module.key] = 1;
        } else {
          instanceMap[module.key] += 1;
        }

        var options = merge({}, moduleDefinition.defaultOptions, module.options);
        var instanceId = 'module-' + module.key + '-' + instanceMap[module.key];
        return merge({__id: instanceId, sectionName: section}, moduleDefinition, {options: options});
      });
    });

  return config;
}


module.exports = function (pageConfig) {
  pageConfig = merge(true, pageConfig);
  return api.getModuleDefinitions()
    .then(function (moduleDefinitions) {
      return mergeModuleDefinitions(pageConfig, moduleDefinitions);
    });
};
```
