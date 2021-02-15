---
title: Коллекция Properties (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 515d28f0d7d99359c36df79cf3b8769d8f71e06d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301283"
---
# <a name="properties-collection-dao"></a>Коллекция Properties (DAO)

**Область применения**: Access 2013, Office 2013

Коллекция **свойств** содержит все **[объекты Property](property-object-dao.md)** для определенного экземпляра объекта.

## <a name="remarks"></a>Заметки

Каждый объект DAO, кроме **объектов Connection** и **Error,** содержит коллекцию **свойств** с определенными встроенными **объектами Property.** Эти **объекты** Property (которые часто называются просто свойствами) уникальным образом характеризуют этот экземпляр объекта.

Помимо встроенных свойств можно также создавать и добавлять собственные пользовательские свойства. Чтобы добавить определяемую пользователем свойство в существующий экземпляр объекта, сначала определите его характеристики с помощью метода **CreateProperty,** а затем добавьте его в коллекцию с помощью метода **Append.** Ссылка на пользовательский объект **Property,** который еще не был придан коллекции **свойств,** приведет к ошибке, так же  как и к коллекции **свойств,** содержащей объект **Property** с тем же именем.

С помощью метода **Delete** можно удалить пользовательские свойства из коллекции **Properties,** но встроенные свойства удалить нельзя.

> [!NOTE]
> Пользовательский объект **Property** связан только с определенным экземпляром объекта. Свойство определяется не для всех экземпляров объектов выбранного типа.

Чтобы сослаться на встроенный объект **Property** в коллекции по его порядковому номеру или по его свойству **Name,** используйте любую из следующих синтаксис-форм:

- object. **Свойства**(0)

- object. **Свойства**("имя")

- object.  \! Свойства \[ name\]

Для встроенного свойства можно также использовать такой синтаксис:

- object.name

> [!NOTE]
> Для определяемого пользователем свойства необходимо использовать полный объект. **Синтаксис** свойств ("имя").

С помощью тех же форм синтаксиса можно также ссылаться на свойство **Value** объекта **Property.** Контекст ссылки определяет, ссылается ли вы на сам объект **Property** или свойство **Value** объекта **Property.**

## <a name="example"></a>Пример

В этом примере создается пользовательское свойство для текущей базы данных, заданы его свойства **Type** и **Value,** а затем оно добавлено в коллекцию **свойств** базы данных. Затем в примере нумеруется все свойства базы данных.

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

В этом примере попытается установить значение свойства, определенного пользователем. Если свойство не существует, оно использует метод **CreateProperty,** чтобы создать и установить значение нового свойства. Процедура SetProperty необходима для запуска этой процедуры.

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
