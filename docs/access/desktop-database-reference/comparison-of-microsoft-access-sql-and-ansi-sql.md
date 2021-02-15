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

Яд баз SQL Microsoft Access, как правило, соответствует стандарту ANSI-89 уровня 1. Однако некоторые функции SQL ANSI не реализованы в Microsoft Access SQL. И наоборот, microsoft Access SQL зарезервированные слова и функции, не поддерживаемые в anSI SQL.

## <a name="major-differences"></a>Основные различия

- Microsoft Access SQL и ANSI SQL имеют разные зарезервированные слова и типы данных. Дополнительные сведения см. в SQL microsoft [Access Database Engine reserved Words](sql-reserved-words.md) and Equivalent [ANSI SQL Data Types.](equivalent-ansi-sql-data-types.md) При использовании поставщика OLE DB для ядоработки Microsoft Access существуют дополнительные зарезервированные слова.

- **[Между... И](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**
    
  *expr1* \[ NOT \] **Between** *value1* **And** *value2*
    
  В Microsoft Access SQL *значение 1* может быть больше *значения 2;* в anSI SQL *значение 1* должно быть равно или меньше *значения 2.*

- Microsoft Access SQL поддерживает как поддиансовые знаки [](using-wildcard-characters-in-string-comparisons.md) anSI SQL, так и поддиафидные знаки, которые используются в ядере баз данных Microsoft Access с оператором **[Like.](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** Использование поддиапозитных знаков ANSI и ядер базы данных Microsoft Access является взаимоисключающими. Необходимо использовать один набор или другой набор и не может их смешивать. Поддиапные SQL ANSI доступны только при использовании ядер базы данных Microsoft Access и поставщика OLE DB ядер баз данных Microsoft Access. Если вы попытались использовать под SQL ANSI через Microsoft Access или DAO, они будут интерпретируются как литералы. При использовании поставщика OLE DB для ядоработки OLE DB для ядоработки Microsoft Access используется обратное.
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Совпадающий символ</p></th>
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


- Как правило SQL Microsoft Access менее строгий. Например, он разрешает группировку и порядок выражений.

- Microsoft Access SQL поддерживает более мощные выражения.

## <a name="enhanced-features-of-microsoft-access-sql"></a>Расширенные функции microsoft Access SQL

Microsoft Access SQL предоставляет следующие расширенные функции:

- Заявление [TRANSFORM,](transform-statement-microsoft-access-sql.md) которое поддерживает перекрестные запросы.

- Дополнительные [агрегатные функции,](sql-aggregate-functions-sql.md)такие как **StDev** и **VarP.**

- Объявление [PARAMETERS](parameters-declaration-microsoft-access-sql.md) для определения запросов параметров.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>Функции SQL ANSI не поддерживаются в Microsoft Access SQL

Microsoft Access SQL не поддерживает следующие функции SQL ANSI:

- ОТДЕЛЬНЫЕ сводные ссылки на функции. Например, microsoft Access SQL не разрешает СУММ(DISTINCT *columnname).*

- Предложение LIMIT TO *nn* ROWS, используемого для ограничения количества строк, возвращаемого запросом. Для ограничения области [запроса можно](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) использовать только предложение WHERE.

