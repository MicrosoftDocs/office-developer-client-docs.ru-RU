---
title: Parameter Members (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 749834dea5511fa0601608c66f65ab14022f4130
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481365"
---
# <a name="parameter-members-dao"></a>Parameter Members (DAO)


**Применимо к**: Access 2013 | Office 2013

Объект параметра представляет значение, заданное в запросе. Параметр связан с объектом QueryDef, созданный из параметра запроса.

## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="parameter-object-dao.md">параметра</a></strong> входного параметра, выходного параметра, оба адресата, или возвращаемое значение из процедуры (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает имя указанного объекта. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее действующие типа или данных тип объекта. Чтение и запись <strong>целое число</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-value-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение объекта. Чтение и запись <strong>типа Variant</strong>.</p></td>
</tr>
</tbody>
</table>
