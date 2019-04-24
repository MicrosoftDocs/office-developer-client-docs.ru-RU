---
title: Свойство QueryDef. ReturnsRecords (DAO)
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
# <a name="querydefreturnsrecords-property-dao"></a>Свойство QueryDef. ReturnsRecords (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, возвращает ли запрос к серверу SQL Server только записи (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Записей

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Замечания

Не все запросы к серверу SQL возвращаются к внешним базам данных и возвращают записи. Например, инструкция SQL UPDATE обновляет записи, не возвращая записи, а инструкция SQL SELECT возвращает записи. Если запрос возвращает записи, задайте для свойства **ReturnsRecords** значение **true**; Если запрос не возвращает записи, задайте для свойства **ReturnsRecords** значение **false**.

> [!NOTE]
> Перед заданием свойства **ReturnsRecords** необходимо задать свойство **[Connect](querydef-connect-property-dao.md)** .

## <a name="example"></a>Пример

В этом примере используются свойства **Connect** и **ReturnsRecords** для выбора пяти основных названий книг из базы данных Microsoft SQL Server на основе сумм продаж с начала года. В случае точного совпадения в суммах продаж в примере увеличивается размер списка, в котором отображаются результаты запроса, и выводится сообщение с объяснением причины возникновения.

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

В этом примере используется свойство **ReturnsRecords** и свойство Custom **логмессажес** для создания запроса к серверу, который будет возвращать данные и все сообщения, созданные удаленным сервером.

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

