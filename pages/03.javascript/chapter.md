---
title: JS Components
taxonomy:
    category: docs
---

## JS Components
Magento uses RequireJS to load and manage component based JS. Each piece of distinct functionality should be a separate component dressed as AMD module. Keeping all custom JS in one big file somewhere in web/js folder and initialized on DOM ready should be avoided. Components should be easily extendable and preferably configurable. 

Magento recognizes different types of components to achieve the expected behaviours:
* jQuery widgets 
* jQuery UI widgets (Magento UI library)
* JS objects 
* UI components (Magento_Ui/js/core/app type components) 
