---
title: Эквивалентные типы данных ANSI SQL
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293513"
---
# <a name="equivalent-ansi-sql-data-types"></a>Эквивалентные типы данных ANSI SQL


**Область применения**: Access 2013, Office 2013

В следующей таблице перечислены типы данных ANSI SQL, эквивалентные типы данных SQL ядра СУБД Microsoft Access и допустимые синонимы. В ней также перечислены эквивалентные типы данных Microsoft SQL Server™.

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
<td><p>BIT, BIT VARYING</p></td>
<td><p>BINARY (см. примечания)</p></td>
<td><p>VARBINARY, BINARY VARYING BIT VARYING</p></td>
<td><p>BINARY, VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>BIT (см. примечания)</p></td>
<td><p>BOOLEAN, LOGICAL, LOGICAL1, YESNO</p></td>
<td><p>BIT</p></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>TINYINT</p></td>
<td><p>INTEGER1, BYTE</p></td>
<td><p>TINYINT</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>COUNTER (см. примечания)</p></td>
<td><p>AUTOINCREMENT</p></td>
<td><p>(См. примечания)</p></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>MONEY</p></td>
<td><p>CURRENCY</p></td>
<td><p>MONEY</p></td>
</tr>
<tr class="even">
<td><p>DATE, TIME, TIMESTAMP</p></td>
<td><p>DATETIME</p></td>
<td><p>DATE, TIME (см. примечания)</p></td>
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
<td><p>NUMERIC, DEC</p></td>
<td><p>DECIMAL</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>REAL</p></td>
<td><p>SINGLE, FLOAT4, IEEESINGLE</p></td>
<td><p>REAL</p></td>
</tr>
<tr class="even">
<td><p>DOUBLE PRECISION, FLOAT</p></td>
<td><p>FLOAT</p></td>
<td><p>DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (см. примечания)</p></td>
<td><p>FLOAT</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>SMALLINT</p></td>
<td><p>SHORT, INTEGER2</p></td>
<td><p>SMALLINT</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>INTEGER</p></td>
<td><p>LONG, INT, INTEGER4</p></td>
<td><p>INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>INTERVAL</p></td>
<td><p>Не поддерживается</p></td>
<td><p></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Не поддерживается</p></td>
<td><p>IMAGE</p></td>
<td><p>LONGBINARY, GENERAL, OLEOBJECT</p></td>
<td><p>IMAGE</p></td>
</tr>
<tr class="odd">
<td><p>Не поддерживается</p></td>
<td><p>TEXT (см. примечания)</p></td>
<td><p>LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (см. примечания)</p></td>
<td><p>TEXT</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</p></td>
<td><p>CHAR (см. примечания)</p></td>
<td><p>TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (см. примечания)</p></td>
<td><p>CHAR, VARCHAR, NCHAR, NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - Тип данных BIT ANSI SQL не соответствует типу данных BIT Microsoft Access SQL. Он соответствует типу данных BINARY. Для типа данных BIT Microsoft Access SQL отсутствует эквивалент ANSI SQL.
> - TIMESTAMP больше не поддерживается в качестве синонима для DATETIME.
> - NUMERIC больше не поддерживается в качестве синонима для FLOAT или DOUBLE. NUMERIC теперь используется в качестве синонима для DECIMAL.
> - Поле LONGTEXT всегда хранится в формате представления Юникода.
> - Если тип данных TEXT используется без указания необязательной длины, например TEXT(25), создается поле LONGTEXT. Это позволяет записывать [операторы CREATE TABLE](create-table-statement-microsoft-access-sql.md), возвращающие типы данных, которые соответствуют Microsoft SQL Server.
> - Поле CHAR всегда хранится в формате представления Юникода, что соответствует типу данных NATIONAL CHAR ANSI SQL.
> - Если тип данных TEXT используется с указанием необязательной длины, например TEXT(25), тип данных поля эквивалентен типу данных CHAR. Это сохраняет обратную совместимость для большинства приложений Microsoft Jet, позволяя сопоставлять тип данных TEXT (без указания длины) с Microsoft SQL Server.


