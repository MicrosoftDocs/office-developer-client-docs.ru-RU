---
title: CursorLocationEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7f8eedd1245be16d87a2d3b2cd2b9121853529c5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863638"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Применимо к**: Access 2013 | Office 2013

Указывает расположение службы курсора.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adUseClient</strong></p></td>
<td><p>3</p></td>
<td><p>Используется в телефонном локальный курсор библиотеки записей на стороне клиента. Локальный курсор служб часто позволит множество функций, которые не разрешается-драйвер курсоры, с помощью этого параметра может предоставить преимущество по отношению к функции, которые будут включены. Для обеспечения обратной совместимости также поддерживается синоним <strong>adUseClientBatch</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>Не используйте службы курсора. (Этой константы является устаревшим и отображается только для обратной совместимости).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Значение, используемое по умолчанию. Использует поставщик данных или курсоры драйвер. Эти курсоры иногда гибкой и позволяют для дополнительных знаков для изменения других пользователей к источнику данных. Тем не менее некоторые функции <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Службы Microsoft курсора для OLE DB</a> (например, этом отдельные объекты <a href="recordset-object-ado.md">набора записей</a> ) нельзя моделируемые с записей на стороне сервера, и эти функции будут недоступны при использовании этого параметра.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorLocation.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.SERVER</p></td>
</tr>
</tbody>
</table>

