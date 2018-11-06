---
title: Пространства имен (Справочник по для настольных баз данных Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5fb61c02a5679c6fd63e9d5dd2a257ab5f7d96a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996470"
---
# <a name="namespaces"></a>Пространства имен

**Применимо к**: Access 2013, Office 2013

Формат сохранения XML в ADO использует следующие четыре пространства имен.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Префикс</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Относится к &quot;XML-данные&quot; пространства имен, содержащего элементы и атрибуты, которые определяют схемы текущего <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>Относится к спецификации определения типа данных.</p></td>
</tr>
<tr class="odd">
<td><p>RS</p></td>
<td><p>Относится к области имен, содержащие элементы и атрибуты, относящиеся к свойствам ADO <strong>записей</strong> и атрибутов.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Относится к схеме текущий набор строк.</p></td>
</tr>
</tbody>
</table>


Клиент не следует добавлять собственные теги следующие пространства имен, определенный в спецификации. Например, клиент не задавайте имен как «urn: schemas-microsoft-com:rowset» и затем записать что-нибудь, например «rs: MyOwnTag.» Дополнительные сведения о пространствах имен [XML](https://www.w3.org/tr/xml-names/)см.

> [!NOTE]
> Идентификатор для тега схемы должен быть «RowsetSchema» и пространство имен, используемое для ссылки на схему текущий набор строк должен указывать «#RowsetSchema».

Обратите внимание, что префикс пространства имен, в правой части двоеточие и слева от знака равенства, произвольных.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

Пользователь может указать это будет любое имя, поскольку это имя будет использоваться постоянно в XML-документ. ADO всегда считывает «s,» «rs», «dt» и «z», но эти имена префикс не жестко в компонент загрузки.



