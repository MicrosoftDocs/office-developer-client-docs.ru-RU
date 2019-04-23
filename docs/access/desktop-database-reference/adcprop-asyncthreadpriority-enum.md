---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281903"
---
# <a name="adcpropasyncthreadpriorityenum"></a>Перечисление АДКПРОП\_асинксреадприорити\_

**Область применения**: Access 2013, Office 2013

Для объекта [RECORDSET](recordset-object-ado.md) RDS указывает приоритет выполнения асинхронного потока, который получает данные.

Используйте эти константы с динамическим свойством **Recordset** "**приоритет фонового потока**", на который ссылается индекс динамического свойства ADO и задокументированы в документации [службы курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .

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
<td><p><strong>Адприоритябовенормал</strong></p></td>
<td><p>SP4</p></td>
<td><p>Задает приоритет между обычным и максимальным приоритетом.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адприоритибеловнормал</strong></p></td>
<td><p>2</p></td>
<td><p>Задает приоритет между самым низким и нормальным.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адприоритихигхест</strong></p></td>
<td><p>17:00</p></td>
<td><p>Задает максимально возможный приоритет.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адприоритиловест</strong></p></td>
<td><p>1,1</p></td>
<td><p>Устанавливает минимально возможный приоритет.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адприоритинормал</strong></p></td>
<td><p>4</p></td>
<td><p>Устанавливает для приоритета значение Обычная.</p></td>
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
<td><p>Адоенумс. Адкпропасинксреадприорити. АБОВЕНОРМАЛ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Адкпропасинксреадприорити. БЕЛОВНОРМАЛ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Адкпропасинксреадприорити. ВЫСШИй</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Адкпропасинксреадприорити. НИЗШИй</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Адкпропасинксреадприорити. NORMAL</p></td>
</tr>
</tbody>
</table>

