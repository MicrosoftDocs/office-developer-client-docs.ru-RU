---
title: Свойство QueryDef.ODBCTimeout (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ceb3cf0fa2e16af4df23c6511fd6d1421487a409
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922757"
---
# <a name="querydefodbctimeout-property-dao"></a><span data-ttu-id="9bc86-102">Свойство QueryDef.ODBCTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="9bc86-102">QueryDef.ODBCTimeout property (DAO)</span></span>


<span data-ttu-id="9bc86-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bc86-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bc86-104">Указывает количество секунд до ошибку времени ожидания происходит, когда **[QueryDef](querydef-object-dao.md)** выполняется в базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9bc86-104">Indicates the number of seconds to wait before a timeout error occurs when a **[QueryDef](querydef-object-dao.md)** is executed on an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bc86-105">Syntax</span></span>

<span data-ttu-id="9bc86-106">*выражение* . Время ожидания ODBC</span><span class="sxs-lookup"><span data-stu-id="9bc86-106">*expression* .ODBCTimeout</span></span>

<span data-ttu-id="9bc86-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="9bc86-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bc86-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="9bc86-108">Remarks</span></span>

<span data-ttu-id="9bc86-109">Если свойство **время ожидания ODBC** — это значение -1, время ожидания по умолчанию используется текущий параметр свойства **[QueryTimeout](database-querytimeout-property-dao.md)** **[подключения](connection-object-dao.md)** или объекта **[базы данных](database-object-dao.md)** , содержащий **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="9bc86-109">When the **ODBCTimeout** property is set to -1, the timeout defaults to the current setting of the **[QueryTimeout](database-querytimeout-property-dao.md)** property of the **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object that contains the **QueryDef**.</span></span> <span data-ttu-id="9bc86-110">Если свойство **время ожидания ODBC** имеет значение 0, время ожидания ошибок нет.</span><span class="sxs-lookup"><span data-stu-id="9bc86-110">When the **ODBCTimeout** property is set to 0, no timeout error occurs.</span></span>

<span data-ttu-id="9bc86-111">При использовании базы данных ODBC, например Microsoft SQL Server, задержки могут возникнуть из-за сетевой трафик или интенсивное использование сервера ODBC.</span><span class="sxs-lookup"><span data-stu-id="9bc86-111">When you're using an ODBC database, such as Microsoft SQL Server, delays can occur because of network traffic or heavy use of the ODBC server.</span></span> <span data-ttu-id="9bc86-112">Без необходимости неограниченное время, можно указать время ожидания перед сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9bc86-112">Rather than waiting indefinitely, you can specify how long to wait before returning an error.</span></span>

<span data-ttu-id="9bc86-113">**Время ожидания ODBC** свойства объекта **QueryDef** переопределяет значение, назначаемое свойству **QueryTimeout** объекта **подключения** или **базы данных** , содержащего **QueryDef**, но только для этого \*\* QueryDef\*\* объекта.</span><span class="sxs-lookup"><span data-stu-id="9bc86-113">Setting the **ODBCTimeout** property of a **QueryDef** object overrides the value specified by the **QueryTimeout** property of the **Connection** or **Database** object containing the **QueryDef**, but only for that **QueryDef** object.</span></span>

## <a name="example"></a><span data-ttu-id="9bc86-114">Пример</span><span class="sxs-lookup"><span data-stu-id="9bc86-114">Example</span></span>

<span data-ttu-id="9bc86-115">В этом примере используется для отображения как параметр **QueryTimeout** для объекта **базы данных** задает **время ожидания ODBC** по умолчанию для любого объекта **QueryDef** , созданный из свойства **QueryTimeout** и **время ожидания ODBC** Объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="9bc86-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

