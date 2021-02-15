---
title: Пространства имен (справочник по базам данных Access для настольных ПК)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288627"
---
# <a name="namespaces"></a>Пространства имен

**Область применения**: Access 2013, Office 2013

Формат сохраняемости XML в ADO использует следующие четыре пространства имен.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefix</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Ссылается на пространство имен XML-Data, содержащее элементы и атрибуты, определяющие схему &quot; &quot; текущего <strong>элемента Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>Относится к спецификации определений типов данных.</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
<td><p>Ссылается на пространство имен, содержащее элементы и атрибуты, специфические для свойств и атрибутов объекта <strong>Recordset</strong> ADO.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Относится к схеме текущего наборов строк.</p></td>
</tr>
</tbody>
</table>


Клиент не должен добавлять собственные теги в эти пространства имен, как определено в спецификации. Например, клиент не должен определять пространство имен как "urn:schemas-microsoft-com:rowset", а затем записывать такие записи, как "rs:MyOwnTag". Дополнительные информацию о пространствах имен см. в [XML-пространствах имен.](https://www.w3.org/tr/xml-names/)

> [!NOTE]
> ИД тега схемы должен быть "RowsetSchema", а пространство имен, используемого для ссылки на схему текущего наборов строк, должно ссылаться на "#RowsetSchema".

Обратите внимание, что префикс пространства имен, части справа от двоеточия и слева от знака равного, является произвольным.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

Пользователь может определить его как любое имя, если это имя постоянно используется в XML-документе. ADO всегда записывает "s", "rs", "dt" и "z", но эти имена префиксов не имеют жесткого кода в компоненте загрузки.



