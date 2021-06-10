---
title: Пространства имен (ссылка на настольные базы данных)
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

Формат Сохраняемости XML в ADO использует следующие четыре пространства имен.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefix</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Ссылается на пространство имен XML-Data, содержащее элементы и атрибуты, определяющие схему &quot; &quot; текущего <strong>наборов записей.</strong></p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>Ссылается на спецификацию определений типов данных.</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
<td><p>Относится к пространству имен, содержащим элементы и атрибуты, определенные свойствам и атрибутам ADO <strong>Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Ссылается на схему текущего ряда.</p></td>
</tr>
</tbody>
</table>


Клиент не должен добавлять свои теги в эти пространства имен, как это определено спецификацией. Например, клиент не должен определять пространство имен как "urn:schemas-microsoft-com:rowset", а затем записывать что-то вроде "rs:MyOwnTag". Дополнительные новости о пространствах имен см. в [xML-пространствах имен.](https://www.w3.org/tr/xml-names/)

> [!NOTE]
> ID для тега схемы должен быть "RowsetSchema", а пространство имен, используемого для ссылки на схему текущего ряда, должно указать на "#RowsetSchema".

Обратите внимание, что префикс пространства имен, который находится справа от толстой кишки и слева от равного знака, является произвольным.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

Пользователь может определить, что это любое имя, если это имя последовательно используется во всем XML-документе. ADO всегда пишет "s", "rs", "dt" и "z", но эти имена префиксов не являются жестко закодироваться в компонент загрузки.



