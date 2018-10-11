---
title: Workspace Object (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86631fb15da775c3c5740dce704c519e2912ffba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481753"
---
# <a name="workspace-object-dao"></a><span data-ttu-id="9b3c7-102">Workspace Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b3c7-102">Workspace Object (DAO)</span></span>

<span data-ttu-id="9b3c7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b3c7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9b3c7-104">Объект **рабочей области** определяет именованный сеанса для пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-104">A **Workspace** object defines a named session for a user.</span></span> <span data-ttu-id="9b3c7-105">Содержит open баз данных и предоставляет механизмы для одновременных операций и, в рабочих областях Microsoft Access безопасного поддержка рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-105">It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b3c7-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b3c7-106">Remarks</span></span>

<span data-ttu-id="9b3c7-107">**Рабочая область** — это непостоянные объект, который определяет, как приложение взаимодействует с данными с помощью ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-107">A **Workspace** is a non-persistent object that defines how your application interacts with data by using the Microsoft Access database engine.</span></span> <span data-ttu-id="9b3c7-108">Используйте объект **рабочей области** для управления текущего сеанса или чтобы начать сеанс обмена дополнительные.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-108">Use the **Workspace** object to manage the current session or to start an additional session.</span></span> <span data-ttu-id="9b3c7-109">В сеансе можно открыть несколько баз данных или подключения к и управление транзакции.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-109">In a session, you can open multiple databases or connections, and manage transactions.</span></span> <span data-ttu-id="9b3c7-110">Например можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-110">For example, you can:</span></span>

- <span data-ttu-id="9b3c7-111">Используйте **имя**, **имя пользователя**и **Тип** свойства именованные сеанс.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-111">Use the **Name**, **UserName**, and **Type** properties to establish a named session.</span></span> <span data-ttu-id="9b3c7-112">Сеанс создается область, в которой вы сможете открыть несколько баз данных и проведение один экземпляр вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-112">The session creates a scope in which you can open multiple databases and conduct one instance of nested transactions.</span></span>

- <span data-ttu-id="9b3c7-113">Используйте метод **Close** для завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-113">Use the **Close** method to terminate a session.</span></span>

- <span data-ttu-id="9b3c7-114">Используйте метод **OpenDatabase** для открытия одного или нескольких существующих баз данных в **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-114">Use the **OpenDatabase** method to open one or more existing databases on a **Workspace**.</span></span>

- <span data-ttu-id="9b3c7-115">Использование методов **BeginTrans** **CommitTrans**и **отката** для управления обработки в **рабочей области для** вложенных транзакций и использовать несколько объектов **рабочей области** для проведения нескольких одновременных и перекрывающиеся транзакции.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-115">Use the **BeginTrans**, **CommitTrans**, and **Rollback** methods to manage nested transaction processing within a **Workspace** and use several **Workspace** objects to conduct multiple, simultaneous, and overlapping transactions.</span></span>

<span data-ttu-id="9b3c7-116">При первом обращайтесь к или использовать объект **рабочей области** , автоматическое создание рабочей области по умолчанию DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="9b3c7-116">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="9b3c7-117">Может принимать следующие значения свойства **Name** и **имя пользователя** рабочей области по умолчанию "\#рабочей области по умолчанию\#" и «Администратор», соответственно.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-117">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="9b3c7-118">Если этот параметр безопасности включен, значение свойства **UserName** — имя пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-118">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="9b3c7-119">При использовании транзакций влияет на все базы данных в указанной **рабочей области** — даже в том случае, если несколько объектов **базы данных** , открываются в **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-119">When you use transactions, all databases in the specified **Workspace** are affected— even if multiple **Database** objects are opened in the **Workspace**.</span></span> <span data-ttu-id="9b3c7-120">К примеру вы используйте метод **BeginTrans** , обновить несколько записей в базе данных и затем удалить записи в другую базу данных.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-120">For example, you use a **BeginTrans** method, update several records in a database, and then delete records in another database.</span></span> <span data-ttu-id="9b3c7-121">При использовании **метода** update и delete операции отмены и откат.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-121">If you then use the **Rollback** method, both the update and delete operations are canceled and rolled back.</span></span> <span data-ttu-id="9b3c7-122">Можно создать дополнительные объекты **рабочей области** для управления транзакции независимо друг от друга через объекты **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="9b3c7-122">You can create additional **Workspace** objects to manage transactions independently across **Database** objects.</span></span>

<span data-ttu-id="9b3c7-123">Объекты **рабочей области** можно создать с помощью метода **CreateWorkspace** .</span><span class="sxs-lookup"><span data-stu-id="9b3c7-123">You can create **Workspace** objects with the **CreateWorkspace** method.</span></span> <span data-ttu-id="9b3c7-124">После создания объекта **рабочей области** , необходимо добавить его семейства сайтов **рабочих областей** при необходимости ссылаться на него из коллекции **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="9b3c7-124">After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span>

<span data-ttu-id="9b3c7-125">Можно использовать только что созданный объект **рабочей области** без добавления его в коллекцию **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="9b3c7-125">You can use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span> <span data-ttu-id="9b3c7-126">Тем не менее должен ссылаться на него переменной объекта, к которому назначена.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-126">However, you must refer to it by the object variable to which you have assigned it.</span></span>

<span data-ttu-id="9b3c7-127">Для ссылки на объект **рабочей области** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="9b3c7-127">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="9b3c7-128">**DBEngine**. **Рабочие области** (0)</span><span class="sxs-lookup"><span data-stu-id="9b3c7-128">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="9b3c7-129">**DBEngine**. **Рабочие области** («имя»)</span><span class="sxs-lookup"><span data-stu-id="9b3c7-129">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="9b3c7-130">**DBEngine**. **Рабочие области** \! \[имя\]</span><span class="sxs-lookup"><span data-stu-id="9b3c7-130">**DBEngine**.**Workspaces**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c7-131">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-131">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="9b3c7-132">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-132">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


## <a name="example"></a><span data-ttu-id="9b3c7-133">Пример</span><span class="sxs-lookup"><span data-stu-id="9b3c7-133">Example</span></span>

<span data-ttu-id="9b3c7-134">В этом примере создается новый объект рабочей области для Microsoft Access и добавляет его в коллекцию **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="9b3c7-134">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection.</span></span> <span data-ttu-id="9b3c7-135">Затем выполняется перечисление семейств сайтов **рабочих областей** и коллекции **свойств** объекта **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="9b3c7-135">It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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

В этом примере используется метод **CreateWorkspace** создать рабочую область для Microsoft Access. <span data-ttu-id="9b3c7-137">Затем приведены свойства theworkspace.</span><span class="sxs-lookup"><span data-stu-id="9b3c7-137">It then lists the properties of theworkspace.</span></span>

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

<span data-ttu-id="9b3c7-138">Следующем примере показано, как использовать транзакции в рабочую область для объектов доступа к данным (DAO).</span><span class="sxs-lookup"><span data-stu-id="9b3c7-138">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="9b3c7-139">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9b3c7-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
