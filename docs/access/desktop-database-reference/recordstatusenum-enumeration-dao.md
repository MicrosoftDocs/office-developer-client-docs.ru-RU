---
title: Перечисление RecordStatusEnum (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb7bffaf91db9e1170702d2e36393da669dbe0c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309236"
---
# <a name="recordstatusenum-enumeration-dao"></a>Перечисление RecordStatusEnum (DAO)


**Область применения**: Access 2013, Office 2013

Используется вместе со свойством **рекордстатус** , чтобы указать состояние обновления текущей записи, если она является частью пакетного обновления.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Дбрекорддбделетед</p></td>
<td><p>SP4</p></td>
<td><p>Запись удалена на локальном компьютере и в базе данных.</p></td>
</tr>
<tr class="even">
<td><p>Дбрекордделетед</p></td>
<td><p>4</p></td>
<td><p>Запись была удалена, но еще не удалена в базе данных.</p></td>
</tr>
<tr class="odd">
<td><p>Дбрекордмодифиед</p></td>
<td><p>1,1</p></td>
<td><p>Запись изменена и не обновлена в базе данных.</p></td>
</tr>
<tr class="even">
<td><p>Дбрекорднев</p></td>
<td><p>2</p></td>
<td><p>Запись была вставлена с помощью метода <strong>AddNew</strong> , но еще не вставлена в базу данных.</p></td>
</tr>
<tr class="odd">
<td><p>Дбрекордунмодифиед</p></td>
<td><p>нуль</p></td>
<td><p>Умолчани Запись не была изменена или была успешно обновлена.</p></td>
</tr>
</tbody>
</table>

