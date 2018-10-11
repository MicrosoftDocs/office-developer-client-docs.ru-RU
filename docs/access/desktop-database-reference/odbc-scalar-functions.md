---
title: ODBC Scalar Functions
TOCTitle: ODBC Scalar Functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d01c5f02cc784518d58365480b30178d4d24a332
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480815"
---
# <a name="odbc-scalar-functions"></a>ODBC Scalar Functions


**Применимо к**: Access 2013 | Office 2013

Microsoft® Access SQL поддерживает использование синтаксиса ODBC определенные скалярные функции. Например следующий запрос:

Выбор DAILYCLOSE, DAILYCHANGE из DAILYQUOTE ГДЕ {fn ABS(DAILYCHANGE)} \> 5

Возвращает строки, в которой было больше, чем пять абсолютного значения изменений в цену акции.

Поддерживается подмножество определенные скалярные функции ODBC. В следующей таблице перечислены функции, которые поддерживаются.

Для описания аргументов и объяснение синтаксиса escape-последовательности для включения функции в инструкции SQL обратитесь к документации ODBC.

## <a name="string-functions"></a>Строковые функции

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ASCII</p></td>
<td><p>ДЛИНА</p></td>
<td><p>RTRIM</p></td>
</tr>
<tr class="even">
<td><p>(ЗНАК)</p></td>
<td><p>НАЙДИТЕ</p></td>
<td><p>ПРОБЕЛ</p></td>
</tr>
<tr class="odd">
<td><p>ОБЪЕДИНИТЬ</p></td>
<td><p>ФУНКЦИИ LTRIM</p></td>
<td><p>ПОДСТРОКИ</p></td>
</tr>
<tr class="even">
<td><p>LCASE</p></td>
<td><p>Правильно</p></td>
<td><p>UCASE</p></td>
</tr>
<tr class="odd">
<td><p>СЛЕВА</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a>Числовые функции

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ABS</p></td>
<td><p>ЭТАЖ</p></td>
<td><p>SIN</p></td>
</tr>
<tr class="even">
<td><p>ATAN</p></td>
<td><p>ЖУРНАЛ</p></td>
<td><p>КОРЕНЬ</p></td>
</tr>
<tr class="odd">
<td><p>ПОТОЛОК</p></td>
<td><p>POWER</p></td>
<td><p>TAN</p></td>
</tr>
<tr class="even">
<td><p>COS</p></td>
<td><p>РЭНД</p></td>
<td><p>MOD</p></td>
</tr>
<tr class="odd">
<td><p>EXP</p></td>
<td><p>ЗНАК</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a>Функции обработки даты и времени

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CURDATE</p></td>
<td><p>DAYOFYEAR</p></td>
<td><p>МЕСЯЦ</p></td>
</tr>
<tr class="even">
<td><p>CURTIME</p></td>
<td><p>ГОД</p></td>
<td><p>НЕДЕЛИ</p></td>
</tr>
<tr class="odd">
<td><p>СЕЙЧАС</p></td>
<td><p>ЧАС</p></td>
<td><p>КВАРТАЛ</p></td>
</tr>
<tr class="even">
<td><p>ДЕНЬ МЕСЯЦА</p></td>
<td><p>МИНУТЫ</p></td>
<td><p>ФУНКЦИЯ MONTHNAME</p></td>
</tr>
<tr class="odd">
<td><p>DAYOFWEEK</p></td>
<td><p>СЕКУНДЫ</p></td>
<td><p>DAYNAME</p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a>Преобразования типов данных

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ПРЕОБРАЗОВАНИЕ</p></td>
<td><p>Строковые литералы можно преобразовать в следующие типы данных: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR и SQL_DATETIME.</p></td>
</tr>
</tbody>
</table>

