---
title: PersistFormatEnum (Справочник по для настольных баз данных Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a1e980debebe6a38ed0c27eabba3abefcd8be152
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887154"
---
# <a name="persistformatenum"></a>PersistFormatEnum

**Применимо к**: Access 2013, Office 2013

Задает формат для сохранения [записей](recordset-object-ado.md).

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
<td><p><strong>adPersistADTG</strong></p></td>
<td><p>0</p></td>
<td><p>Указывает формат TableGram дополнительные данные (ADTG).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistADO</strong></p></td>
<td><p>1</p></td>
<td><p>Указывает, что будет использоваться формат ADO собственные языке (XML). Это значение совпадает с adPersistXML и будет включено для обратной совместимости.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPersistXML</strong></p></td>
<td><p>1</p></td>
<td><p>Указывает формат языке (XML).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistProviderSpecific</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что поставщик будет сохраняться <strong>набора записей</strong> с использованием собственного формата.</p></td>
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
<td><p>AdoEnums.PersistFormat.ADTG</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PersistFormat.XML</p></td>
</tr>
</tbody>
</table>

