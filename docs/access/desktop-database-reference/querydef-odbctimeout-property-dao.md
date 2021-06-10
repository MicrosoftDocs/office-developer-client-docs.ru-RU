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
localization_priority: Normal
ms.openlocfilehash: 2d34aee30e649b1c25ddc6af8078da2af9dd3b84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301003"
---
# <a name="querydefodbctimeout-property-dao"></a><span data-ttu-id="2b05d-102">Свойство QueryDef.ODBCTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b05d-102">QueryDef.ODBCTimeout property (DAO)</span></span>


<span data-ttu-id="2b05d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b05d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b05d-104">Указывает количество секунд, которые нужно ждать до возникновения ошибки ожидания при выполнении **[запроса в](querydef-object-dao.md)** базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="2b05d-104">Indicates the number of seconds to wait before a timeout error occurs when a **[QueryDef](querydef-object-dao.md)** is executed on an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b05d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b05d-105">Syntax</span></span>

<span data-ttu-id="2b05d-106">*выражения* . ODBCTimeout</span><span class="sxs-lookup"><span data-stu-id="2b05d-106">*expression* .ODBCTimeout</span></span>

<span data-ttu-id="2b05d-107">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="2b05d-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b05d-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b05d-108">Remarks</span></span>

<span data-ttu-id="2b05d-109">Когда свойство **ODBCTimeout** задает значение -1, по умолчанию по умолчанию будет установлен текущий параметр свойства **[QueryTimeout](database-querytimeout-property-dao.md)** объекта **[Подключение](connection-object-dao.md)** или **[База](database-object-dao.md)** данных, содержащий **объект QueryDef.**</span><span class="sxs-lookup"><span data-stu-id="2b05d-109">When the **ODBCTimeout** property is set to -1, the timeout defaults to the current setting of the **[QueryTimeout](database-querytimeout-property-dao.md)** property of the **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object that contains the **QueryDef**.</span></span> <span data-ttu-id="2b05d-110">Если свойство **ODBCTimeout** настроено на 0, ошибки в периодике не происходит.</span><span class="sxs-lookup"><span data-stu-id="2b05d-110">When the **ODBCTimeout** property is set to 0, no timeout error occurs.</span></span>

<span data-ttu-id="2b05d-111">При использовании базы данных ODBC, например Microsoft SQL Server, могут возникать задержки из-за сетевого трафика или интенсивного использования сервера ODBC.</span><span class="sxs-lookup"><span data-stu-id="2b05d-111">When you're using an ODBC database, such as Microsoft SQL Server, delays can occur because of network traffic or heavy use of the ODBC server.</span></span> <span data-ttu-id="2b05d-112">Вместо того, чтобы ждать бесконечно, можно указать, как долго ждать, прежде чем возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="2b05d-112">Rather than waiting indefinitely, you can specify how long to wait before returning an error.</span></span>

<span data-ttu-id="2b05d-113">Настройка **свойства ODBCTimeout** объекта **QueryDef** переопределяет значение, указанное **свойством QueryTimeout** объекта Connection **или** **Database,** содержащего **объект QueryDef,** но только для этого объекта **QueryDef.**</span><span class="sxs-lookup"><span data-stu-id="2b05d-113">Setting the **ODBCTimeout** property of a **QueryDef** object overrides the value specified by the **QueryTimeout** property of the **Connection** or **Database** object containing the **QueryDef**, but only for that **QueryDef** object.</span></span>

## <a name="example"></a><span data-ttu-id="2b05d-114">Пример</span><span class="sxs-lookup"><span data-stu-id="2b05d-114">Example</span></span>

<span data-ttu-id="2b05d-115">В этом примере используются свойства **ODBCTimeout** и **QueryTimeout,** чтобы показать, как параметр **QueryTimeout** на объекте **Базы** данных задает по умолчанию **параметр ODBCTimeout** для любых объектов **QueryDef,** созданных из объекта **Database.**</span><span class="sxs-lookup"><span data-stu-id="2b05d-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

