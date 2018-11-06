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
ms.openlocfilehash: 0156983a455c72e4046424def188e41b94705087
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998230"
---
# <a name="querydefmaxrecords-property-dao"></a><span data-ttu-id="f6132-102">Свойство QueryDef.MaxRecords (DAO)</span><span class="sxs-lookup"><span data-stu-id="f6132-102">QueryDef.MaxRecords property (DAO)</span></span>

<span data-ttu-id="f6132-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6132-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6132-104">Задает или возвращает максимальное число записей для возврата из запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="f6132-104">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6132-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6132-105">Syntax</span></span>

<span data-ttu-id="f6132-106">*выражение* . MaxRecords</span><span class="sxs-lookup"><span data-stu-id="f6132-106">*expression* .MaxRecords</span></span>

<span data-ttu-id="f6132-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="f6132-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6132-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6132-108">Remarks</span></span>

<span data-ttu-id="f6132-109">Значение по умолчанию равно 0, указывающее без ограничений на количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="f6132-109">The default value is 0, indicating no limit on the number of records returned.</span></span>

<span data-ttu-id="f6132-110">После возвращения максимальному числу строк, указанного идентификатором **MaxRecords** в приложение в **[набор записей](recordset-object-dao.md)**, обработчик запросов остановит возвращение дополнительные записи даже в том случае, если удовлетворяющих несколько записей для включения в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f6132-110">Once the number of rows specified by **MaxRecords** is returned to your application in a **[Recordset](recordset-object-dao.md)**, the query processor will stop returning additional records even if more records would qualify for inclusion in the **Recordset**.</span></span> <span data-ttu-id="f6132-111">Это свойство можно использовать в ситуациях, где ресурсы ограниченный клиент запретить управление большим количеством записей.</span><span class="sxs-lookup"><span data-stu-id="f6132-111">This property is useful in situations where limited client resources prohibit management of large numbers of records.</span></span>

> [!NOTE]
> <span data-ttu-id="f6132-112">Свойство **MaxRecords** может использоваться только с источником данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="f6132-112">The **MaxRecords** property can only be used with an ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="f6132-113">Пример</span><span class="sxs-lookup"><span data-stu-id="f6132-113">Example</span></span>

<span data-ttu-id="f6132-114">В этом примере используется свойство **MaxRecords** задание ограничения на количество записей возвращаемых запросом на источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="f6132-114">This example uses the **MaxRecords** property to set a limit on how many records are returned by a query on an ODBC data source.</span></span>

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

