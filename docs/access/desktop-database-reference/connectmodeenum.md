---
title: ConnectModeEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295697"
---
# <a name="connectmodeenum"></a>ConnectModeEnum

**Область применения**: Access 2013, Office 2013

Указывает доступные разрешения для изменения данных в [connection,](connection-object-ado.md)открытия записи или указания значений для свойства [Mode](mode-property-ado.md) объектов **Record** и [Stream.](stream-object-ado.md) [](record-object-ado.md)

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
<td><p>1 </p></td>
<td><p>Указывает разрешения только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeReadWrite</strong></p></td>
<td><p>3 </p></td>
<td><p>Указывает разрешения на чтение и записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeRecursive</strong></p></td>
<td><p>0x400000</p></td>
<td><p>Используется в сочетании с другими значениями <em>*ShareDeny*</em> <strong>(adModeShareDenyNone,</strong> <strong>adModeShareDenyWrite</strong>или <strong>adModeShareDenyRead)</strong>для распространения ограничений общего доступа ко всем в субфиксам текущей записи. <strong></strong> Это не влияет, если <strong>у записи</strong> нет детей.</p><p>Ошибка во время запуска создается, если она используется только <strong>с adModeShareDenyNone.</strong> Однако его можно использовать с <strong>adModeShareDenyNone</strong> в сочетании с другими значениями. Например, можно использовать &quot; <strong>adModeRead</strong> или <strong>adModeShareDenyNone</strong> или <strong>adModeRecursive.</strong> &quot;</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyNone</strong></p></td>
<td><p>16 </p></td>
<td><p>Позволяет другим пользователям открывать подключение с любыми разрешениями. Другим не может быть отказано в доступе на чтение и записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareDenyRead</strong></p></td>
<td><p>4 </p></td>
<td><p>Запретить другим людям открывать подключение с разрешениями на чтение.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyWrite</strong></p></td>
<td><p>8 </p></td>
<td><p>Запретить другим людям открывать подключение с разрешениями на записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareExclusive</strong></p></td>
<td><p>12 </p></td>
<td><p>Запретить другим людям открывать подключение.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что разрешения еще не установлены или не могут быть определены.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeWrite</strong></p></td>
<td><p>2 </p></td>
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
<th><p>Константа</p></th>
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

