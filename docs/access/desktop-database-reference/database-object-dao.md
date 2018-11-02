---
title: Объект базы данных (DAO)
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
ms.openlocfilehash: 265edf6b5d426b87d718c66e9886b7a4877120de
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918851"
---
# <a name="database-object-dao"></a>Объект базы данных (DAO)

**Применимо к**: Access 2013, Office 2013

Объект **базы данных** представляет базу данных.

## <a name="remarks"></a>Примечания

Используйте объект **базы данных** и его методы и свойства для работы с открытой базы данных. В базе данных любого типа можно выполнить следующие действия.

  - Метод **Execute** для выполнения запроса.

  - Присвойте свойству **подключение** для установления подключения к источнику данных ODBC.

  - Присвойте свойству **QueryTimeout** , чтобы ограничить время ожидания для запроса к источнику данных ODBC.

  - Свойство **RecordsAffected** позволяет определить, сколько записей были изменены с запроса.

  - Используйте метод **OpenRecordset** для выполнения запроса и создания объекта **набора записей** .

  - Используйте свойство **Version** для определения, какая версия ядра базы данных создана база данных.

С базой данных ядра базы данных Microsoft Access можно также использовать другие методы, свойства и семейств сайтов для работы с объекта **базы данных** , а также создавать, изменять и получать сведения о его таблицы, запросы и связи. Например можно выполнить следующие действия.

  - Используйте методы **CreateTableDef** и **CreateRelation** для создания таблицы и связи, соответственно.

  - Используйте метод **CreateProperty** для определения нового свойства **базы данных** .

  - Используйте метод **CreateQueryDef** для создания определения постоянной или временной запроса.

  - Используйте методы **MakeReplica**, **Синхронизация**и **PopulatePartial** для создания и синхронизации реплик полное или частичное базы данных.

  - Присвойте свойству **CollatingOrder** для установления буквам и цифрам порядка сортировки для текстового поля на разных языках.

Используйте метод **CreateDatabase** Создание сохраняемого объекта **базы данных** , который автоматически добавляется к коллекции **баз данных** , таким образом, сохраните его на диске.

При использовании метода **OpenDatabase** указать объект **DBEngine** не требуется.

Открытие базы данных в связанных таблицах не устанавливать автоматически ссылки на указанные внешние файлы. Необходимо ссылок на объекты **TableDef** или **поля** в таблице или открывает объект **набора записей** . Если не удается установить ссылки на эти таблицы, то перехватываемые возникает ошибка. Может также потребоваться разрешение на доступ к базе данных или другой пользователь может быть база данных, открыть в монопольном режиме. В таких случаях перехватываемые ошибки.

При выполнении процедуры, которая объявляет объекта **базы данных** и все открытые объекты **набора записей** закрываются локальных объектов **базы данных** . Все ожидающие обновления не сохраняются все ожидающие транзакции будет выполнен откат, а перехватываемые ошибка не происходит. Необходимо явно завершения любой транзакций в состоянии ожидания или изменения и закройте **записей** и объекты **базы данных** перед выходом из процедуры, которые работают эти данными локально.

При использовании одного из методов транзакций (**BeginTrans**, **CommitTrans**или **отката**) на объекте **рабочей области для** этих операций применяются ко всем базам данных, открытых в **рабочей области** , из которой базе **базы данных** объект был открыт. Если вы хотите использовать независимых транзакций, необходимо сначала открыть дополнительные объекта **рабочей области** и откройте другой объект **базы данных** в **рабочей области для** объекта.


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
