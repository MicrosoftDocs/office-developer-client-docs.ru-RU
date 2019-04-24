---
title: Коннектмодинум (Справочник по базам данных Access на компьютере)
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

Указывает доступные разрешения для изменения данных в [подключении](connection-object-ado.md), открытия [записи](record-object-ado.md)или указания значений для свойства [mode](mode-property-ado.md) объектов **Record** и [Stream](stream-object-ado.md) .

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
<td><p><strong>Адмодереад</strong></p></td>
<td><p>1,1</p></td>
<td><p>Указывает разрешения только на чтение.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адмодереадврите</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает разрешения на чтение и запись.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адмодерекурсиве</strong></p></td>
<td><p>0x400000</p></td>
<td><p>Используется совместно с другими значениями <em>*шаредени*</em> (<strong>адмодешаредениноне</strong>, <strong>адмодешаредениврите</strong>или <strong>адмодешаредениреад</strong>) для распространения ограничений общего доступа ко всем вложенным записям текущей <strong>записи</strong>. Он не оказывает влияния, если у <strong>записи</strong> нет дочерних элементов.</p><p>Ошибка во время выполнения создается, если она используется только с <strong>адмодешаредениноне</strong> . Однако его можно использовать с <strong>адмодешаредениноне</strong> в сочетании с другими значениями. Например, можно использовать &quot; <strong>адмодереад</strong> или <strong>адмодешаредениноне</strong> или <strong>адмодерекурсиве</strong>&quot;.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адмодешаредениноне</strong></p></td>
<td><p>столбцов</p></td>
<td><p>Позволяет другим пользователям открывать подключение с любыми разрешениями. Ни доступ для чтения, ни доступ для записи не могут быть запрещены для других пользователей.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адмодешаредениреад</strong></p></td>
<td><p>SP4</p></td>
<td><p>Запрещает другим пользователям открывать подключение с разрешениями на чтение.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адмодешаредениврите</strong></p></td>
<td><p>8,5</p></td>
<td><p>Запрещает другим пользователям открывать подключение с разрешениями на запись.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адмодешариксклусиве</strong></p></td>
<td><p>12</p></td>
<td><p>Запрещает другим пользователям открывать подключение.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адмодеункновн</strong></p></td>
<td><p>нуль</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что разрешения еще не установлены или не могут быть определены.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адмодеврите</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает разрешения только на запись.</p></td>
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
<td><p>Адоенумс. Коннектмоде. READ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Коннектмоде. READWRITE</p></td>
</tr>
<tr class="odd">
<td><p>(Нет эквивалента Адоенумс. Коннектмоде. recursive)</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Коннектмоде. ШАРЕДЕНИНОНЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Коннектмоде. ШАРЕДЕНИРЕАД</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Коннектмоде. ШАРЕДЕНИВРИТЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Коннектмоде. ШАРИКСКЛУСИВЕ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Коннектмоде. UNKNOWN</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Коннектмоде. WRITE</p></td>
</tr>
</tbody>
</table>

