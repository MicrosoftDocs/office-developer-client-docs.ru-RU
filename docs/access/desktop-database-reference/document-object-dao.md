---
title: Объект document (DAO)
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
# <a name="document-object-dao"></a>Объект document (DAO)

**Область применения**: Access 2013, Office 2013

Объект **Document** содержит сведения об одном экземпляре объекта. Объектом может быть база данных, сохраненная таблица, запрос или связь (только базы данных базы данных Microsoft Access).

## <a name="remarks"></a>Примечания

Каждый **объект Контейнер** имеет коллекцию **Документов,** содержащую объекты **Document,** описывая экземпляры встроенных объектов типа, указанного **контейнером.** В следующей таблице перечислены  тип объекта, описываемого каждым документом, имя его объекта **Контейнер** и тип сведений, **содержащийся в документе.**

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
<td><p>Сохраненные отношения</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Не путайте **объекты Container,** перечисленные в предыдущей таблице, с коллекциями с одним и тем же именем. Объект Контейнера **баз** данных относится к всем сохраненным объектам базы данных, но коллекция **Баз** данных относится только к объектам баз данных, которые открыты в определенном рабочем пространстве.

С помощью **объекта Document** можно:

- Используйте свойство **Name,** чтобы вернуть имя, которое пользователь или двигатель базы данных Microsoft Access дал объекту при его создания.

- Используйте свойство **Контейнер,** чтобы вернуть имя объекта **Контейнер,** содержаного **объект Document.**

- Используйте свойство **Owner,** чтобы установить или вернуть владельца объекта. Чтобы установить свойство **Owner,** необходимо иметь разрешение на написание объекта **Document,** а также установить его имя существующего объекта **User** или **Group.**

- Используйте свойства **UserName** или **Permissions** для набора или возврата разрешений доступа пользователя или группы для объекта. Чтобы установить эти свойства, необходимо иметь разрешение на написание объекта **Document,** а свойство **UserName** должно быть назначено имени существующего объекта **User** или **Group.**

- Используйте **свойства DateCreated** и **LastUpdated,** чтобы вернуть  дату и время создания и последнего изменения объекта Document.

Так как **объект Document** соответствует существующему объекту, нельзя создавать новые объекты **Document** или удалять существующие. Чтобы сослаться на объект **Document** в коллекции по его порядковому номеру или по параметру свойства **Name,** используйте любую из следующих форм синтаксиса:

- **Документы**(0)

- **Документы***("имя")*

-  \! Документы \[ *имя*\]

## <a name="example"></a>Пример

В этом примере содержится коллекция Документов контейнера Tables, а затем — коллекция **свойств** первого объекта **Document** в коллекции. 

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

В этом **примере свойства Owner** и **SystemDB** используются для демонстрации владельцев различных объектов **Document.**

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

