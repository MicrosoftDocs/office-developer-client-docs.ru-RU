---
title: Исолатионлевеленум (Справочник по базам данных Access на компьютере)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0176772b366b39d368f8bae1e402d420f0136c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291158"
---
# <a name="isolationlevelenum"></a>IsolationLevelEnum

**Область применения**: Access 2013, Office 2013

Задает уровень изоляции транзакции для объекта [подключения](connection-object-ado.md) .

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
<td><p><strong>адксактунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Указывает, что поставщик использует уровень изоляции, отличный от указанного, но уровень не может быть определен.</p></td>
</tr>
<tr class="even">
<td><p><strong>адксактчаос</strong></p></td>
<td><p>16 </p></td>
<td><p>Указывает, что ожидающие изменения более изолированных транзакций не могут быть перезаписаны.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адксактбровсе</strong></p></td>
<td><p>256</p></td>
<td><p>Указывает, что из одной транзакции можно просматривать незафиксированные изменения в других транзакциях.</p></td>
</tr>
<tr class="even">
<td><p><strong>адксактреадункоммиттед</strong></p></td>
<td><p>256</p></td>
<td><p>То же, что и <strong>адксактбровсе</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адксакткурсорстабилити</strong></p></td>
<td><p>4096</p></td>
<td><p>Указывает, что из одной транзакции вы можете просматривать изменения в других транзакциях только после того, как они были зафиксированы.</p></td>
</tr>
<tr class="even">
<td><p><strong>адксактреадкоммиттед</strong></p></td>
<td><p>4096</p></td>
<td><p>То же, что и <strong>адксакткурсорстабилити</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адксактрепеатаблереад</strong></p></td>
<td><p>65536</p></td>
<td><p>Указывает, что из одной транзакции невозможно увидеть изменения, внесенные в другие транзакции, но это может привести к извлечению новых объектов <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>адксактисолатед</strong></p></td>
<td><p>1048576</p></td>
<td><p>Указывает на то, что транзакции проведены в изоляции других транзакций.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адксактсериализабле</strong></p></td>
<td><p>1048576</p></td>
<td><p>То же, что и <strong>адксактисолатед</strong>.</p></td>
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
<td><p>Адоенумс. IsolationLevel. unspecifieded</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. IsolationLevel. беспорядок</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. IsolationLevel. BROWSE</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. IsolationLevel. РЕАДУНКОММИТТЕД</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. IsolationLevel. КУРСОРСТАБИЛИТИ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. IsolationLevel. РЕАДКОММИТТЕД</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. IsolationLevel. РЕПЕАТАБЛЕРЕАД</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. IsolationLevel. изоляция</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. IsolationLevel. SERIALIZABLE</p></td>
</tr>
</tbody>
</table>

