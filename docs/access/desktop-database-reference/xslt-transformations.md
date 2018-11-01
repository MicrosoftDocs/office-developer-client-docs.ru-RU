---
title: Преобразование в XSLT
TOCTitle: XSLT Transformations
ms:assetid: 6a19310d-027f-e8d6-9859-0b545ae7e2f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249418(v=office.15)
ms:contentKeyID: 48545425
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8bbb7e935dece05d4616044b399601c393d5f07c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889437"
---
# <a name="xslt-transformations"></a>Преобразование в XSLT


**Применимо к**: Access 2013, Office 2013

## <a name="xslt-transformations"></a>Преобразование в XSLT

XSLT может применяться к созданным XML для преобразования в другой формат. Общие сведения о формате XML в ADO помогает при разработке XSLT-шаблонов, которые можно преобразовать в форме удобства работы.

Например известно, что каждой строки **набора записей** сохраняется как элемент z: строки внутри элемента rs: данные. Аналогично каждого поля **набора записей** сохраняется в виде пара значение атрибута для этого элемента.

Приведенный ниже сценарий XSLT может применяться к XML, показано в предыдущем разделе, для преобразования в HTML-таблицы для отображения в браузере:

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

Преобразования XSLT преобразует поток XML, созданные с помощью метода ADO **Сохранить** в таблицу HTML, в котором отображаются все поля **набора записей** , а также заголовка таблицы. В таблице заголовки строк также назначаются и различных шрифтов и цвета.

