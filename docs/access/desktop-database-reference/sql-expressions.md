---
title: Выражения SQL (Справочник по для настольных баз данных Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a8d340f008fd198068d6dacc1b2bf847838ede1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025737"
---
# <a name="sql-expressions"></a><span data-ttu-id="1d56d-102">Выражения SQL</span><span class="sxs-lookup"><span data-stu-id="1d56d-102">SQL expressions</span></span>

<span data-ttu-id="1d56d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d56d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d56d-104">Выражение SQL — это строка, которая значительно облегчает копирование полностью или частично инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="1d56d-104">An SQL expression is a string that makes up all or part of an SQL statement.</span></span> <span data-ttu-id="1d56d-105">Например метод **FindFirst** **целиком** использует выражение SQL, составляет выбора SQL [предложение WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="1d56d-105">For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="1d56d-106">Ядро базы данных Microsoft Access используется служба выражений Microsoft Visual Basic для приложений (или VBA) для выполнения простых вычислений арифметические операторы и функции.</span><span class="sxs-lookup"><span data-stu-id="1d56d-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="1d56d-107">Все операторы, используемые в выражения SQL ядра базы данных Microsoft Access (за исключением **[ **[между](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)** и **[как](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**)](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** определены службы выражений VBA.</span><span class="sxs-lookup"><span data-stu-id="1d56d-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="1d56d-108">Кроме того, VBA выражения, которые предлагает служба более 100 функций, которые можно использовать в выражениях SQL.</span><span class="sxs-lookup"><span data-stu-id="1d56d-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="1d56d-109">Например эти функции VBA можно использовать для создания запроса SQL в режиме конструктора запроса Microsoft Access, и можно также использовать эти функции в SQL-запроса в методе DAO **OpenRecordset** в Microsoft Visual C++, Microsoft Visual Basic и Microsoft Код Excel.</span><span class="sxs-lookup"><span data-stu-id="1d56d-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d56d-110">См. также</span><span class="sxs-lookup"><span data-stu-id="1d56d-110">See also</span></span>

- [<span data-ttu-id="1d56d-111">Основные понятия Access VBA</span><span class="sxs-lookup"><span data-stu-id="1d56d-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)