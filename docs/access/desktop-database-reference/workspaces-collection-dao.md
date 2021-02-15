---
title: Коллекция Workspaces (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c615be9e92a936486c15377514c2b695f68bb5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308325"
---
# <a name="workspaces-collection-dao"></a><span data-ttu-id="0d3c3-102">Коллекция Workspaces (DAO)</span><span class="sxs-lookup"><span data-stu-id="0d3c3-102">Workspaces collection (DAO)</span></span>


<span data-ttu-id="0d3c3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d3c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d3c3-104">Коллекция **Workspaces** содержит все активные незагруженные объекты **Workspace** объекта **DBEngine.**</span><span class="sxs-lookup"><span data-stu-id="0d3c3-104">A **Workspaces** collection contains all active, unhidden **Workspace** objects of the **DBEngine** object.</span></span> <span data-ttu-id="0d3c3-105">**(Объекты Скрытой** рабочей области не примеся к коллекции и не ссылаются на них переменной, которой они назначены.)</span><span class="sxs-lookup"><span data-stu-id="0d3c3-105">(Hidden **Workspace** objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="remarks"></a><span data-ttu-id="0d3c3-106">Заметки</span><span class="sxs-lookup"><span data-stu-id="0d3c3-106">Remarks</span></span>

<span data-ttu-id="0d3c3-107">Объект **Workspace** используется для управления текущим сеансом или начала дополнительного сеанса.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-107">Use the **Workspace** object to manage the current session or to start an additional session.</span></span>

<span data-ttu-id="0d3c3-108">При первом указании или использовании объекта **Workspace** автоматически создается рабочая область по умолчанию DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="0d3c3-108">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="0d3c3-109">Параметры свойств **Name** и **UserName** рабочей области по умолчанию: "\#Default Workspace\#" и "Admin," соответственно.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-109">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="0d3c3-110">Если включена система безопасности, значение свойства **UserName** соответствует имени пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-110">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="0d3c3-111">Вы можете создавать новые **объекты Workspace** с помощью **[метода CreateWorkspace.](dbengine-createworkspace-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="0d3c3-111">You can create new **Workspace** objects with the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span> <span data-ttu-id="0d3c3-112">После создания объекта **Workspace** его необходимо добавить в коллекцию **Workspaces**, если нужно ссылаться на него из коллекции **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-112">After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span> <span data-ttu-id="0d3c3-113">Однако можно использовать только что созданный **объект Workspace,** не внося его в коллекцию **Workspaces.**</span><span class="sxs-lookup"><span data-stu-id="0d3c3-113">You can, however, use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span>

<span data-ttu-id="0d3c3-114">Чтобы сослаться на объект **Workspace** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-114">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="0d3c3-115">**DBEngine**.**Workspaces**(0)</span><span class="sxs-lookup"><span data-stu-id="0d3c3-115">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="0d3c3-116">**DBEngine**.**Workspaces**("name")</span><span class="sxs-lookup"><span data-stu-id="0d3c3-116">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="0d3c3-117">**DBEngine**.**Workspaces**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="0d3c3-117">**DBEngine**.**Workspaces**\!\[name\]</span></span>


> [!NOTE]
> <span data-ttu-id="0d3c3-118">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-118">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0d3c3-119">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-119">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



## <a name="example"></a><span data-ttu-id="0d3c3-120">Пример</span><span class="sxs-lookup"><span data-stu-id="0d3c3-120">Example</span></span>

<span data-ttu-id="0d3c3-121">В этом примере создается новый объект Microsoft Access Workspace, который добавляется в коллекцию **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-121">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection.</span></span> <span data-ttu-id="0d3c3-122">Затем выполняется перечисление коллекции **Workspaces** и коллекции **Properties** объекта **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-122">It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

В этом примере используется метод **CreateWorkspace** для создания рабочей области Microsoft Access. <span data-ttu-id="0d3c3-124">Затем перечисляются свойства рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0d3c3-124">It then lists the properties of theworkspace.</span></span>

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
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```

