---
title: Рабочая область для объекта (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711583"
---
# <a name="workspace-object-dao"></a>Рабочая область для объекта (DAO)

**Применимо к**: Access 2013, Office 2013

Объект **рабочей области** определяет именованный сеанса для пользователя. Содержит open баз данных и предоставляет механизмы для одновременных операций и, в рабочих областях Microsoft Access безопасного поддержка рабочей группы.

## <a name="remarks"></a>Замечания

**Рабочая область** — это непостоянные объект, который определяет, как приложение взаимодействует с данными с помощью ядро базы данных Microsoft Access. Используйте объект **рабочей области** для управления текущего сеанса или чтобы начать сеанс обмена дополнительные. В сеансе можно открыть несколько баз данных или подключения к и управление транзакции. Например можно выполнить следующие действия.

- Используйте **имя**, **имя пользователя**и **Тип** свойства именованные сеанс. Сеанс создается область, в которой вы сможете открыть несколько баз данных и проведение один экземпляр вложенных транзакций.

- Используйте метод **Close** для завершения сеанса.

- Используйте метод **OpenDatabase** для открытия одного или нескольких существующих баз данных в **рабочей области**.

- Использование методов **BeginTrans** **CommitTrans**и **отката** для управления обработки в **рабочей области для** вложенных транзакций и использовать несколько объектов **рабочей области** для проведения нескольких одновременных и перекрывающиеся транзакции.

При первом обращайтесь к или использовать объект **рабочей области** , автоматическое создание рабочей области по умолчанию DBEngine.Workspaces(0). Может принимать следующие значения свойства **Name** и **имя пользователя** рабочей области по умолчанию "\#рабочей области по умолчанию\#" и «Администратор», соответственно. Если этот параметр безопасности включен, значение свойства **UserName** — имя пользователя, вошедшего в систему.

При использовании транзакций влияет на все базы данных в указанной **рабочей области** — даже в том случае, если несколько объектов **базы данных** , открываются в **рабочей области**. К примеру вы используйте метод **BeginTrans** , обновить несколько записей в базе данных и затем удалить записи в другую базу данных. При использовании **метода** update и delete операции отмены и откат. Можно создать дополнительные объекты **рабочей области** для управления транзакции независимо друг от друга через объекты **базы данных** .

Объекты **рабочей области** можно создать с помощью метода **CreateWorkspace** . После создания объекта **рабочей области** , необходимо добавить его семейства сайтов **рабочих областей** при необходимости ссылаться на него из коллекции **рабочих областей** .

Можно использовать только что созданный объект **рабочей области** без добавления его в коллекцию **рабочих областей** . Тем не менее должен ссылаться на него переменной объекта, к которому назначена.

Для ссылки на объект **рабочей области** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:

**DBEngine**. **Рабочие области** (0)

**DBEngine**. **Рабочие области** («имя»)

**DBEngine**. **Рабочие области** \! \[имя\]

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.


## <a name="example"></a>Пример

В этом примере создается новый объект рабочей области для Microsoft Access и добавляет его в коллекцию **рабочих областей** . Затем выполняется перечисление семейств сайтов **рабочих областей** и коллекции **свойств** объекта **рабочей области** .

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

В этом примере используется метод **CreateWorkspace** создать рабочую область для Microsoft Access. Затем приведены свойства theworkspace.

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

Следующем примере показано, как использовать транзакции в рабочую область для объектов доступа к данным (DAO).

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


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
