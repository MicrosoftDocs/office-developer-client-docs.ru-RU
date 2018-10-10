---
title: Workspaces Collection (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37fd4ce04dbd35fccb2356b8088450d07af203d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480980"
---
# <a name="workspaces-collection-dao"></a>Workspaces Collection (DAO)


**Применимо к**: Access 2013 | Office 2013

**Рабочие области для** семейства содержит все активные, Показать объекты **рабочей области для** объекта **DBEngine** . (Скрытые **рабочей области** объекты не добавляется в конец коллекции и ссылается переменная, к которому они назначены.)

## <a name="remarks"></a>Замечания

Используйте объект **рабочей области** для управления текущего сеанса или чтобы начать сеанс обмена дополнительные.

При первом обращайтесь к или использовать объект **рабочей области** , автоматическое создание рабочей области по умолчанию DBEngine.Workspaces(0). Может принимать следующие значения свойства **Name** и **имя пользователя** рабочей области по умолчанию "\#рабочей области по умолчанию\#" и «Администратор», соответственно. Если этот параметр безопасности включен, значение свойства **UserName** — имя пользователя, вошедшего в систему.

Новые объекты **рабочей области** можно создать с помощью метода **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** . После создания объекта **рабочей области** , необходимо добавить его семейства сайтов **рабочих областей** при необходимости ссылаться на него из коллекции **рабочих областей** . Тем не менее, можно используйте только что созданный объект **рабочей области** без добавления его в коллекцию **рабочих областей** .

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

