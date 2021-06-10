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

Движок базы данных Microsoft Access SQL, как правило, является совместимым с ANSI-89 Level 1. Однако некоторые функции SQL anSI не реализованы в Microsoft Access SQL. И наоборот, microsoft Access SQL содержит зарезервированные слова и функции, не поддерживаемые в ansi SQL.

## <a name="major-differences"></a>Основные различия

- Microsoft Access SQL и ANSI SQL имеют разные зарезервированные слова и типы данных. Дополнительные сведения см. в ядро СУБД SQL Microsoft [Access ядро СУБД SQL](sql-reserved-words.md) и [эквивалентных SQL anSI.](equivalent-ansi-sql-data-types.md) С помощью поставщика ядро СУБД OLE DB есть дополнительные зарезервированные слова.

- **[Между... И](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**
    
  *expr1* \[ NOT \] **Between** *value1* **And** *value2*
    
  В microsoft Access SQL *значение1* может быть больше *значения 2;* в SQL *anSI значение1 должно* быть равно или меньше *значения2.*

- Microsoft Access SQL поддерживает как символы SQL ansi, [](using-wildcard-characters-in-string-comparisons.md) так и символы подмайки, которые являются специфическими для двигателя базы данных Microsoft Access для использования с оператором **[Like.](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** Использование символов подкардных знаков базы данных anSI и Microsoft Access является взаимоисключающими. Необходимо использовать один набор или другой набор и не смешивать их. Подкарды SQL anSI доступны только при использовании двигателя базы данных Microsoft Access и поставщика ядро СУБД OLE DB. Если вы попробуете использовать SQL anSI через Microsoft Access или DAO, они будут интерпретируются как буквальные. При использовании поставщика OLE DB ядро СУБД Microsoft Access ядро СУБД обратное.
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Соответствие символу</p></th>
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


- Microsoft Access SQL, как правило, менее строгим. Например, позволяет группить и заказывать выражения.

- Microsoft Access SQL поддерживает более мощные выражения.

## <a name="enhanced-features-of-microsoft-access-sql"></a>Расширенные возможности microsoft Access SQL

Microsoft Access SQL предоставляет следующие расширенные функции:

- Заявление [TRANSFORM,](transform-statement-microsoft-access-sql.md) которое обеспечивает поддержку запросов на перекрестие.

- Дополнительные [агрегированные](sql-aggregate-functions-sql.md)функции, такие как **StDev** и **VarP.**

- Объявление [PARAMETERS](parameters-declaration-microsoft-access-sql.md) для определения запросов параметров.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>Функции SQL anSI, не поддерживаемые в Microsoft Access SQL

Microsoft Access SQL не поддерживает следующие функции SQL ANSI:

- Ссылки на отдельные совокупные функции. Например, microsoft Access SQL не позволяет sum (DISTINCT *columnname).*

- Пункт LIMIT TO *nn* ROWS, используемый для ограничения количества строк, возвращаемого запросом. Чтобы ограничить область запроса, можно использовать только пункт [WHERE.](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql)

