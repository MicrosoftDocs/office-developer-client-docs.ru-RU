---
title: TableDef.RefreshLink Method (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 88cd8083f8dc1b71c574be1e31a8b7b735595090
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876878"
---
# <a name="tabledefrefreshlink-method-dao"></a><span data-ttu-id="91509-102">TableDef.RefreshLink Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="91509-102">TableDef.RefreshLink Method (DAO)</span></span>

<span data-ttu-id="91509-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91509-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="91509-104">Обновляет сведения о подключении для связанной таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="91509-104">Updates the connection information for a linked table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="91509-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91509-105">Syntax</span></span>

<span data-ttu-id="91509-106">*выражение* . RefreshLink</span><span class="sxs-lookup"><span data-stu-id="91509-106">*expression* .RefreshLink</span></span>

<span data-ttu-id="91509-107">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="91509-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91509-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="91509-108">Remarks</span></span>

<span data-ttu-id="91509-109">Чтобы изменить сведения о подключении для связанной таблицы, сброс свойству **[Connect](connection-connect-property-dao.md)** соответствующего объекта **TableDef** и затем использовать метод **RefreshLink** для обновления данных.</span><span class="sxs-lookup"><span data-stu-id="91509-109">To change the connection information for a linked table, reset the **[Connect](connection-connect-property-dao.md)** property of the corresponding **TableDef** object and then use the **RefreshLink** method to update the information.</span></span> <span data-ttu-id="91509-110">С помощью метода **RefreshLink** не изменяет свойства и объекты **[отношений](relation-object-dao.md)** связанной таблицы.</span><span class="sxs-lookup"><span data-stu-id="91509-110">Using **RefreshLink** method doesn't change the linked table's properties and **[Relation](relation-object-dao.md)** objects.</span></span>

<span data-ttu-id="91509-111">Для этого сведения о подключении существовать в все семейства сайтов, связанного с объектом **TableDef** , представляющий связанную таблицу необходимо использовать метод **[Refresh](tabledefs-refresh-method-dao.md)** для каждого семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="91509-111">For this connection information to exist in all collections associated with the **TableDef** object that represents the linked table, you must use the **[Refresh](tabledefs-refresh-method-dao.md)** method on each collection.</span></span>

## <a name="example"></a><span data-ttu-id="91509-112">Пример</span><span class="sxs-lookup"><span data-stu-id="91509-112">Example</span></span>

<span data-ttu-id="91509-113">В этом примере используется метод **RefreshLink** для обновления данных в связанной таблице после его подключения изменения из источника данных в другой.</span><span class="sxs-lookup"><span data-stu-id="91509-113">This example uses the **RefreshLink** method to refresh the data in a linked table after its connection has been changed from one data source to another.</span></span> <span data-ttu-id="91509-114">Процедура RefreshLinkOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="91509-114">The RefreshLinkOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

