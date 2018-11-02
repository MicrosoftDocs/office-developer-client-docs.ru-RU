---
title: Метод QueryDef.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: ad9e859e-c6fe-496c-a1f2-a000cf4bebcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821728(v=office.15)
ms:contentKeyID: 48547043
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052884
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 165a2703b3b3715ace7326df31477f1f9293be12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926215"
---
# <a name="querydefexecute-method-dao"></a>Метод QueryDef.Execute (DAO)

**Применимо к**: Access 2013, Office 2013

Выполняет инструкции SQL на указанный объект.

## <a name="syntax"></a>Синтаксис

*выражение* . Выполнение (***Параметры***)

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

### <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Параметры</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** можно использовать для доступа к параметрам.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Запрещает разрешение на запись другим пользователям (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(По умолчанию) Выполняет несогласованных обновлений (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Выполняет согласованности обновлений (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Выполняет запрос к серверу. Если этот параметр передает инструкции SQL к базе данных ODBC для обработки (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Откат обновления при возникновении ошибки (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Создает ошибку времени выполнения, если другой пользователь изменение данных, редактировании (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Выполняет асинхронный запрос (только объекты технология ODBCDirect подключения и QueryDef).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Выполняет оператор без первого вызова функции SQLPrepare ODBC API (только объекты технология ODBCDirect подключения и QueryDef).</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.

> [!NOTE]
> Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими. Можно использовать одно или другое, но не оба в экземпляре **OpenRecordset**. С помощью **dbConsistent** и **dbInconsistent** приводит к ошибке.

Используйте свойство **[RecordsAffected](querydef-recordsaffected-property-dao.md)** объекта **[подключения](connection-object-dao.md)**, **[базы данных](database-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** для определения количества записей, влияет на последнюю метод **[Execute](querydef-execute-method-dao.md)** . Например **RecordsAffected** содержит число записей удален, обновляется или вставляется при выполнении запроса. При использовании метода **Execute** для выполнения запроса, свойство **RecordsAffected** объекта **QueryDef** присваивается количество записей.

В рабочей области Microsoft Access, если предоставить синтаксически правильные инструкции SQL и имеют соответствующие разрешения метода **Execute** не ошибка — даже в том случае, если не одной строки можно изменить или удалить. Таким образом всегда используйте параметр **dbFailOnError** , при использовании метода **Execute** для запуска и обновления или удаления запроса. Этот параметр, возникает ошибка времени выполнения и выполняет откат всех изменений успешно Если никакой из записей влияет на блокируется и не может быть обновлении или удалении.

В более ранних версиях ядра базы данных Microsoft Jet SQL операторы автоматически были внедрены в неявные транзакции. Если не удалось выполнить инструкции, с **dbFailOnError** , всей оператор будет выполнен откат. В целях повышения производительности эти неявные транзакции были удалены, начиная с версии 3.5. При обновлении старых кода DAO, необходимо принять во внимание использование явных транзакций вокруг **выполнение** инструкций.

Для достижения наилучшей производительности в рабочую область для Microsoft Access, особенно в многопользовательской среде вложить метода **Execute** внутри транзакции. Используйте метод **[BeginTrans](workspace-begintrans-method-dao.md)** на текущий объект **[рабочей области](workspace-object-dao.md)** , а затем используйте метод **Execute** и завершения транзакции с помощью метода **[CommitTrans](workspace-committrans-method-dao.md)** в **рабочей области**. Это сохраняет изменения на диске и освобождает любые блокировки во время выполнения запроса.

## <a name="example"></a>Пример

В этом примере демонстрируется использование метода **Execute** при вызове из объекта **QueryDef** и объекта **базы данных** . Процедуры ExecuteQueryDef и PrintOutput необходимы для выполнения этой процедуры.

```vb
    Sub ExecuteX() 
     
       Dim dbsNorthwind As Database 
       Dim strSQLChange As String 
       Dim strSQLRestore As String 
       Dim qdfChange As QueryDef 
       Dim rstEmployees As Recordset 
       Dim errLoop As Error 
     
       ' Define two SQL statements for action queries. 
       strSQLChange = "UPDATE Employees SET Country = " & _ 
          "'United States' WHERE Country = 'USA'" 
       strSQLRestore = "UPDATE Employees SET Country = " & _ 
          "'USA' WHERE Country = 'United States'" 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Create temporary QueryDef object. 
       Set qdfChange = dbsNorthwind.CreateQueryDef("", _ 
          strSQLChange) 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "SELECT LastName, Country FROM Employees", _ 
          dbOpenForwardOnly) 
     
       ' Print report of original data. 
       Debug.Print _ 
          "Data in Employees table before executing the query" 
       PrintOutput rstEmployees 
        
       ' Run temporary QueryDef. 
       ExecuteQueryDef qdfChange, rstEmployees 
        
       ' Print report of new data. 
       Debug.Print _ 
          "Data in Employees table after executing the query" 
       PrintOutput rstEmployees 
     
       ' Run action query to restore data. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       dbsNorthwind.Execute strSQLRestore, dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstEmployees.Requery 
     
       ' Print report of restored data. 
       Debug.Print "Data after executing the query " & _ 
          "to restore the original information" 
       PrintOutput rstEmployees 
     
       rstEmployees.Close 
        
       Exit Sub 
        
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub ExecuteQueryDef(qdfTemp As QueryDef, _ 
       rstTemp As Recordset) 
     
       Dim errLoop As Error 
        
       ' Run the specified QueryDef object. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       qdfTemp.Execute dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstTemp.Requery 
        
       Exit Sub 
     
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub PrintOutput(rstTemp As Recordset) 
     
       ' Enumerate Recordset. 
       Do While Not rstTemp.EOF 
          Debug.Print "  " & rstTemp!LastName & _ 
             ", " & rstTemp!Country 
          rstTemp.MoveNext 
       Loop 
     
    End Sub 
```

<br/>

Приведенный ниже показано, как выполнить запрос параметра. Коллекции параметров используется для задания параметра организации запроса myActionQuery до выполнения запроса.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
