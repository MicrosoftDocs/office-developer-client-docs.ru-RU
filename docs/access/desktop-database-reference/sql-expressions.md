---
title: Выражения SQL (справочник по базам данных Access на компьютере)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5bbe9718bfb18ced5f09d2a9396e1e0829d0d81b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308570"
---
# <a name="sql-expressions"></a><span data-ttu-id="ef851-102">Выражения SQL</span><span class="sxs-lookup"><span data-stu-id="ef851-102">SQL expressions</span></span>

<span data-ttu-id="ef851-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef851-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef851-104">Выражение SQL — это строка, из которой частично или полностью состоит инструкция SQL.</span><span class="sxs-lookup"><span data-stu-id="ef851-104">An SQL expression is a string that makes up all or part of an SQL statement.</span></span> <span data-ttu-id="ef851-105">Например, метод **FindFirst**, примененный к объекту **Recordset**, использует выражение SQL, состоящее из условий отбора в [предложении WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="ef851-105">For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="ef851-106">Для выполнения простых арифметических действий и вычисления функций ядро СУБД Microsoft Access использует Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="ef851-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="ef851-107">При этом все операторы, используемые в выражениях SQL ядра СУБД Microsoft Access (за исключением **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** и **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**), определяются службой выражений VBA.</span><span class="sxs-lookup"><span data-stu-id="ef851-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="ef851-108">Кроме того, VBA позволяет использовать для выражений SQL более 100 функций VBA.</span><span class="sxs-lookup"><span data-stu-id="ef851-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="ef851-109">Например, функции VBA можно использовать для создания запроса SQL в режиме конструктора запросов Microsoft Access, а также в режиме DAO с использованием метода **OpenRecordset** в коде Microsoft Visual C++, Microsoft Visual Basic и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ef851-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef851-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ef851-110">See also</span></span>

- [<span data-ttu-id="ef851-111">Основные понятия VBA для Access</span><span class="sxs-lookup"><span data-stu-id="ef851-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
