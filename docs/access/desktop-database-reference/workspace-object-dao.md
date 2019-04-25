---
title: Объект Workspace (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308360"
---
# <a name="workspace-object-dao"></a>Объект Workspace (DAO)

**Область применения**: Access 2013, Office 2013

Объект **Workspace** определяет именованный сеанс для пользователя. Он содержит открытые базы данных и предоставляет механизмы для одновременных транзакций и (в рабочих областях Microsoft Access) поддержку защищенной рабочей группы.

## <a name="remarks"></a>Примечания

Объект **Workspace** — это непостоянный объект, определяющий, как приложение взаимодействует с данными с помощью ядра СУБД Microsoft Access. Объект **Workspace** используется для управления текущим сеансом или начала дополнительного сеанса. В сеансе можно открыть несколько баз данных или подключений и управлять транзакциями. Например, вы можете:

- Использовать свойства **Name**, **UserName** и **Type**, чтобы создать именованный сеанс. Сеанс создает область, в которой можно открыть несколько баз данных и провести один экземпляр вложенных транзакций.

- Использовать метод **Close**, чтобы завершить сеанс.

- Использовать метод **OpenDatabase** метод, чтобы открыть одну или несколько существующих баз данных в объекте **Workspace**.

- Использовать методы **BeginTrans**, **CommitTrans** и **Rollback**, чтобы управлять обработкой вложенных транзакций в объекте **Workspace** и использовать несколько объектов **Workspace** для выполнения нескольких, одновременных и накладывающихся транзакций.

При первом указании или использовании объекта **Workspace** автоматически создается рабочая область по умолчанию DBEngine.Workspaces(0). Параметры свойств **Name** и **UserName** рабочей области по умолчанию: "\#Default Workspace\#" и "Admin," соответственно. Если включена система безопасности, значение свойства **UserName** соответствует имени пользователя, вошедшего в систему.

При использовании транзакции затрагиваются все базы данных в указанном объекте **Workspace**, даже если открыто несколько объектов **Database** в объекте **Workspace**. Предположим, вы используете метод **BeginTrans**, обновляете несколько записей в базе данных, а затем удаляете записи из другой базы данных. Если вы затем используете метод **Rollback**, как операция обновления, так и операция удаления отменяются с откатом результатов. Вы можете создать дополнительные объекты **Workspace**, чтобы независимо управлять транзакциями в объектах **Database**.

Объекты **Workspace** можно создать с помощью метода **CreateWorkspace**. После создания объекта **Workspace** его необходимо добавить в коллекцию **Workspaces**, если нужно ссылаться на него из коллекции **Workspaces**.

Вы можете использовать только что созданный объект **Workspace** без его добавления в коллекцию **Workspaces**. Однако на него нужно ссылаться по объектной переменной, для которой он назначен.

Чтобы сослаться на объект **Workspace** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из указанных ниже синтаксических форм.

**DBEngine**.**Workspaces**(0)

**DBEngine**.**Workspaces**("name")

**DBEngine**.**Workspaces**\!\[name\]

> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.


## <a name="example"></a>Пример

В этом примере создается новый объект Microsoft Access Workspace, который добавляется в коллекцию **Workspaces**. Затем выполняется перечисление коллекции **Workspaces** и коллекции **Properties** объекта **Workspace**.

```vb 
Sub WorkspaceX() 
 
   Dim wrkNewAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   ' Create a new Microsoft Access workspace. 
   Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
      "admin", "", dbUseJet) 
   Workspaces.Append wrkNewAcc 
 
   ' Enumerate the Workspaces collection. 
   For Each wrkLoop In Workspaces 
      With wrkLoop 
         Debug.Print "Properties of " & .Name 
         ' Enumerate the Properties collection of the new 
         ' Workspace object. 
         For Each prpLoop In .Properties 
            On Error Resume Next 
            If prpLoop <> "" Then Debug.Print "  " & _ 
               prpLoop.Name & " = " & prpLoop 
            On Error GoTo 0 
         Next prpLoop 
      End With 
   Next wrkLoop 
 
   wrkNewAcc.Close 
End Sub 
```

<br/>

В этом примере используется метод **CreateWorkspace** для создания рабочей области Microsoft Access. Затем перечисляются свойства рабочей области.

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

В следующем примере показано, как использовать транзакцию в рабочей области объектов доступа к данным (DAO).

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
