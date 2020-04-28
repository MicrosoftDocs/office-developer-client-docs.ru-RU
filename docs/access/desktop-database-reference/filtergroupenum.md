---
title: Филтерграупенум (Справочник по базам данных Access на компьютере)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2ce54fe743c46468850abc5dc16520e208ec9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292421"
---
# <a name="filtergroupenum"></a>FilterGroupEnum

**Область применения**: Access 2013, Office 2013

Задает группу записей для фильтрации из [набора записей](recordset-object-ado.md).

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
<td><p><strong>адфилтераффектедрекордс</strong></p></td>
<td><p>2</p></td>
<td><p>Фильтры для просмотра записей, затронутых последним вызовом <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>или <a href="cancelbatch-method-ado.md">CancelBatch</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>адфилтерконфликтингрекордс</strong></p></td>
<td><p>5 </p></td>
<td><p>Фильтры для просмотра записей, для которых не удалось выполнить Последнее пакетное обновление.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адфилтерфетчедрекордс</strong></p></td>
<td><p>4</p></td>
<td><p>Фильтры для просмотра записей в текущем кэше (то есть результаты последнего вызова для получения записей из базы данных).</p></td>
</tr>
<tr class="even">
<td><p><strong>адфилтерноне</strong></p></td>
<td><p>нуль</p></td>
<td><p>Удаляет текущий фильтр и восстанавливает все записи для просмотра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адфилтерпендингрекордс</strong></p></td>
<td><p>1,1</p></td>
<td><p>Фильтры для просмотра только тех записей, которые были изменены, но еще не отправлены на сервер. Применяется только для режима пакетного обновления.</p></td>
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
<td><p>Адоенумс. Филтерграуп. АФФЕКТЕДРЕКОРДС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Филтерграуп. КОНФЛИКТИНГРЕКОРДС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Филтерграуп. ФЕТЧЕДРЕКОРДС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Филтерграуп. NONE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Филтерграуп. ПЕНДИНГРЕКОРДС</p></td>
</tr>
</tbody>
</table>

