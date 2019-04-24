---
title: XSLT Transformations
TOCTitle: XSLT Transformations
ms:assetid: 6a19310d-027f-e8d6-9859-0b545ae7e2f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249418(v=office.15)
ms:contentKeyID: 48545425
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7120ec08a6a222293fc53c5a98f62c50fd5b3621
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302473"
---
# <a name="xslt-transformations"></a>XSLT


**Область применения**: Access 2013, Office 2013

## <a name="xslt-transformations"></a>XSLT Transformations

XSLT можно применять к созданному XML-коду, чтобы преобразовать его в другой формат. Общие сведения о формате XML в ADO помогают разрабатывать шаблоны XSLT, которые могут преобразовать его в более удобное для пользователя форму.

Например, вы знаете, что каждая строка **набора записей** сохранена в элементе з:ров в элементе RS: Data. Аналогично, каждое поле **набора записей** сохраняется как запись Attribute-Value для этого элемента.

Приведенный ниже скрипт XSLT можно применить к XML-коду, приведенному в предыдущем разделе, чтобы преобразовать его в HTML-таблицу для отображения в браузере:

```xml 
 
<?xml version="1.0" encoding="ISO-8859-1"?> 
<html xmlns:xsl="https://www.w3.org/TR/WD-xsl"> 
<body STYLE="font-family:Arial, helvetica, sans-serif; font-size:12pt; background-color:white"> 
<table border="1" style="table-layout:fixed" width="600"> 
  <col width="200"></col> 
  <tr bgcolor="teal"> 
    <th><font color="white">CustomerId</font></th> 
    <th><font color="white">CompanyName</font></th> 
    <th><font color="white">ContactName</font></th> 
  </tr> 
<xsl:for-each select="xml/rs:data/z:row"> 
  <tr bgcolor="navy"> 
    <td><font color="white"><xsl:value-of select="@CustomerID"/></font></td> 
    <td><font color="white"><xsl:value-of select="@CompanyName"/></font></td> 
    <td><font color="white"><xsl:value-of select="@ContactName"/></font></td>  
  </tr> 
</xsl:for-each> 
</table> 

</body> 
</html> 
```

XSLT преобразует поток XML, созданный методом **сохранения** ADO, в HTML-таблицу, которая отображает каждое поле **набора записей** вместе с заголовком таблицы. Для заголовков и строк таблицы также назначаются различные шрифты и цвета.

