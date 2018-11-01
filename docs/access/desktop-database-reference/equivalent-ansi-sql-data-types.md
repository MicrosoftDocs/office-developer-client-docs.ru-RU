---
title: Типы данных SQL эквивалентный ANSI
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cac58601277079f6843df6ac9ac7bcae7824b18a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869528"
---
# <a name="equivalent-ansi-sql-data-types"></a>Типы данных SQL эквивалентный ANSI


**Применимо к**: Access 2013, Office 2013

В следующей таблице перечислены типы данных ANSI SQL, эквивалентные им типы данных ядра базы данных Microsoft Access SQL и допустимые синонимы. Он также приведены эквивалентные типы данных Microsoft® SQL Server™.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип данных ANSI SQL</p></th>
<th><p>Тип данных Microsoft Access SQL</p></th>
<th><p>Синоним</p></th>
<th><p>Тип данных Microsoft SQL Server</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BIT, ИЗМЕНЕНИЕ БИТА</p></td>
<td><p>ДВОИЧНЫЙ (см. примечания)</p></td>
<td><p>VARBINARY ДВОИЧНЫЕ МЕНЯЮЩЕГОСЯ ИЗМЕНЕНИЕ БИТА</p></td>
<td><p>ДВОИЧНЫЙ VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>БИТ (см. примечания)</p></td>
<td><p>ЛОГИЧЕСКОЕ ЗНАЧЕНИЕ, ЛОГИЧЕСКИХ, ЛОГИЧЕСКОЕ_ЗНАЧЕНИЕ1, YESNO</p></td>
<td><p>БИТ</p></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>TINYINT</p></td>
<td><p>INTEGER1 БАЙТ</p></td>
<td><p>TINYINT</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>СЧЕТЧИК (см. примечания)</p></td>
<td><p>АВТОУВЕЛИЧЕНИЕ</p></td>
<td><p>(См. примечания)</p></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>ДЕНЬГИ</p></td>
<td><p>CURRENCY</p></td>
<td><p>ДЕНЬГИ</p></td>
</tr>
<tr class="even">
<td><p>ДАТА, ВРЕМЯ, МЕТКИ ВРЕМЕНИ</p></td>
<td><p>DATETIME</p></td>
<td><p>Дата и время СОЗДАНИЯ (см. примечания)</p></td>
<td><p>DATETIME</p></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>GUID</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
</tr>
<tr class="even">
<td><p>DECIMAL</p></td>
<td><p>DECIMAL</p></td>
<td><p>ЧИСЛОВЫЕ, ДЕК</p></td>
<td><p>DECIMAL</p></td>
</tr>
<tr class="odd">
<td><p>РЕАЛЬНЫЕ</p></td>
<td><p>РЕАЛЬНЫЕ</p></td>
<td><p>SINGLE, FLOAT4, IEEESINGLE</p></td>
<td><p>РЕАЛЬНЫЕ</p></td>
</tr>
<tr class="even">
<td><p>ДВОЙНОЙ ТОЧНОСТИ С ПЛАВАЮЩЕЙ ЗАПЯТОЙ</p></td>
<td><p>FLOAT</p></td>
<td><p>Данные типа DOUBLE, FLOAT8, IEEEDOUBLE, номер (см. примечания)</p></td>
<td><p>FLOAT</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>SMALLINT</p></td>
<td><p>SHORT INTEGER2</p></td>
<td><p>SMALLINT</p></td>
</tr>
<tr class="even">
<td><p>ЦЕЛОЕ ЧИСЛО</p></td>
<td><p>ЦЕЛОЕ ЧИСЛО</p></td>
<td><p>LONG, INT, INTEGER4</p></td>
<td><p>ЦЕЛОЕ ЧИСЛО</p></td>
</tr>
<tr class="odd">
<td><p>ИНТЕРВАЛ</p></td>
<td><p>Не поддерживается</p></td>
<td><p></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>ИЗОБРАЖЕНИЕ</p></td>
<td><p>OLEOBJECT LONGBINARY, ОБЩЕЕ,</p></td>
<td><p>ИЗОБРАЖЕНИЕ</p></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>ТЕКСТ (см. примечания)</p></td>
<td><p>LONGTEXT, LONGCHAR, ЗАМЕТКА, примечание, NTEXT (см. примечания)</p></td>
<td><p>ТЕКСТ</p></td>
</tr>
<tr class="even">
<td><p>СИМВОЛ, РАЗЛИЧНАЯ СИМВОЛ, НАЦИОНАЛЬНЫЙ СИМВОЛ МЕНЯЮЩЕГОСЯ НАЦИОНАЛЬНЫЙ СИМВОЛОВ</p></td>
<td><p>ЗНАКОВ (см. примечания)</p></td>
<td><p>Text(n) буквы, символов, строка, VARCHAR, VARYING символ, NCHAR, НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ символ, VARYING НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ ЗНАКОВ VARYING (см. примечания)</p></td>
<td><p>СИМВОЛ, VARCHAR, NCHAR, NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - Тип данных ANSI SQL BIT не соответствует типа данных Microsoft Access SQL BIT. Он соответствует типу ДВОИЧНЫХ данных вместо этого. Для типа данных Microsoft Access SQL РАЗРЯДНАЯ эквивалентно не ANSI SQL.
> - Метка времени больше не поддерживается как синоним для даты и времени.
> - ЧИСЛОВОЙ больше не поддерживается как синоним с плавающей запятой или DOUBLE. ЧИСЛОВОЙ теперь используется как синоним для знаков после запятой.
> - Поле LONGTEXT всегда хранятся в формате Юникод представления.
> - Если тип данных, имя, которое TEXT используется без указания длины, например TEXT(25), создается поле LONGTEXT. Это позволяет написать, приведет к типов данных, схожих с Microsoft SQL Server [инструкции CREATE TABLE](create-table-statement-microsoft-access-sql.md) .
> - Поле символов всегда хранится в формате представления Unicode эквивалентен параметру типа данных НАЦИОНАЛЬНЫЙ ЗНАКОВ ANSI SQL.
> - Если имя типа данных TEXT используется с указанием длины, например TEXT(25), тип данных поля эквивалентно тип данных (знак). Это позволяет сохранить обратной совместимости для большинства приложений Microsoft Jet, обеспечивая тип данных TEXT (без указания длины) для совместимости с Microsoft SQL Server.


