---
title: ConnectOptionEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295683"
---
# <a name="connectoptionenum"></a>ConnectOptionEnum

**Область применения**: Access 2013, Office 2013

Указывает, должен ли метод [Open](open-method-ado-connection.md) объекта [Connection](connection-object-ado.md) возвращаться после (синхронно) или до (асинхронно) подключения.

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
<td><p><strong>adAsyncConnect</strong></p></td>
<td><p>16 </p></td>
<td><p>Открывает подключение асинхронно. Событие <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> может использоваться для определения того, когда подключение доступно.</p></td>
</tr>
<tr class="even">
<td><p><strong>adConnectUnspecified</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Синхронно открывает подключение.</p></td>
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
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ConnectOption.ASYNCCONNECT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectOption.CONNECTUNSPECIFIED</p></td>
</tr>
</tbody>
</table>

