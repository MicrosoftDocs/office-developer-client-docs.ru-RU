---
title: LockTypeEnum (Справочник по базам данных Access на компьютере)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289866"
---
# <a name="locktypeenum"></a>LockTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает тип блокировки, помещаемой в записи во время редактирования.

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
<td><p><strong>Адлоккбатчоптимистик</strong></p></td>
<td><p>SP4</p></td>
<td><p>Указывает на неоптимистичные пакетные обновления. Обязательный режим для режима пакетного обновления.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адлоккоптимистик</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает на оптимистичную блокировку, запись по записи. Поставщик использует оптимистическую блокировку, блокируя записи только при вызове метода <a href="update-method-ado.md">Update</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адлоккпессимистик</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает на пессимистическую блокировку, запись по записи. Поставщик выполняет то, что необходимо для успешного редактирования записей, как правило, путем блокировки записей в источнике данных сразу же после редактирования.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адлоккреадонли</strong></p></td>
<td><p>1,1</p></td>
<td><p>Указывает записи, предназначенные только для чтения. Вы не можете изменить данные.</p></td>
</tr>
<tr class="odd">
<td><p><strong>АдлоккунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Не указывает тип блокировки. Для клонов создается клон с тем же типом блокировки, что и исходный.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

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
<td><p>Адоенумс. LockType. БАТЧОПТИМИСТИК</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. LockType. ОПТИМИСТИЧеская блокировка</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. LockType. ПЕССИМИСТическая блокировка</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. LockType. READONLY</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. LockType. unspecifieded</p></td>
</tr>
</tbody>
</table>

