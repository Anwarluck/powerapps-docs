---
title: "JavaScript web resources (model-driven apps) | Microsoft Docs" # Intent and product brand in a unique string of 43-59 chars including spaces
description: "Learn about using JavaScript web resources to create a library of JavaScript functions that can be accessed from anywhere." # 115-145 characters including spaces. This abstract displays in the search result.
author: sriharibs-msft
ms.author: srihas
ms.date: 04/01/2022
ms.reviewer: jdaly
ms.topic: article
ms.subservice: mda-developer
search.audienceType: 
  - developer
search.app: 
  - PowerApps
  - D365CE
contributors: 
  - JimDaly
  - caburk
---
# JavaScript web resources

Use JavaScript web resources to create a library of JavaScript functions that can be accessed from anywhere.  
  
<a name="BKMK_capabilities"></a>

## Capabilities of JavaScript web resources

With JavaScript web resources, you can more efficiently manage code used in form scripts, webpage (HTML) web resources, or ribbon commands by linking them to shared library of JavaScript functions.  
  
<a name="BKMK_limitations"></a>

## Limitations of JavaScript web resources

 Like all web resources, JavaScript web resources use the model-driven apps security context. Only licensed users who have the necessary privileges can access them.  
  
> [!NOTE]
>  References included in code between web resources aren’t tracked as solution dependencies.  
  
<a name="BKMK_Using"></a>

## Using JavaScript libraries

For information about developing and testing JavaScript libraries as well as how to associate them with ribbon commands and form events, see [Client scripting using JavaScript](client-scripting.md).  
  
<a name="BKMK_Referencing"></a>

## Referencing a script web resource from a webpage web resource

All web resources can use relative URLs to reference each other. In the following example, for the webpage web resource `new_/content/contentpage.htm` to reference the JavaScript web resource `new_/scripts/myScript.js`, add the following HTML code to the head element of `new_/content/contentpage.htm`.  
  
```html  
<script type="text/jscript" src="../scripts/myScript.js"></script>  
```  
  
 To reference a JavaScript from a different publisher, the path must include the customization prefix for that publisher. For example, for the `new_/content/contentpage.htm` page to reference the `MyIsv_/scripts/customscripts.js` page, the `src` attribute value should be `../../MyIsv_/scripts/customscripts.js`.  
  
### See also

[Client scripting using JavaScript](client-scripting.md)<br />
[Web resources](web-resources.md)<br />
[Using Web Page (HTML) web resources](webpage-html-web-resources.md)<br />
[Using Style Sheet (CSS) web resources](css-web-resources.md)<br />
[Using Data (XML) web resources](data-xml-web-resources.md)<br />
[Using Image (JPG, PNG, GIF) web resources](image-web-resources.md)<br />
[Using Stylesheet (XSL) web resources](stylesheet-xsl-web-resources.md)<br />
[Streamline web resource development using Fiddler AutoResponder](streamline-javascript-development-fiddler-autoresponder.md)<br />


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
