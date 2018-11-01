---
title: Workspaces Collection (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4108be7d6c1b2ee66ec5cddf4d26599796bf844c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870270"
---
# <a name="workspaces-collection-dao"></a><span data-ttu-id="b98fd-102">Workspaces Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="b98fd-102">Workspaces Collection (DAO)</span></span>


<span data-ttu-id="b98fd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b98fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b98fd-104">**Рабочие области для** семейства содержит все активные, Показать объекты **рабочей области для** объекта **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b98fd-104">A **Workspaces** collection contains all active, unhidden **Workspace** objects of the **DBEngine** object.</span></span> <span data-ttu-id="b98fd-105">(Скрытые **рабочей области** объекты не добавляется в конец коллекции и ссылается переменная, к которому они назначены.)</span><span class="sxs-lookup"><span data-stu-id="b98fd-105">(Hidden **Workspace** objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="remarks"></a><span data-ttu-id="b98fd-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="b98fd-106">Remarks</span></span>

<span data-ttu-id="b98fd-107">Используйте объект **рабочей области** для управления текущего сеанса или чтобы начать сеанс обмена дополнительные.</span><span class="sxs-lookup"><span data-stu-id="b98fd-107">Use the **Workspace** object to manage the current session or to start an additional session.</span></span>

<span data-ttu-id="b98fd-108">При первом обращайтесь к или использовать объект **рабочей области** , автоматическое создание рабочей области по умолчанию DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="b98fd-108">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="b98fd-109">Может принимать следующие значения свойства **Name** и **имя пользователя** рабочей области по умолчанию "\#рабочей области по умолчанию\#" и «Администратор», соответственно.</span><span class="sxs-lookup"><span data-stu-id="b98fd-109">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="b98fd-110">Если этот параметр безопасности включен, значение свойства **UserName** — имя пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="b98fd-110">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="b98fd-111">Новые объекты **рабочей области** можно создать с помощью метода **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="b98fd-111">You can create new **Workspace** objects with the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span> <span data-ttu-id="b98fd-112">После создания объекта **рабочей области** , необходимо добавить его семейства сайтов **рабочих областей** при необходимости ссылаться на него из коллекции **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="b98fd-112">After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span> <span data-ttu-id="b98fd-113">Тем не менее, можно используйте только что созданный объект **рабочей области** без добавления его в коллекцию **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="b98fd-113">You can, however, use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span>

<span data-ttu-id="b98fd-114">Для ссылки на объект **рабочей области** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="b98fd-114">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="b98fd-115">**DBEngine**. **Рабочие области** (0)</span><span class="sxs-lookup"><span data-stu-id="b98fd-115">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="b98fd-116">**DBEngine**. **Рабочие области** («имя»)</span><span class="sxs-lookup"><span data-stu-id="b98fd-116">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="b98fd-117">**DBEngine**. **Рабочие области** \! \[имя\]</span><span class="sxs-lookup"><span data-stu-id="b98fd-117">**DBEngine**.**Workspaces**\!\[name\]</span></span>


> [!NOTE]
> <span data-ttu-id="b98fd-118">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="b98fd-118">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="b98fd-119">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b98fd-119">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



## <a name="example"></a><span data-ttu-id="b98fd-120">Пример</span><span class="sxs-lookup"><span data-stu-id="b98fd-120">Example</span></span>

<span data-ttu-id="b98fd-121">В этом примере создается новый объект рабочей области для Microsoft Access и добавляет его в коллекцию **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="b98fd-121">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection.</span></span> <span data-ttu-id="b98fd-122">Затем выполняется перечисление семейств сайтов **рабочих областей** и коллекции **свойств** объекта **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="b98fd-122">It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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

В этом примере используется метод **CreateWorkspace** создать рабочую область для Microsoft Access. <span data-ttu-id="b98fd-124">Затем приведены свойства theworkspace.</span><span class="sxs-lookup"><span data-stu-id="b98fd-124">It then lists the properties of theworkspace.</span></span>

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

