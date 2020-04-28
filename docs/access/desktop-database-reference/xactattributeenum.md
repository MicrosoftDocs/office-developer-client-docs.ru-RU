---
title: Ксактаттрибутинум (Справочник по базам данных Access на компьютере)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302571"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**Область применения**: Access 2013, Office 2013

Задает атрибуты транзакции для объекта [Connection](connection-object-ado.md) .

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
<td><p><strong>адксактабортретаининг</strong></p></td>
<td><p>262144</p></td>
<td><p>Выполняет сохранение аварийных завершений; то есть при вызове <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> автоматически запускается новая транзакция. Не все поставщики поддерживают эту возможность.</p></td>
</tr>
<tr class="even">
<td><p><strong>адксакткоммитретаининг</strong></p></td>
<td><p>131072</p></td>
<td><p>Сохраняет фиксации; то есть при вызове <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> автоматически запускается новая транзакция. Не все поставщики поддерживают эту возможность.</p></td>
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
<td><p>Адоенумс. Ксактаттрибуте. АБОРТРЕТАИНИНГ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Ксактаттрибуте. КОММИТРЕТАИНИНГ</p></td>
</tr>
</tbody>
</table>

