---
title: Сравнение Microsoft Access SQL и ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 195d9f5d882fd252b1b10e937fe851c4830c52d3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713081"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a>Сравнение Microsoft Access SQL и ANSI SQL

**Применимо к**: Access 2013, Office 2013

Ядро СУБД Microsoft Access SQL обычно является совместимым с ANSI-89 уровня 1. Тем не менее некоторые функции ANSI SQL не реализованы в Microsoft Access SQL. С другой стороны Microsoft Access SQL включает в себя зарезервированные слова и функции, не поддерживаемые в формате ANSI SQL.

## <a name="major-differences"></a>Основные различия

- Microsoft Access SQL и ANSI SQL иметь разные зарезервированные слова и типы данных. Для получения дополнительных сведений см [Microsoft Access базы данных модуля SQL зарезервированные слова](sql-reserved-words.md) и [Эквивалентные типы данных ANSI SQL](equivalent-ansi-sql-data-types.md). С помощью Microsoft Access базы данных модуля поставщика OLE DB существуют дополнительные зарезервированные слова.

- **[Между... И](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**
    
  *Expr1* \[Не\] **между** *значение1* **и** *значение2*
    
  В Microsoft Access SQL *значение1* может быть больше, чем *значение2*; в формате ANSI SQL *значение1* должно быть не более чем *значение2.*

- Microsoft Access SQL поддерживает подстановочные знаки ANSI SQL и [подстановочные знаки](using-wildcard-characters-in-string-comparisons.md) , относящиеся к ядру базы данных Microsoft Access для использования с оператор **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** . Использование ANSI и Microsoft Access базы данных модуля подстановочные знаки являются взаимоисключающими. Необходимо использовать один набор знаков, их нельзя смешивать. Подстановочные знаки доступны только при использовании ядро базы данных Microsoft Access и Microsoft Access базы данных модуля поставщика OLE DB. При попытке использовать подстановочные знаки ANSI SQL через Microsoft Access или DAO, они будут интерпретируются как литералы. При использовании Microsoft Access базы данных модуля поставщика OLE DB верно обратное.
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Символ соответствия</p></th>
    <th><p>Microsoft Access SQL</p></th>
    <th><p>ANSI SQL</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Любой знак</p></td>
    <td><p>?</p></td>
    <td><p>_ (знак подчеркивания)</p></td>
    </tr>
    <tr class="even">
    <td><p>Ноль или более символов</p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- Microsoft Access SQL обычно меньше ограничений. Например уменьшение Группировка и порядок выражений.

- Microsoft Access SQL поддерживает более мощного выражения.

## <a name="enhanced-features-of-microsoft-access-sql"></a>Расширенные возможности Microsoft Access SQL

Microsoft Access SQL предоставляет следующие расширенные возможности:

- Оператор [ПРЕОБРАЗОВАНИЯ](transform-statement-microsoft-access-sql.md) , который обеспечивает поддержку перекрестных запросов.

- Дополнительные [агрегатных функций](sql-aggregate-functions-sql.md), таких как **StDev** и **VarP**.

- Объявление [параметров](parameters-declaration-microsoft-access-sql.md) для определения параметров запроса.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>Функции ANSI SQL, не поддерживаемые в Microsoft Access SQL

Microsoft Access SQL не поддерживает следующие функции ANSI SQL:

- Ссылки на РАЗЛИЧНЫЕ статистические функции. К примеру Microsoft Access SQL не разрешает сумм (ЧЕТКИЕ *columnname*).

- Предложения LIMIT TO *nn* СТРОК используется, чтобы ограничить число строк, возвращаемых запросом. [Предложение WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) можно использовать для ограничения области запроса.

