---
title: Коллекция workspaces (DAO)
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
# <a name="workspaces-collection-dao"></a>Коллекция workspaces (DAO)


**Область применения**: Access 2013, Office 2013

Коллекция **Workspaces** содержит все активные незавершенные объекты **рабочей** области **объекта DBEngine.** **(Скрытые объекты** рабочей области не примыкают к коллекции и ссылаются на переменную, к которой они назначены.)

## <a name="remarks"></a>Примечания

Объект **Workspace** используется для управления текущим сеансом или начала дополнительного сеанса.

При первом указании или использовании объекта **Workspace** автоматически создается рабочая область по умолчанию DBEngine.Workspaces(0). Параметры свойств **Name** и **UserName** рабочей области по умолчанию: "\#Default Workspace\#" и "Admin," соответственно. Если включена система безопасности, значение свойства **UserName** соответствует имени пользователя, вошедшего в систему.

Вы можете создавать новые **объекты Рабочей области** с помощью **[метода CreateWorkspace.](dbengine-createworkspace-method-dao.md)** После создания объекта **Workspace** его необходимо добавить в коллекцию **Workspaces**, если нужно ссылаться на него из коллекции **Workspaces**. Однако можно использовать только что созданный **объект Workspace,** не привнося его в коллекцию **Workspaces.**

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

