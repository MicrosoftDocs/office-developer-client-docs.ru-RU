---
title: Свойство Database. QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f47d6c51079bf36cb7e1ca596a3476f1a7219c5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294740"
---
# <a name="databasequerytimeout-property-dao"></a><span data-ttu-id="21e59-102">Свойство Database. QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="21e59-102">Database.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="21e59-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21e59-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="21e59-104">Задает или возвращает значение, задающее время ожидания в секундах до возникновения ошибки времени ожидания при выполнении запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="21e59-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21e59-105">Syntax</span></span>

<span data-ttu-id="21e59-106">*Expression* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="21e59-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="21e59-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="21e59-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21e59-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="21e59-108">Remarks</span></span>

<span data-ttu-id="21e59-109">Значение по умолчанию  60.</span><span class="sxs-lookup"><span data-stu-id="21e59-109">The default value is 60.</span></span>

<span data-ttu-id="21e59-110">При использовании базы данных ODBC, такой как Microsoft SQL Server, могут возникать задержки из-за сетевого трафика или интенсивного использования сервера ODBC.</span><span class="sxs-lookup"><span data-stu-id="21e59-110">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server.</span></span> <span data-ttu-id="21e59-111">Вместо неопределенного периода ожидания можно указать время ожидания.</span><span class="sxs-lookup"><span data-stu-id="21e59-111">Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="21e59-112">При использовании **QueryTimeOut** с **[подключением](connection-object-dao.md)** или объектом **[базы данных](database-object-dao.md)** он задает глобальное значение для всех запросов, связанных с базой данных.</span><span class="sxs-lookup"><span data-stu-id="21e59-112">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database.</span></span> <span data-ttu-id="21e59-113">Вы можете переопределить это значение для определенного запроса, задав свойство **ODBCTimeout** для определенного объекта **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="21e59-113">You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="example"></a><span data-ttu-id="21e59-114">Пример</span><span class="sxs-lookup"><span data-stu-id="21e59-114">Example</span></span>

<span data-ttu-id="21e59-115">В этом примере используются свойства **ODBCTimeout** и **QueryTimeOut** , чтобы показать, как параметр **QueryTimeOut** в объекте **Database** задает значение по умолчанию **ODBCTimeout** для объектов **QueryDef** , созданных из объекта **Database** .</span><span class="sxs-lookup"><span data-stu-id="21e59-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

