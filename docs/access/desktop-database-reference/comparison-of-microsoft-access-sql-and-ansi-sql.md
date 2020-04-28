---
title: Сравнение Microsoft Access SQL и ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e9f30401891452970fdbe80123fc373e26f26c6
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870859"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a>Сравнение Microsoft Access SQL и ANSI SQL

**Область применения**: Access 2013, Office 2013

SQL ядра СУБД Microsoft Access, как правило, соответствует стандарту ANSI-89 Level 1. Однако некоторые функции ANSI SQL не реализованы в Microsoft Access SQL. И наоборот, Microsoft Access SQL включает зарезервированные слова и функции, не поддерживаемые в ANSI SQL.

## <a name="major-differences"></a>Основные различия

- Microsoft Access SQL и ANSI SQL имеют различные зарезервированные слова и типы данных. Для получения дополнительных сведений см [зарезервированные слова SQL для ядра СУБД Microsoft Access](sql-reserved-words.md) и [эквивалентные типы данных ANSI SQL](equivalent-ansi-sql-data-types.md). Использование поставщика OLE DB для ядра СУБД Microsoft Access содержит дополнительные зарезервированные слова.

- **[Между... С](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**
    
  *Выражение1* \[— не\] **между** *Значение1* **и** *value2*
    
  В Microsoft Access SQL *Значение1* может быть больше, чем *value2*. в ANSI SQL *Значение1* должно быть равно или меньше *value2.*

- Microsoft Access SQL поддерживает как подстановочные знаки ANSI SQL, так и [подстановочные знаки](using-wildcard-characters-in-string-comparisons.md) , которые относятся к ядру СУБД Microsoft Access с помощью оператора **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** . Использование подстановочных знаков для механизма базы данных ANSI и Microsoft Access является взаимно исключающим. Вы должны использовать один набор или другой, и они не могут смешиваться. Подстановочные знаки ANSI SQL доступны только при использовании ядра СУБД Microsoft Access и поставщика OLE DB ядра СУБД Microsoft Access. Если вы попытаетесь использовать подстановочные знаки ANSI SQL с помощью Microsoft Access или DAO, они будут интерпретироваться как литералы. Противоположным является true при использовании поставщика OLE DB для ядра СУБД Microsoft Access.
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Сопоставленный символ</p></th>
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


- Microsoft Access SQL, как правило, является менее ограниченным. Например, Допускается группировка и упорядочивание выражений.

- Microsoft Access SQL поддерживает более эффективные выражения.

## <a name="enhanced-features-of-microsoft-access-sql"></a>Расширенные функции Microsoft Access SQL

Microsoft Access SQL предоставляет следующие расширенные возможности:

- Оператор [Transform](transform-statement-microsoft-access-sql.md) , который обеспечивает поддержку перекрестных запросов.

- Дополнительные [статистические функции](sql-aggregate-functions-sql.md), такие как **STDEV** и **ДИСПР**.

- Объявление [параметров](parameters-declaration-microsoft-access-sql.md) для определения запросов с параметрами.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>Функции ANSI SQL, не поддерживаемые в Microsoft Access SQL

Microsoft Access SQL не поддерживает следующие функции ANSI SQL:

- Ссылки на статистические функции DISTINCT. Например, SQL Microsoft Access не позволяет использовать SUM *(DISTINCT)*.

- Предложение LIMIT TO *nn* Rows, используемое для ограничения числа строк, возвращаемых запросом. Для ограничения области запроса можно использовать только [предложение WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) .

