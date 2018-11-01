---
title: Document Members (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ae19e30aa2a2f60f606f2380712815732eac932
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871369"
---
# <a name="document-members-dao"></a>Document Members (DAO)


**Применимо к**: Access 2013, Office 2013

Объект Document содержит сведения о один экземпляр объекта. Объект может быть базы данных, сохраненные в таблице, запрос или связь (Microsoft Access базами данных, ядро только).

## <a name="methods"></a>Методы

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
<td><p><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</p></td>
</tr>
</tbody>
</table>


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
<td><p><strong><a href="document-container-property-dao.md">Контейнер</a></strong></p></td>
<td><p>Возвращает имя объекта <strong><a href="container-object-dao.md">контейнера</a></strong> , которому принадлежит объект <strong>Document</strong> (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Возвращает дату и время создания объекта. Только для чтения <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Возвращает дату и время последнего изменения, внесенные в объект. Только для чтения <strong>Variant</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает имя указанного объекта. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
</tbody>
</table>

