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

Коллекция **Workspace** содержит все активные, нескрытые объекты **рабочей области** объекта **DBEngine** . (Скрытые объекты **рабочей области** не добавляются в коллекцию и ссылаются на переменную, которой они назначены.)

## <a name="remarks"></a>Замечания

Используйте объект **Workspace** для управления текущим сеансом или для запуска дополнительного сеанса.

Когда вы впервые указываете на объект **Workspace** или используете его, вы автоматически создаете рабочую область по умолчанию DBEngine. workspaces (0). Параметры свойств **Name** и **username** для рабочей области по умолчанию: "\#Рабочая область\#по умолчанию" и "Администратор" соответственно. Если параметр "безопасность" включен, свойство **username** является именем пользователя, выполнившего вход в систему.

Вы можете создавать новые объекты **Workspace** с помощью метода **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** . После создания нового объекта **Workspace** его необходимо добавить в коллекцию workspaces, если **** необходимо сослаться на него из коллекции **workspaces** . Тем не менее, вы можете использовать только что созданный объект **Workspace** , не добавив его **** в коллекцию workspaces.

Чтобы сослаться на объект **Workspace** в коллекции по его порядковому номеру или по значению свойства **Name** , используйте любую из следующих синтаксических форм:

**DBEngine**. **Рабочие области** нуль

**DBEngine**. **Рабочие области** ("имя")

**DBEngine**. **Рабочие области** \! \[\]


> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.



## <a name="example"></a>Пример

В этом примере создается новый объект рабочей области Microsoft Access, который добавляется в **** коллекцию workspaces. Затем перечисляет коллекции workspaces **** и **свойства** объекта **Workspace** .

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

В этом примере используется метод **CreateWorkspace** для создания рабочей области Microsoft Access. Затем выводится список свойств севоркспаце.

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

