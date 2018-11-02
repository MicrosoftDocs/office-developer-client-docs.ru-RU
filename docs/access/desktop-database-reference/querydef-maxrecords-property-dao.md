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
ms.openlocfilehash: 5893dd0c6538a1812dc9b19aede2b9114899d68c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927128"
---
# <a name="querydefmaxrecords-property-dao"></a><span data-ttu-id="9fb38-102">Свойство QueryDef.MaxRecords (DAO)</span><span class="sxs-lookup"><span data-stu-id="9fb38-102">QueryDef.MaxRecords property (DAO)</span></span>


<span data-ttu-id="9fb38-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9fb38-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9fb38-104">Задает или возвращает максимальное число записей для возврата из запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9fb38-104">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fb38-105">Syntax</span></span>

<span data-ttu-id="9fb38-106">*выражение* . MaxRecords</span><span class="sxs-lookup"><span data-stu-id="9fb38-106">*expression* .MaxRecords</span></span>

<span data-ttu-id="9fb38-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="9fb38-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb38-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fb38-108">Remarks</span></span>

<span data-ttu-id="9fb38-109">Значение по умолчанию равно 0, указывающее без ограничений на количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="9fb38-109">The default value is 0, indicating no limit on the number of records returned.</span></span>

<span data-ttu-id="9fb38-110">После возвращения максимальному числу строк, указанного идентификатором **MaxRecords** в приложение в **[набор записей](recordset-object-dao.md)**, обработчик запросов остановит возвращение дополнительные записи даже в том случае, если удовлетворяющих несколько записей для включения в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="9fb38-110">Once the number of rows specified by **MaxRecords** is returned to your application in a **[Recordset](recordset-object-dao.md)**, the query processor will stop returning additional records even if more records would qualify for inclusion in the **Recordset**.</span></span> <span data-ttu-id="9fb38-111">Это свойство можно использовать в ситуациях, где ресурсы ограниченный клиент запретить управление большим количеством записей.</span><span class="sxs-lookup"><span data-stu-id="9fb38-111">This property is useful in situations where limited client resources prohibit management of large numbers of records.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9fb38-112">Свойство <STRONG>MaxRecords</STRONG> может использоваться только с источником данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9fb38-112">The <STRONG>MaxRecords</STRONG> property can only be used with an ODBC data source.</span></span></P>



## <a name="example"></a><span data-ttu-id="9fb38-113">Пример</span><span class="sxs-lookup"><span data-stu-id="9fb38-113">Example</span></span>

<span data-ttu-id="9fb38-114">В этом примере используется свойство **MaxRecords** задание ограничения на количество записей возвращаемых запросом на источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9fb38-114">This example uses the **MaxRecords** property to set a limit on how many records are returned by a query on an ODBC data source.</span></span>

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

