---
title: Выражения SQL (справочник по базам данных Access на компьютере)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f38932ed4744e5479c523446f9ab77065f4eb203
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870866"
---
# <a name="sql-expressions"></a>Выражения SQL

**Область применения**: Access 2013, Office 2013

Выражение SQL — это строка, из которой частично или полностью состоит инструкция SQL. Например, метод **FindFirst**, примененный к объекту **Recordset**, использует выражение SQL, состоящее из условий отбора в [предложении WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).

Для выполнения простых арифметических действий и вычисления функций ядро СУБД Microsoft Access использует Microsoft Visual Basic для приложений (VBA). При этом все операторы, используемые в выражениях SQL ядра СУБД Microsoft Access (за исключением **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** и **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**), определяются службой выражений VBA. 

Кроме того, VBA позволяет использовать для выражений SQL более 100 функций VBA. Например, функции VBA можно использовать для создания запроса SQL в режиме конструктора запросов Microsoft Access, а также в режиме DAO с использованием метода **OpenRecordset** в коде Microsoft Visual C++, Microsoft Visual Basic и Microsoft Excel.

## <a name="see-also"></a>См. также

- [Основные понятия VBA для Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
