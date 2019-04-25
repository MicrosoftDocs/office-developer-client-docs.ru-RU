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
# <a name="workspace-object-dao"></a><span data-ttu-id="4cb05-102">Объект Workspace (DAO)</span><span class="sxs-lookup"><span data-stu-id="4cb05-102">Workspace Object (DAO)</span></span>

<span data-ttu-id="4cb05-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4cb05-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4cb05-104">Объект **Workspace** определяет именованный сеанс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="4cb05-104">A **Workspace** object defines a named session for a user.</span></span> <span data-ttu-id="4cb05-105">Он содержит открытые базы данных и предоставляет механизмы для одновременных транзакций и (в рабочих областях Microsoft Access) поддержку защищенной рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="4cb05-105">It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cb05-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cb05-106">Remarks</span></span>

<span data-ttu-id="4cb05-107">Объект **Workspace** — это непостоянный объект, определяющий, как приложение взаимодействует с данными с помощью ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4cb05-107">A **Workspace** is a non-persistent object that defines how your application interacts with data by using the Microsoft Access database engine.</span></span> <span data-ttu-id="4cb05-108">Объект **Workspace** используется для управления текущим сеансом или начала дополнительного сеанса.</span><span class="sxs-lookup"><span data-stu-id="4cb05-108">Use the **Workspace** object to manage the current session or to start an additional session.</span></span> <span data-ttu-id="4cb05-109">В сеансе можно открыть несколько баз данных или подключений и управлять транзакциями.</span><span class="sxs-lookup"><span data-stu-id="4cb05-109">In a session, you can open multiple databases or connections, and manage transactions.</span></span> <span data-ttu-id="4cb05-110">Например, вы можете:</span><span class="sxs-lookup"><span data-stu-id="4cb05-110">For example, you can:</span></span>

- <span data-ttu-id="4cb05-111">Использовать свойства **Name**, **UserName** и **Type**, чтобы создать именованный сеанс.</span><span class="sxs-lookup"><span data-stu-id="4cb05-111">Use the **Name**, **UserName**, and **Type** properties to establish a named session.</span></span> <span data-ttu-id="4cb05-112">Сеанс создает область, в которой можно открыть несколько баз данных и провести один экземпляр вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="4cb05-112">The session creates a scope in which you can open multiple databases and conduct one instance of nested transactions.</span></span>

- <span data-ttu-id="4cb05-113">Использовать метод **Close**, чтобы завершить сеанс.</span><span class="sxs-lookup"><span data-stu-id="4cb05-113">Use the **Close** method to terminate a session.</span></span>

- <span data-ttu-id="4cb05-114">Использовать метод **OpenDatabase** метод, чтобы открыть одну или несколько существующих баз данных в объекте **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-114">Use the **OpenDatabase** method to open one or more existing databases on a **Workspace**.</span></span>

- <span data-ttu-id="4cb05-115">Использовать методы **BeginTrans**, **CommitTrans** и **Rollback**, чтобы управлять обработкой вложенных транзакций в объекте **Workspace** и использовать несколько объектов **Workspace** для выполнения нескольких, одновременных и накладывающихся транзакций.</span><span class="sxs-lookup"><span data-stu-id="4cb05-115">Use the **BeginTrans**, **CommitTrans**, and **Rollback** methods to manage nested transaction processing within a **Workspace** and use several **Workspace** objects to conduct multiple, simultaneous, and overlapping transactions.</span></span>

<span data-ttu-id="4cb05-116">При первом указании или использовании объекта **Workspace** автоматически создается рабочая область по умолчанию DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="4cb05-116">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="4cb05-117">Параметры свойств **Name** и **UserName** рабочей области по умолчанию: "\#Default Workspace\#" и "Admin," соответственно.</span><span class="sxs-lookup"><span data-stu-id="4cb05-117">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="4cb05-118">Если включена система безопасности, значение свойства **UserName** соответствует имени пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="4cb05-118">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="4cb05-119">При использовании транзакции затрагиваются все базы данных в указанном объекте **Workspace**, даже если открыто несколько объектов **Database** в объекте **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-119">When you use transactions, all databases in the specified **Workspace** are affected— even if multiple **Database** objects are opened in the **Workspace**.</span></span> <span data-ttu-id="4cb05-120">Предположим, вы используете метод **BeginTrans**, обновляете несколько записей в базе данных, а затем удаляете записи из другой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4cb05-120">For example, you use a **BeginTrans** method, update several records in a database, and then delete records in another database.</span></span> <span data-ttu-id="4cb05-121">Если вы затем используете метод **Rollback**, как операция обновления, так и операция удаления отменяются с откатом результатов.</span><span class="sxs-lookup"><span data-stu-id="4cb05-121">If you then use the **Rollback** method, both the update and delete operations are canceled and rolled back.</span></span> <span data-ttu-id="4cb05-122">Вы можете создать дополнительные объекты **Workspace**, чтобы независимо управлять транзакциями в объектах **Database**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-122">You can create additional **Workspace** objects to manage transactions independently across **Database** objects.</span></span>

<span data-ttu-id="4cb05-123">Объекты **Workspace** можно создать с помощью метода **CreateWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-123">You can create **Workspace** objects with the **CreateWorkspace** method.</span></span> <span data-ttu-id="4cb05-124">После создания объекта **Workspace** его необходимо добавить в коллекцию **Workspaces**, если нужно ссылаться на него из коллекции **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-124">After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span>

<span data-ttu-id="4cb05-125">Вы можете использовать только что созданный объект **Workspace** без его добавления в коллекцию **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-125">You can use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span> <span data-ttu-id="4cb05-126">Однако на него нужно ссылаться по объектной переменной, для которой он назначен.</span><span class="sxs-lookup"><span data-stu-id="4cb05-126">However, you must refer to it by the object variable to which you have assigned it.</span></span>

<span data-ttu-id="4cb05-127">Чтобы сослаться на объект **Workspace** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="4cb05-127">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="4cb05-128">**DBEngine**.**Workspaces**(0)</span><span class="sxs-lookup"><span data-stu-id="4cb05-128">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="4cb05-129">**DBEngine**.**Workspaces**("name")</span><span class="sxs-lookup"><span data-stu-id="4cb05-129">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="4cb05-130">**DBEngine**.**Workspaces**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="4cb05-130">**DBEngine**.**Workspaces**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="4cb05-131">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="4cb05-131">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="4cb05-132">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4cb05-132">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


## <a name="example"></a><span data-ttu-id="4cb05-133">Пример</span><span class="sxs-lookup"><span data-stu-id="4cb05-133">Example</span></span>

<span data-ttu-id="4cb05-134">В этом примере создается новый объект Microsoft Access Workspace, который добавляется в коллекцию **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-134">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection.</span></span> <span data-ttu-id="4cb05-135">Затем выполняется перечисление коллекции **Workspaces** и коллекции **Properties** объекта **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="4cb05-135">It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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

В этом примере используется метод **CreateWorkspace** для создания рабочей области Microsoft Access. <span data-ttu-id="4cb05-137">Затем перечисляются свойства рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4cb05-137">It then lists the properties of theworkspace.</span></span>

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

<span data-ttu-id="4cb05-138">В следующем примере показано, как использовать транзакцию в рабочей области объектов доступа к данным (DAO).</span><span class="sxs-lookup"><span data-stu-id="4cb05-138">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="4cb05-139">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4cb05-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
