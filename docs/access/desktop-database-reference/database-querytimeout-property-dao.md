---
title: Database.QueryTimeout Property (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e924dfb89cb67ffa4bc8ec29d0c24a7c61fcb5b5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887966"
---
# <a name="databasequerytimeout-property-dao"></a><span data-ttu-id="df1ed-102">Database.QueryTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="df1ed-102">Database.QueryTimeout Property (DAO)</span></span>


<span data-ttu-id="df1ed-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df1ed-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="df1ed-104">Задает или возвращает значение, указывающее количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса на источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="df1ed-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df1ed-105">Syntax</span></span>

<span data-ttu-id="df1ed-106">*выражение* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="df1ed-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="df1ed-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="df1ed-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="df1ed-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="df1ed-108">Remarks</span></span>

<span data-ttu-id="df1ed-109">Значение по умолчанию — 60.</span><span class="sxs-lookup"><span data-stu-id="df1ed-109">The default value is 60.</span></span>

<span data-ttu-id="df1ed-110">При использовании базы данных ODBC, например Microsoft SQL Server, могут возникнуть задержки из-за сетевой трафик или высокая интенсивность операций использования ODBC сервера.</span><span class="sxs-lookup"><span data-stu-id="df1ed-110">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server.</span></span> <span data-ttu-id="df1ed-111">Вместо ожидания, можно указать время ожидания.</span><span class="sxs-lookup"><span data-stu-id="df1ed-111">Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="df1ed-112">При использовании **QueryTimeout** с объектом **[подключения](connection-object-dao.md)** или **[базы данных](database-object-dao.md)** , задает глобальное значение для всех запросов, связанной с базой данных.</span><span class="sxs-lookup"><span data-stu-id="df1ed-112">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database.</span></span> <span data-ttu-id="df1ed-113">Можно переопределить это значение для конкретного запроса, задав свойство **время ожидания ODBC** определенного объекта **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="df1ed-113">You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="example"></a><span data-ttu-id="df1ed-114">Пример</span><span class="sxs-lookup"><span data-stu-id="df1ed-114">Example</span></span>

<span data-ttu-id="df1ed-115">В этом примере используется для отображения как параметр **QueryTimeout** для объекта **базы данных** задает **время ожидания ODBC** по умолчанию для любого объекта **QueryDef** , созданный из свойства **QueryTimeout** и **время ожидания ODBC** Объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="df1ed-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

