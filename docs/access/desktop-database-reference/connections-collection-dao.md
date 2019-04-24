---
title: Коллекция Connections (DAO)
TOCTitle: Connections collection
ms:assetid: 65d073be-a84b-e3f2-cb43-b87ffa60e497
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195178(v=office.15)
ms:contentKeyID: 48545330
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 66f122b7bdaa9069b839cd5884b5da5da48a15f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295788"
---
# <a name="connections-collection-dao"></a>Коллекция Connections (DAO)

**Область применения**: Access 2013, Office 2013

> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.

Коллекция **Connections** содержит текущие объекты **подключения** объекта **Workspace** . (Только для рабочих областей ODBCDirect).

## <a name="remarks"></a>Замечания

При открытии объекта **подключения** он автоматически добавляется в коллекцию **Connections** **рабочей области**. При закрытии объекта **Connection** с помощью метода **[Close](connection-close-method-dao.md)** он удаляется из коллекции Connections **** . Прежде чем закрыть все открытые объекты **[Recordset](recordset-object-dao.md)** в **подключении** , необходимо закрыть их.

При открытии объекта **Connection** создается соответствующий объект **[базы данных](database-object-dao.md)** , который добавляется в коллекцию **[баз данных](databases-collection-dao.md)** в той же **рабочей области**и наоборот. Аналогично, когда вы закрываете **Подключение**, соответствующая **база данных** удаляется из коллекции **баз данных** и т. д.

Значение свойства **Name** для **подключения** — это строка, указывающая путь к файлу базы данных. Чтобы сослаться на объект **Connection** в коллекции по его порядковому номеру или по значению свойства **Name** , используйте любую из следующих синтаксических форм:

- **Connections (подключения** ) нуль

- **Connections (подключения** ) ("*имя*")

- ****\!\[*Имя* подключений\]


> [!NOTE]
> Вы можете открыть один и тот же источник данных несколько раз, создав повторяющиеся имена **** в коллекции Connections. Необходимо назначить объекты **подключения** переменным объектов и ссылаться на них по имени переменной.


## <a name="example"></a>Пример

В этом примере демонстрируется объект **Connection** и коллекция **Connections** , открывая объект **базы данных** и два объекта **подключения** ODBCDirect и указывая свойства, доступные для каждого объекта.

```vb 
Sub ConnectionObjectX() 
 
   Dim wrkAcc as Workspace 
   Dim dbsNorthwind As Database 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conLoop As Connection 
   Dim prpLoop As Property 
 
   ' Open a Database object. 
   Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
      "admin", "", dbUseJet) 
   Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
   ' Create ODBCDirect Workspace object and open Connection 
   ' objects. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
       
   ' Note: The DSNs referenced below must be configured to  
   '       use Microsoft Windows NT Authentication Mode to  
   '       authorize user access to the Microsoft SQL Server. 
   Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
      "ODBC;DATABASE=pubs;DSN=Publishers") 
       
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
      True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   Debug.Print "Database properties:" 
 
   With dbsNorthwind 
      ' Enumerate Properties collection of Database object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         Debug.Print "  " & prpLoop.Name & " = " & _ 
            prpLoop.Value 
         On Error GoTo 0 
      Next prpLoop 
   End With 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   dbsNorthwind.Close 
   conPubs.Close 
   conPubs2.Close 
   wrkAcc.Close 
   wrkODBC.Close 
 
End Sub 
 
```

<br/>

В этом примере используется метод **OpenConnection** с другими параметрами для открытия трех различных объектов **Connection** .

```vb 
Sub OpenConnectionX() 
 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conPubs3 As Connection 
   Dim conLoop As Connection 
 
   ' Create ODBCDirect Workspace object. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
 
   ' Open Connection object using supplied information in  
   ' the connect string. If this information were  
   ' insufficient, you could trap for an error rather than  
   ' go to an ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection1..." 
       
    ' Note: The DSN referenced below must be set to  
    '       use Microsoft Windows NT Authentication Mode to  
    '       authorize user access to the Microsoft SQL Server. 
    Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
       dbDriverNoPrompt, , _ 
       "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   ' Open read-only Connection object based on information  
   ' you enter in the ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection2..." 
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
      dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
   ' Open read-only Connection object by entering only the  
   ' missing information in the ODBC Driver Manager dialog  
   ' box. 
   MsgBox "Opening Connection3..." 
   Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
      dbDriverCompleteRequired, True, _ 
      "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   conPubs.Close 
   conPubs2.Close 
   conPubs3.Close 
   wrkODBC.Close 
 
End Sub 
 
```

