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

Объект **Document** включает сведения об одном экземпляре объекта. Объект может быть базой данных, сохраненной таблицей, запросом или отношением (только для баз данных я могу использовать яд баз данных Microsoft Access).

## <a name="remarks"></a>Заметки

Каждый **объект** Container имеет коллекцию **Documents,** содержащую объекты **Document,** которые описывают экземпляры встроенных объектов типа, указанного **контейнером.** В следующей таблице перечислены  тип объекта, описываемого в документе, имя его **объекта-контейнера** и тип сведений, которые содержит **документ.**

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
<td><p>Таблицы</p></td>
<td><p>Сохраненная таблица или запрос</p></td>
</tr>
<tr class="odd">
<td><p>Связь</p></td>
<td><p>Relations</p></td>
<td><p>Сохраненная связь</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Не путайте **объекты-контейнеры,** перечисленные в предыдущей таблице, с коллекциями с тем же именем. Объект **контейнера databases** ссылается на все сохраненные объекты базы данных, но коллекция **Databases** ссылается только на объекты баз данных, открытые в определенной рабочей области.

С помощью **объекта Document** вы можете:

- Используйте свойство **Name,** чтобы вернуть имя, которое пользователь или яд баз данных Microsoft Access предоставил объекту при его создания.

- Используйте свойство **Container,** чтобы вернуть имя объекта **Container,** который содержит **объект Document.**

- Используйте свойство **Owner,** чтобы установить или вернуть владельца объекта. Чтобы установить свойство **Owner,** необходимо иметь разрешение на написание для объекта **Document** и установить для свойства имя существующего объекта **User** или **Group.**

- Используйте свойства **UserName** или **Permissions,** чтобы установить или вернуть разрешения доступа пользователя или группы для объекта. Чтобы установить эти свойства, необходимо иметь разрешение на написание для объекта **Document,** а для свойства **UserName** необходимо установить имя существующего объекта **User** или **Group.**

- Используйте свойства **DateCreated** и **LastUpdated** для возврата даты и времени создания и последнего изменения объекта **Document.**

Так как **объект Document** соответствует существующему объекту, нельзя создавать новые объекты **Document** или удалять существующие. Чтобы сослаться **на объект Document** в коллекции по порядковому номеру или по его свойству **Name,** используйте любую из следующих синтаксис форм:

- **Документы**(0)

- **Документы**("*имя")*

-  \! Документы \[ *name*\]

## <a name="example"></a>Пример

В этом примере включается enumerates the **Documents** collection of the Tables container, а затем — коллекция **Properties** первого объекта **Document** в коллекции.

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

В этом примере **свойства Owner** и **SystemDB** используются для показа владельцев различных объектов **Document.**

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

