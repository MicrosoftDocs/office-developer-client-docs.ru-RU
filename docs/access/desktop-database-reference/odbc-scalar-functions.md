---
title: Скалярные функции ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288513"
---
# <a name="odbc-scalar-functions"></a>Скалярные функции ODBC

**Область применения**: Access 2013, Office 2013

Microsoft Access SQL поддерживает использование определенного синтаксиса ODBC для скалярных функций. 

Например, запрос `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` возвращает все строки, где абсолютное значение изменения цены на акции превышает 5.

Поддерживается подмножество определенных в ODBC скалярных функций. В следующей таблице перечислены поддерживаемые функции.

Описание аргументов и полное описание синтаксиса escape для включения функций в инструкцию SQL см в документации по ODBC.

## <a name="string-functions"></a>Строковые функции

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ФОРМАТ</p></td>
<td><p>ВРЕМЕНИ</p></td>
<td><p>RTRIM</p></td>
</tr>
<tr class="even">
<td><p>РАЗДЕЛИТЕЛ</p></td>
<td><p>РАЗДЕЛ</p></td>
<td><p>SPACE</p></td>
</tr>
<tr class="odd">
<td><p>ЗНАЧЕНИЙ</p></td>
<td><p>LTRIM</p></td>
<td><p>SUBSTRING</p></td>
</tr>
<tr class="even">
<td><p>LCASE</p></td>
<td><p>Правильно</p></td>
<td><p>укасе</p></td>
</tr>
<tr class="odd">
<td><p>ЛЕВЫЙ</p></td>
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
<td><p>КУХОН</p></td>
<td><p>Синус</p></td>
</tr>
<tr class="even">
<td><p>ATAN</p></td>
<td><p>ВХОДЕ</p></td>
<td><p>КОРЕНЬ</p></td>
</tr>
<tr class="odd">
<td><p>Г</p></td>
<td><p>ПОТРЕБЛЕНИЕ</p></td>
<td><p>TAN</p></td>
</tr>
<tr class="even">
<td><p>COS</p></td>
<td><p>СЛЧИС</p></td>
<td><p>MOD</p></td>
</tr>
<tr class="odd">
<td><p>Кнопка</p></td>
<td><p>ДОЛЛАР</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a>Функции времени & даты

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>курдате</p></td>
<td><p>DAYOFYEAR</p></td>
<td><p>MONTH</p></td>
</tr>
<tr class="even">
<td><p>куртиме</p></td>
<td><p>YEAR</p></td>
<td><p>Я</p></td>
</tr>
<tr class="odd">
<td><p>НАСТРОЕН</p></td>
<td><p>HOUR</p></td>
<td><p>КВАРТАЛЕ</p></td>
</tr>
<tr class="even">
<td><p>DAYOFMONTH</p></td>
<td><p>MINUTE</p></td>
<td><p>MONTHNAME</p></td>
</tr>
<tr class="odd">
<td><p>DAYOFWEEK</p></td>
<td><p>SECOND</p></td>
<td><p>дайнаме</p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a>Преобразование типов данных

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CONVERT</p></td>
<td><p>Строковые литералы могут быть преобразованы в следующие типы данных: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR и SQL_DATETIME.</p></td>
</tr>
</tbody>
</table>

