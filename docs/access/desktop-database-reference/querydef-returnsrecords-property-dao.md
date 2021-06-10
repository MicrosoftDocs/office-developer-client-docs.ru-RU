---
title: Свойство QueryDef.ReturnsRecords (DAO)
TOCTitle: ReturnsRecords Property
ms:assetid: 3d1e538b-4d60-588f-4a20-89f1e2b434e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192701(v=office.15)
ms:contentKeyID: 48544334
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053005
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7d2202aa506750cd0a0d2a84eea5c507c3bb1147
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303341"
---
# <a name="querydefreturnsrecords-property-dao"></a><span data-ttu-id="402fd-102">Свойство QueryDef.ReturnsRecords (DAO)</span><span class="sxs-lookup"><span data-stu-id="402fd-102">QueryDef.ReturnsRecords property (DAO)</span></span>

<span data-ttu-id="402fd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="402fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="402fd-104">Задает или возвращает значение, которое указывает, возвращает ли SQL-сквозной запрос во внешнюю базу данных записи (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="402fd-104">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="402fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="402fd-105">Syntax</span></span>

<span data-ttu-id="402fd-106">*выражения* . ReturnsRecords</span><span class="sxs-lookup"><span data-stu-id="402fd-106">*expression* .ReturnsRecords</span></span>

<span data-ttu-id="402fd-107">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="402fd-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="402fd-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="402fd-108">Remarks</span></span>

<span data-ttu-id="402fd-109">Не все SQL к внешним базам данных возвращают записи.</span><span class="sxs-lookup"><span data-stu-id="402fd-109">Not all SQL pass-through queries to external databases return records.</span></span> <span data-ttu-id="402fd-110">Например, заявление SQL UPDATE обновляет записи без возврата записей, а SQL SELECT возвращает записи.</span><span class="sxs-lookup"><span data-stu-id="402fd-110">For example, an SQL UPDATE statement updates records without returning records, while an SQL SELECT statement does return records.</span></span> <span data-ttu-id="402fd-111">Если запрос возвращает записи, установите свойство **ReturnsRecords** **true;** если запрос не возвращает записи, установите свойство **ReturnsRecords** **false.**</span><span class="sxs-lookup"><span data-stu-id="402fd-111">If the query returns records, set the **ReturnsRecords** property to **True**; if the query doesn't return records, set the **ReturnsRecords** property to **False**.</span></span>

> [!NOTE]
> <span data-ttu-id="402fd-112">Необходимо задать **[Подключение,](querydef-connect-property-dao.md)** прежде чем задать свойство **ReturnsRecords.**</span><span class="sxs-lookup"><span data-stu-id="402fd-112">You must set the **[Connect](querydef-connect-property-dao.md)** property before you set the **ReturnsRecords** property.</span></span>

## <a name="example"></a><span data-ttu-id="402fd-113">Пример</span><span class="sxs-lookup"><span data-stu-id="402fd-113">Example</span></span>

<span data-ttu-id="402fd-114">В этом примере свойства **Подключение** **и ReturnsRecords** для выбора пяти верхних названий книг из Microsoft SQL Server базы данных на основе объемов продаж за год.</span><span class="sxs-lookup"><span data-stu-id="402fd-114">This example uses the **Connect** and **ReturnsRecords** properties to select the top five book titles from a Microsoft SQL Server database based on year-to-date sales amounts.</span></span> <span data-ttu-id="402fd-115">В случае точного совпадения объемов продаж в примере увеличивается размер списка, отображаемого в результатах запроса, и печатается сообщение с объяснением причин этого.</span><span class="sxs-lookup"><span data-stu-id="402fd-115">In the event of an exact match in sales amounts, the example increases the size of the list displaying the results of the query and prints a message explaining why this occurred.</span></span>

```vb 
Sub ClientServerX1() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTopFive As Recordset 
 Dim strMessage As String 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("AllTitles") 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles " & _ 
 "ORDER BY ytd_sales DESC" 
 qdfPassThrough.ReturnsRecords = True 
 
 ' Create a temporary QueryDef object to retrieve 
 ' data from the pass-through query. 
 Set qdfLocal = dbsCurrent.CreateQueryDef("") 
 qdfLocal.SQL = "SELECT TOP 5 title FROM AllTitles" 
 
 Set rstTopFive = qdfLocal.OpenRecordset() 
 
 ' Display results of queries. 
 With rstTopFive 
 strMessage = _ 
 "Our top 5 best-selling books are:" & vbCr 
 
 Do While Not .EOF 
 strMessage = strMessage & " " & !Title & _ 
 vbCr 
 .MoveNext 
 Loop 
 
 If .RecordCount > 5 Then 
 strMessage = strMessage & _ 
 "(There was a tie, resulting in " & _ 
 vbCr & .RecordCount & _ 
 " books in the list.)" 
 End If 
 
 MsgBox strMessage 
 .Close 
 End With 
 
 ' Delete new pass-through query because this is a 
 ' demonstration. 
 dbsCurrent.QueryDefs.Delete "AllTitles" 
 dbsCurrent.Close 
 
```

<br/>

<span data-ttu-id="402fd-116">В этом примере используется свойство **ReturnsRecords** и настраиваемая свойство **LogMessages** для создания сквозного запроса, который будет возвращать данные и любые сообщения, созданные удаленным сервером.</span><span class="sxs-lookup"><span data-stu-id="402fd-116">This example uses the **ReturnsRecords** property and the custom **LogMessages** property to create a pass-through query that will return data and any messages generated by the remote server.</span></span>

```vb 
Sub LogMessagesX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsCurrent As Database 
 Dim qdfTemp As QueryDef 
 Dim prpNew As Property 
 Dim rstTemp As Recordset 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 Set dbsCurrent = wrkAcc.OpenDatabase("DB1.mdb") 
 
 ' Create a QueryDef that will log any messages from the 
 ' server in temporary tables. 
 Set qdfTemp = dbsCurrent.CreateQueryDef("NewQueryDef") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfTemp.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfTemp.SQL = "SELECT * FROM stores" 
 qdfTemp.ReturnsRecords = True 
 Set prpNew = qdfTemp.CreateProperty("LogMessages", _ 
 dbBoolean, True) 
 qdfTemp.Properties.Append prpNew 
 
 ' Execute query and display results. 
 Set rstTemp = qdfTemp.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfTemp.Name 
 dbsCurrent.Close 
 wrkAcc.Close 
 
End Sub 
 
```

