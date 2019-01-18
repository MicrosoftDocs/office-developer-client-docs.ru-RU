---
title: Объект Document (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f82ace31a991a6700417d4c0d66bf775fcb7b26
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710799"
---
# <a name="document-object-dao"></a>Объект Document (DAO)

**Применимо к**: Access 2013, Office 2013

Объект **Document** содержит сведения о один экземпляр объекта. Объект может быть базы данных, сохраненные в таблице, запрос или связь (Microsoft Access базами данных, ядро только).

## <a name="remarks"></a>Замечания

Каждый объект- **контейнер** имеет **документы** коллекцию, содержащую объекты **документов** , которые описывают экземпляры встроенные объекты типа, указанного в качестве **контейнера**. В следующей таблице перечислены тип объекта, который описывает каждого **документа** , имя его объекта- **контейнера** , а какая информация **документ** содержит.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Document</p></th>
<th><p>Container</p></th>
<th><p>Содержит сведения о</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>База данных</p></td>
<td><p>Databases</p></td>
<td><p>Сохраненные базы данных</p></td>
</tr>
<tr class="even">
<td><p>Таблица или запрос</p></td>
<td><p>таблицы;</p></td>
<td><p>Сохранить таблицы или запроса</p></td>
</tr>
<tr class="odd">
<td><p>Связь</p></td>
<td><p>Relations</p></td>
<td><p>Сохраненные отношения</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Не следует путать объекты **контейнеров** , перечисленных в предыдущей таблице с семействами с таким же именем. Баз данных **контейнер** объекта ссылается на все объекты сохраненного базы данных, но семейства **баз данных** относится только к объекты базы данных, которые открыты в конкретной рабочей области.

Объект **Document** можно выполнить следующие действия.

- Используйте свойство **Name** возвращает имя, которое пользователь или ядро базы данных Microsoft Access присваивает объекту при его создании.

- Свойство **контейнера** возвращает имя объекта **контейнера** , который содержит объект **Document** .

- Используйте свойство **владельца** или возвращает владельца объекта. Для установки свойства **Owner** , необходимо иметь разрешения на запись для объекта **Document** , а свойству необходимо присвоить имя существующего объекта **пользователя** или **группы** .

- Использование свойств **имя пользователя** или **разрешения** или возвращает разрешения на доступ к пользователю или группе для объекта. Чтобы задать эти свойства, необходимо иметь разрешения на запись для объекта **Document** , а свойство **UserName** необходимо присвоить имя существующего объекта **пользователя** или **группы** .

- Использование свойства **DateCreated** и **LastUpdated** возвращает дату и время создания и последнего изменения объекта **Document** .

Поскольку объект **Document** соответствует существующий объект, не могут создавать новые объекты **документа** или удалять существующие. Для ссылки на объект **Document** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:

- **Документы** (0)

- **Документы** («*имя*»)

- **Документы**\!\[*имя*\]

## <a name="example"></a>Пример

В этом примере создается перечисление коллекции **документов** контейнер таблиц и затем создается перечисление коллекции **свойств** первый объект **документа** в коллекции.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<br/>

В этом примере используются свойства **владельца** и **SystemDB** для отображения владельцев различных объектов **документа** .

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

