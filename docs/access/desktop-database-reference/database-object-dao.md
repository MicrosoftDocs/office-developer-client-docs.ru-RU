---
title: Объект Database (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c23772c54f2f980b8d10d4afc352687935840752
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294842"
---
# <a name="database-object-dao"></a>Объект Database (DAO)

**Область применения**: Access 2013, Office 2013

Объект **Database** представляет открытую базу данных.

## <a name="remarks"></a>Примечания

Объект **Database**, его методы и свойства используются для операций с открытой базы данных. В базе данных любого типа вы можете:

  - Использовать метод **Execute**, чтобы выполнить запрос на изменение.

  - Задать свойство **Connect**, чтобы установить соединение с источником данных ODBC.

  - Задать свойство **QueryTimeout**, чтобы ограничить продолжительность ожидания выполнения запроса в источнике данных ODBC.

  - Использовать свойство **RecordsAffected**, чтобы определить количество измененных записей в результате запроса на изменение.

  - Использовать метод **OpenRecordset**, чтобы выполнить запрос на выборку и создать объект **Recordset**.

  - Использовать свойство **Version**, чтобы определить версию ядра СУБД, создавшую базу данных.

С помощью базы данных ядра СУБД Microsoft Access можно также использовать другие методы, свойства и коллекции для работы с объектом **Database**, а также создавать, изменять или получать сведения о его таблицах, запросах и отношениях. Например, вы можете:

  - Использовать методы **CreateTableDef** и **CreateRelation**, чтобы создавать таблицы и отношения соответственно.

  - Использовать метод **CreateProperty**, чтобы определить новые свойства **Database**.

  - Использовать метод **CreateQueryDef**, чтобы создать постоянное или временное определение запроса.

  - Использовать методы **MakeReplica**, **Synchronize** и **PopulatePartial**, чтобы создать и синхронизировать полные или частичные копии базы данных.

  - Задать свойство **CollatingOrder**, чтобы установить порядок сортировки по алфавиту для символьных полей на разных языках.

Метод **CreateDatabase** используется для создания постоянного объекта **Database**, автоматически добавляемого в коллекцию **Databases**, что обеспечивает его сохранение на диске.

Не нужно указывать объект **DBEngine** при использовании метода **OpenDatabase**.

Открытие базы данных со связанными таблицами не создает автоматически ссылки на указанные внешние файлы. Необходимо либо создать ссылку на объект **TableDef** или объекты **Field** таблицы, либо открыть объект **Recordset**. Если не удается создать ссылки на эти таблицы, возникает перехватываемая ошибка. Может также требоваться разрешение на доступ к базе данных или другой пользователь мог открыть базу данных в монопольном режиме. В этих случаях возникают перехватываемые ошибки.

Когда выполнена процедура, объявляющая объект **Database**, локальные объекты **Database** закрываются вместе с любыми открытыми объектами **Recordset**. Любые ожидающие обновления пропадают, и выполняется откат всех ожидающих транзакций, но перехватываемая ошибка не возникает. Следует явным образом завершить все ожидающие транзакции или изменения и закрыть объекты **Recordset** и **Database** перед процедурами выхода, локально объявляющими эти переменные объектов.

Если вы используете один из методов транзакции (**BeginTrans**, **CommitTrans** или **Rollback**) для объекта **Workspace**, эти транзакции применяются ко всем базам данных, открытым в объекте **Workspace**, из которого был открыт объект **Database**. Если нужно использовать независимые транзакции, необходимо сначала открыть дополнительный объект **Workspace**, а затем открыть другой объект **Database** в этом объекте **Workspace**.


> [!NOTE]
> Вы можете открывать один источник данных или базу данных несколько раз, создавая дублирующие имена в коллекции **Databases**. Вы должны назначить объекты **Database** для переменных объекта и ссылаться на них по имени переменной.



## <a name="example"></a>Пример

В этом примере создается новый объект **Database** и открывается существующий объект **Database** в объекте **Workspace**, используемом по умолчанию. Затем выполняется перечисление коллекции **Database** и коллекции **Properties** каждого объекта **Database**.

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
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

В этом примере используется метод **CreateDatabase** для создания нового зашифрованного объекта **Database**.

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
