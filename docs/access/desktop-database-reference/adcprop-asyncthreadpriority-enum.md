---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae89c81b903930eb114cf050688598bc2802a25e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482276"
---
# <a name="adcpropasyncthreadpriorityenum"></a>ADCPROP\_ASYNCTHREADPRIORITY\_ENUM

**Применимо к**: Access 2013 | Office 2013

Объект служб удаленных рабочих СТОЛОВ [записей](recordset-object-ado.md) указывает приоритет выполнения асинхронного потока, который получает данные.

Используйте эти константы с свойство динамических «**Приоритет потока фона**» **набора записей** , которое по ссылке в индексе динамические свойства ADO и описаны в документации по [Microsoft служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .

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
<td><p><strong>adPriorityAboveNormal</strong></p></td>
<td><p>4</p></td>
<td><p>Задает между обычной и самый высокий приоритет.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPriorityBelowNormal</strong></p></td>
<td><p>2</p></td>
<td><p>Задает приоритет между низкий и обычный.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityHighest</strong></p></td>
<td><p>5</p></td>
<td><p>Задает приоритет к наибольшим возможной.</p></td>
</tr>
<tr class="even">
<td><p><strong>AdPriorityLowest</strong></p></td>
<td><p>1</p></td>
<td><p>Задает приоритет до наименьшего возможного.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityNormal</strong></p></td>
<td><p>3</p></td>
<td><p>Задает приоритет normal.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

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
<td><p>AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.LOWEST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.NORMAL</p></td>
</tr>
</tbody>
</table>

