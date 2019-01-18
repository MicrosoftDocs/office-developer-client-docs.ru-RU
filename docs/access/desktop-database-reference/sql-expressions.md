---
title: Выражения SQL (Справочник по для настольных баз данных Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5bbe9718bfb18ced5f09d2a9396e1e0829d0d81b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710547"
---
# <a name="sql-expressions"></a>Выражения SQL

**Применимо к**: Access 2013, Office 2013

Выражение SQL — это строка, которая значительно облегчает копирование полностью или частично инструкции SQL. Например метод **FindFirst** **целиком** использует выражение SQL, составляет выбора SQL [предложение WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).

Ядро базы данных Microsoft Access используется служба выражений Microsoft Visual Basic для приложений (или VBA) для выполнения простых вычислений арифметические операторы и функции. Все операторы, используемые в выражения SQL ядра базы данных Microsoft Access (за исключением **[ **[между](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)** и **[как](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**)](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** определены службы выражений VBA. Кроме того, VBA выражения, которые предлагает служба более 100 функций, которые можно использовать в выражениях SQL. Например эти функции VBA можно использовать для создания запроса SQL в режиме конструктора запроса Microsoft Access, и можно также использовать эти функции в SQL-запроса в методе DAO **OpenRecordset** в Microsoft Visual C++, Microsoft Visual Basic и Microsoft Код Excel.

## <a name="see-also"></a>См. также

- [Основные понятия Access VBA](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
