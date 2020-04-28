---
title: Коммандтипинум (Справочник по базам данных Access на компьютере)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296117"
---
# <a name="commandtypeenum"></a>CommandTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает, как должен интерпретироваться аргумент команды.

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
<td><p><strong>адкмдунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Не указывает аргумент типа команды.</p></td>
</tr>
<tr class="even">
<td><p><strong>адкмдтекст</strong></p></td>
<td><p>1,1</p></td>
<td><p>Вычисляет значение <a href="commandtext-property-ado.md">CommandText</a> в качестве текстового определения команды или вызова хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адкмдтабле</strong></p></td>
<td><p>2</p></td>
<td><p>Оценивает свойство <strong>CommandText</strong> как имя таблицы, столбцы которой возвращаются внутренним запросом SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong>адкмдсторедпрок</strong></p></td>
<td><p>4 </p></td>
<td><p>Вычисляет значение <strong>CommandText</strong> в качестве имени хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адкмдункновн</strong></p></td>
<td><p>8 </p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что тип команды в свойстве <strong>CommandText</strong> неизвестен.</p></td>
</tr>
<tr class="even">
<td><p><strong>адкмдфиле</strong></p></td>
<td><p>256</p></td>
<td><p>Вычисляет значение <strong>CommandText</strong> в качестве имени файла сохраняемого сохраняемого <a href="recordset-object-ado.md">набора записей</a>. Используется с <strong>Recordset.</strong> Только для <a href="open-method-ado-recordset.md">открытия или повторного</a> <a href="requery-method-ado.md">запроса</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>адкмдтабледирект</strong></p></td>
<td><p>512</p></td>
<td><p>Оценивает свойство <strong>CommandText</strong> как имя таблицы, в которой возвращаются все столбцы. Используется с параметром <strong>Recordset. Open</strong> или <strong>Requery</strong> only. Чтобы использовать метод <a href="seek-method-ado.md">Seek</a> , необходимо открыть объект <strong>Recordset</strong> с помощью <strong>адкмдтабледирект</strong>. Это значение не может сочетаться со <a href="executeoptionenum.md">ExecuteOptionEnum</a> значением ексекутеоптионенум <strong>адасинцексекуте</strong>.</p></td>
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
<td><p>Адоенумс. CommandType. unspecifiedо</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. CommandType. TEXT</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. CommandType. TABLE</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. CommandType. СТОРЕДПРОК</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. CommandType. UNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. CommandType. FILE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. CommandType. TABLEDIRECT</p></td>
</tr>
</tbody>
</table>

