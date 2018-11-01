---
title: ConnectModeEnum (Справочник по для настольных баз данных Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6a09ea4d781e5560e335c2e75fc2da9a5508bae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874008"
---
# <a name="connectmodeenum"></a>ConnectModeEnum

**Применимо к**: Access 2013, Office 2013

Задает разрешения, доступные для изменения данных в [подключения](connection-object-ado.md), открытие [записи](record-object-ado.md)или указания значения для свойства [режима](mode-property-ado.md) объектов [потока](stream-object-ado.md) и **запись** .

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
<td><p><strong>adModeRead</strong></p></td>
<td><p>1</p></td>
<td><p>Указывает разрешения только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeReadWrite</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает разрешения на чтение и запись.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeRecursive</strong></p></td>
<td><p>0x400000</p></td>
<td><p>Используется в сочетании с другими <em>*ShareDeny*</em> значения (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>или <strong>adModeShareDenyRead</strong>) для распространения ограничения общего доступа ко всем дочерним записям текущей <strong>записи</strong>. Он не оказывает воздействия, если <strong>запись</strong> не имеет дочерние элементы.</p><p>При использовании с <strong>adModeShareDenyNone</strong> только создается ошибку времени выполнения. Тем не менее его можно использовать с <strong>adModeShareDenyNone</strong> в сочетании с другими значениями. Например, можно использовать &quot; <strong>adModeRead</strong> или <strong>adModeShareDenyNone</strong> или <strong>adModeRecursive</strong>&quot;.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyNone</strong></p></td>
<td><p>16</p></td>
<td><p>Позволяет другим пользователям открывать соединение с другими разрешениями. Доступ на запись ни чтения можно запретить другим пользователям.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareDenyRead</strong></p></td>
<td><p>4</p></td>
<td><p>Запрет другим пользователям открывать соединение с разрешениями на чтение.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyWrite</strong></p></td>
<td><p>8</p></td>
<td><p>Запрет другим пользователям открывать соединение с разрешениями на запись.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareExclusive</strong></p></td>
<td><p>12</p></td>
<td><p>Запрет другим пользователям открывать подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Показывает, что разрешения еще не были настроены или не может быть определен.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeWrite</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает разрешения только для записи.</p></td>
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
<td><p>AdoEnums.ConnectMode.READ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.READWRITE</p></td>
</tr>
<tr class="odd">
<td><p>(Нет эквивалента AdoEnums.ConnectMode.RECURSIVE)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.SHAREDENYNONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.SHAREDENYREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.SHAREDENYWRITE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.SHAREEXCLUSIVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.UNKNOWN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.WRITE</p></td>
</tr>
</tbody>
</table>

