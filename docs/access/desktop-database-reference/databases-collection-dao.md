---
title: Databases Collection (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f5eb99d19efb14ae78f3623efaf6dd5b2e3d751
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878327"
---
# <a name="databases-collection-dao"></a>Databases Collection (DAO)

**Применимо к**: Access 2013, Office 2013

Коллекция **баз данных** содержит все открытые объекты **базы данных** открывается или созданы в **рабочей области для** объекта.

## <a name="remarks"></a>Замечания

При открытии существующего объекта **базы данных** или создайте новый из **рабочей области**, автоматически добавляется в коллекцию **баз данных** . При закрытии объекта **базы данных** с помощью метода **[закрытия](connection-close-method-dao.md)** , удалены из коллекции **баз данных** , но не удаляется с диска. Закройте все открытые объекты **набора записей** перед закрытием объекта **базы данных** .

В рабочей области Microsoft Access **свойства Name базы данных** — это строка, которая указывает путь к файлу базы данных.

Для ссылки на объект **базы данных** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:

- **Базы данных** (0)

- **Базы данных** («*имя*»)

- **Базы данных**\!\[*имя*\]

> [!NOTE]
> Можно открыть один и тот же источник данных или базы данных более одного раза, Создание повторяющихся имен в семействе **баз данных** . Следует назначать объектных переменных объектов **базы данных** и обращаться к ним с именем переменной.

## <a name="example"></a>Пример

В этом примере создается новый объект **базы данных** и открывает существующий объект **базы данных** в объекте **рабочей области** по умолчанию. Затем перечисляет набор **баз данных** и коллекции **свойств** каждого объекта **базы данных** .

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

В этом примере используется **CreateDatabase** для создания нового, зашифрованные объекта **базы данных** .

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
