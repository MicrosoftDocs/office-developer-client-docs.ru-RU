---
title: Выражения SQL (Справочник по для настольных баз данных Access)
TOCTitle: SQL Expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c42bd49e25ad15a46955e46d60684836e52a9f32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873266"
---
# <a name="sql-expressions"></a><span data-ttu-id="d2a6b-102">Выражения SQL</span><span class="sxs-lookup"><span data-stu-id="d2a6b-102">SQL Expressions</span></span>


<span data-ttu-id="d2a6b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2a6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2a6b-104">Выражение SQL — это строка, которая значительно облегчает копирование полностью или частично инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-104">An SQL expression is a string that makes up all or part of an SQL statement.</span></span> <span data-ttu-id="d2a6b-105">Например метод**FindFirst** **целиком** использует выражение SQL, составляет выбора SQL [предложение WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d2a6b-105">For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="d2a6b-106">Ядро базы данных Microsoft Access используется служба выражений Microsoft® Visual Basic для приложений (или VBA) для выполнения простых вычислений арифметические операторы и функции.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-106">The Microsoft Access database engine uses the Microsoft® Visual Basic® for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="d2a6b-107">Все операторы, используемые в выражения SQL ядра базы данных Microsoft Access (за исключением **[ **[между](https://msdn.microsoft.com/library/ff192436\(v=office.15\))** и **[как](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**)](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** определены службы выражений VBA.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service.</span></span> <span data-ttu-id="d2a6b-108">Кроме того, VBA выражения, которые предлагает служба более 100 функций, которые можно использовать в выражениях SQL.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="d2a6b-109">Например эти функции VBA можно использовать для создания запроса SQL в режиме конструктора запроса Microsoft Access, и можно также использовать эти функции в SQL-запроса в методе DAO **OpenRecordset** Microsoft Visual C++®, Microsoft Visual Basic и Microsoft Код Excel.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++®, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

