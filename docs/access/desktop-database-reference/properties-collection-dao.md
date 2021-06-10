---
title: Коллекция свойств (DAO)
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
# <a name="properties-collection-dao"></a>Коллекция свойств (DAO)

**Область применения**: Access 2013, Office 2013

Коллекция **свойств** содержит все объекты **[Свойства](property-object-dao.md)** для определенного экземпляра объекта.

## <a name="remarks"></a>Примечания

Каждый объект DAO, кроме **объектов Подключения** и **Ошибок,** содержит коллекцию **свойств,** в которой есть определенные встроенные **объекты Свойства.** Эти **объекты** Свойства (которые часто называются просто свойствами) однозначно характеризуют этот экземпляр объекта.

Помимо встроенных свойств можно также создавать и добавлять собственные свойства, определенные пользователем. Чтобы добавить свойство, определенное пользователем, в существующий экземпляр объекта, сначала определите его характеристики методом **CreateProperty,** а затем добавьте его в коллекцию с помощью метода **Append.** Ссылка на объект Свойства,  определенный пользователем, который еще не был придан коллекции **свойств,** приведет к ошибке,  так же как и к объекту свойства, определенному пользователем, к коллекции **свойств,** содержащей объект **Property** с таким же именем.

Вы можете использовать метод **Delete** для удаления свойств, определенных пользователем, из коллекции **Свойств,** но вы не можете удалить встроенные свойства.

> [!NOTE]
> Объект Свойства, **определенный** пользователем, связан только с определенным экземпляром объекта. Свойство не определено для всех экземпляров объектов выбранного типа.

Чтобы сослаться на встроенный объект **Property** в коллекции по его порядковому номеру или по его параметру **Свойства Name,** используйте любую из следующих форм синтаксиса:

- объект. **Свойства**(0)

- объект. **Свойства**("имя")

- объект.  \! Свойства \[ имя\]

Для встроенного свойства можно также использовать этот синтаксис:

- object.name

> [!NOTE]
> Для свойства, определяемого пользователем, необходимо использовать полный объект. **Синтаксис Свойства**("имя").

С помощью тех же синтаксисных форм можно также ссылаться на свойство **Value** объекта **Property.** Контекст ссылки определяет, имеется ли в виду сам объект **Property** или свойство **Value** объекта **Property.**

## <a name="example"></a>Пример

В этом примере создается свойство, определенное пользователем для текущей базы данных, задает его свойства **Type** и **Value** и примыкает его к коллекции **свойств** базы данных. Затем в примере 100 000 000 000 000 000 000 000 000 000 00

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

В этом примере попытается задать значение свойства, определяемого пользователем. Если свойство не существует, он использует метод **CreateProperty** для создания и набора значения нового свойства. Для запуска этой процедуры требуется процедура SetProperty.

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
