---
title: Свойство QueryDef.MaxRecords (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6738762ba18289293c67392d47e278066ead071d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301080"
---
# <a name="querydefmaxrecords-property-dao"></a><span data-ttu-id="1083c-102">Свойство QueryDef.MaxRecords (DAO)</span><span class="sxs-lookup"><span data-stu-id="1083c-102">QueryDef.MaxRecords property (DAO)</span></span>

<span data-ttu-id="1083c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1083c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1083c-104">Задает или возвращает максимальное количество записей, возвращаемых из запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="1083c-104">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="1083c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1083c-105">Syntax</span></span>

<span data-ttu-id="1083c-106">*выражения* . MaxRecords</span><span class="sxs-lookup"><span data-stu-id="1083c-106">*expression* .MaxRecords</span></span>

<span data-ttu-id="1083c-107">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="1083c-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1083c-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="1083c-108">Remarks</span></span>

<span data-ttu-id="1083c-109">Значение по умолчанию — 0, что не указывает ограничения на количество возвращенных записей.</span><span class="sxs-lookup"><span data-stu-id="1083c-109">The default value is 0, indicating no limit on the number of records returned.</span></span>

<span data-ttu-id="1083c-110">После того, как количество строк, заданных **MaxRecords,** будет возвращено вашему приложению в **[Recordset,](recordset-object-dao.md)** процессор запроса прекратит возвращать дополнительные записи, даже если больше записей будут иметь право на включение в **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="1083c-110">Once the number of rows specified by **MaxRecords** is returned to your application in a **[Recordset](recordset-object-dao.md)**, the query processor will stop returning additional records even if more records would qualify for inclusion in the **Recordset**.</span></span> <span data-ttu-id="1083c-111">Это свойство полезно в ситуациях, когда ограниченные клиентские ресурсы запрещают управление большим количеством записей.</span><span class="sxs-lookup"><span data-stu-id="1083c-111">This property is useful in situations where limited client resources prohibit management of large numbers of records.</span></span>

> [!NOTE]
> <span data-ttu-id="1083c-112">Свойство **MaxRecords** можно использовать только с источником данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="1083c-112">The **MaxRecords** property can only be used with an ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="1083c-113">Пример</span><span class="sxs-lookup"><span data-stu-id="1083c-113">Example</span></span>

<span data-ttu-id="1083c-114">В этом примере свойство **MaxRecords** использует, чтобы установить ограничение на количество записей, возвращаемой запросом в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="1083c-114">This example uses the **MaxRecords** property to set a limit on how many records are returned by a query on an ODBC data source.</span></span>

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

