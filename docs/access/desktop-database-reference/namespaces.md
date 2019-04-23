---
title: Пространства имен (Справочник по базам данных Access на компьютере)
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
<td><p>Указывает пространство имен &quot;XML-данных&quot; , содержащее элементы и атрибуты, определяющие схему текущего <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Microsof</p></td>
<td><p>Ссылается на спецификацию определений типов данных.</p></td>
</tr>
<tr class="odd">
<td><p>кабел</p></td>
<td><p>Ссылается на пространство имен, содержащее элементы и атрибуты, относящиеся к свойствам и атрибутам <strong>Recordset</strong> объекта ADO.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Ссылается на схему текущего набора строк.</p></td>
</tr>
</tbody>
</table>


Клиент не должен добавлять собственные теги к этим пространствам имен, как определено в спецификации. Например, клиент не должен определять пространство имен как "urn: schemas-microsoft-com: RowSet", а затем записывать что-то вроде "RS: Мйовнтаг". Дополнительные сведения о пространствах имен содержатся в разделе [пространства имен XML](https://www.w3.org/tr/xml-names/).

> [!NOTE]
> ИДЕНТИФИКАТОР тега схемы должен иметь значение "Ровсетсчема", а пространство имен, используемое для ссылки на схему текущего набора строк, должно указывать на "#RowsetSchema".

Обратите внимание, что префикс пространства имен, который является частью справа от двоеточия и слева от знака равенства, является произвольным.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

Пользователь может задать любое имя, если это имя постоянно используется в пределах XML-документа. ADO всегда записывает "s", "RS", "DT" и "z", но эти имена префиксов не жестко задаются в компонент загрузки.



