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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293779"
---
# <a name="document-object-dao"></a>Объект Document (DAO)

**Область применения**: Access 2013, Office 2013

Объект **Document** включает сведения об одном экземпляре объекта. Объект может быть базой данных, сохраненной таблицей, запросом или отношением (только базы данных ядра СУБД Microsoft Access).

## <a name="remarks"></a>Замечания

Каждый объект **Container** содержит коллекцию **Documents** , содержащую объекты **Document** , которые описывают экземпляры встроенных объектов типа, указанного в контейнере ****. В следующей таблице перечислены типы объектов, описанных в каждом **документе** , имя его объекта **Container** и тип информационного **документа** .

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
<td><p>Database</p></td>
<td><p>Базы данных</p></td>
<td><p>Сохраненная база данных</p></td>
</tr>
<tr class="even">
<td><p>Таблица или запрос</p></td>
<td><p>Tables</p></td>
<td><p>Сохраненная таблица или запрос</p></td>
</tr>
<tr class="odd">
<td><p>Отношение</p></td>
<td><p>Relations</p></td>
<td><p>Сохраненная связь</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Не путайте объекты **контейнера** , перечисленные в предыдущей таблице, с коллекциями с одинаковыми именами. Объект **контейнера** баз данных относится ко всем сохраненным объектам базы данных, но семейство **баз данных** относится только к объектам базы данных, открытым в определенной рабочей области.

Объект **Document** позволяет:

- Используйте свойство **Name** , чтобы возвратить имя, которое пользователь или ядро СУБД Microsoft Access предоставило объекту при его создании.

- С помощью свойства **Container** можно возвратить имя объекта **контейнера** , содержащего объект **Document** .

- Используйте свойство **owner** , чтобы задать или вернуть владельца объекта. Чтобы задать свойство **owner** , необходимо иметь разрешение на запись для объекта **Document** , а свойству необходимо присвоить имя существующего объекта **пользователя** или **группы** .

- Используйте свойства **username** и **Permissions** , чтобы задать или вернуть разрешения на доступ к объекту для пользователя или группы. Чтобы задать эти свойства, необходимо иметь разрешение на запись для объекта **Document** , а свойству **username** необходимо присвоить имя существующего объекта **пользователя** или **группы** .

- Используйте свойства **DateCreated** и **ластупдатед** , чтобы получить дату и время создания и последнего изменения объекта **документа** .

Так как объект **Document** соответствует существующему объекту, вы не можете создавать новые объекты **документа** или удалять существующие. Чтобы сослаться на объект **Document** в коллекции по его порядковому номеру или по его свойству **Name** , используйте любую из следующих синтаксических форм:

- **Документы** нуль

- **Документы** ("*имя*")

- ****\!\[*Имя* документа\]

## <a name="example"></a>Пример

В этом примере выполняется перечисление коллекции **Documents** контейнера Tables, после чего выполняется перечисление коллекции **свойств** первого объекта **Document** в коллекции.

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

В этом примере используются свойства **owner** и **системдб** для отображения владельцев множества объектов **Document** .

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

