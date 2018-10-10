---
title: QueryDef.ReturnsRecords Property (DAO)
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
ms.openlocfilehash: f1d10a8e348021d88510519c61825714ca434b3b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481555"
---
# <a name="querydefreturnsrecords-property-dao"></a>QueryDef.ReturnsRecords Property (DAO)


**Применимо к**: Access 2013 | Office 2013


Задает или возвращает значение, указывающее, возвращает ли запрос к серверу к внешней базе данных записей (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . ReturnsRecords

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Не все запросы к серверу SQL к внешним базам данных возвращает записи. Например инструкция SQL UPDATE обновляет записи без возвращения записей, пока инструкции SQL SELECT возврата записей. Если запрос возвращает записей, присвойте свойству **ReturnsRecords** значение **True**; Если запрос не возвращает записей, присвойте свойству **ReturnsRecords** значение **False**.


> [!NOTE]
> <P>Необходимо установить свойство <STRONG><A href="querydef-connect-property-dao.md">подключение</A></STRONG> , прежде чем задать свойство <STRONG>ReturnsRecords</STRONG> .</P>



## <a name="example"></a>Пример

В этом примере используется **подключение** и **ReturnsRecords** свойств, выберите верхний пять книги заголовков из базы данных Microsoft SQL Server, используя суммы продаж с начала года. В случае точное совпадение в суммы продаж в примере увеличивается размер списка отображения результатов запроса и печатает сообщение о том, почему это произошло.

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

В этом примере используется свойство **ReturnsRecords** и пользовательское свойство **LogMessages** для создания запроса к серверу, который будет возвращать данные и все сообщения, создаваемые с удаленного сервера.

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

