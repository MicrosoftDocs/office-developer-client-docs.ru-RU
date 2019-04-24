---
title: Коллекция баз данных (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbaa0fe7aaa50c8aec582e2f03cd2849268816b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294647"
---
# <a name="databases-collection-dao"></a>Коллекция баз данных (DAO)

**Область применения**: Access 2013, Office 2013

Коллекция **баз данных** содержит все открытые объекты **базы данных** , открытые или созданные в объекте **Workspace** .

## <a name="remarks"></a>Замечания

Когда вы открываете существующий объект **базы данных** или создаете новый в **рабочей области**, он автоматически добавляется в коллекцию **баз данных** . При закрытии объекта **базы данных** с помощью метода **[Close](connection-close-method-dao.md)** он удаляется из коллекции **баз данных** , но не удаляется с диска. Перед закрытием объекта **базы данных** следует закрыть все открытые объекты **Recordset** .

В рабочей области Microsoft Access значение свойства " **имя** " базы данных — это строка, указывающая путь к файлу базы данных.

Чтобы сослаться на объект **базы данных** в коллекции по порядковому номеру или по его свойству **Name** , используйте любую из следующих синтаксических форм:

- **Базы данных** нуль

- **Базы данных** ("*имя*")

- **Имя базы данных**\!\[**\]

> [!NOTE]
> Вы можете открыть один и тот же источник данных или базу данных несколько раз, создав повторяющиеся имена в коллекции **баз данных** . Необходимо назначить объекты **базы данных** переменным объектов и ссылаться на них по имени переменной.

## <a name="example"></a>Пример

В этом примере показано, как создать объект **базы данных** и открыть существующий объект **базы данных** в объекте **рабочей области** по умолчанию. Затем выполняется перечисление коллекции **баз данных** и коллекции **свойств** каждого объекта **Database** .

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

В этом примере используется **CreateDatabase** для создания нового зашифрованного объекта **базы данных** .

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
