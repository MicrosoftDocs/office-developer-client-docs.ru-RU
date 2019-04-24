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

Коллекция **Properties** содержит все объекты **[Property](property-object-dao.md)** для определенного экземпляра объекта.

## <a name="remarks"></a>Замечания

Каждый объект DAO, за исключением объектов **Connection** и **Error** , содержит коллекцию **Properties** , у которой есть некоторые встроенные объекты **Property** . Эти объекты **свойств** (часто называемые свойствами) однозначно характеризуют экземпляр объекта.

В дополнение к встроенным свойствам можно также создавать и добавлять собственные пользовательские свойства. Чтобы добавить пользовательское свойство в существующий экземпляр объекта, сначала определите его характеристики с помощью метода **CreateProperty** , а затем добавьте его в коллекцию с помощью метода **append** . Обращение к объекту пользовательского **Свойства** , еще не добавленному в коллекцию **свойств** , приводит к ошибке, в результате чего объект пользовательского **Свойства** будет добавлен в коллекцию **свойств** , содержащую ** Объект Property** с тем же именем.

С помощью метода **Delete** можно удалять пользовательские свойства из коллекции **свойств** , но нельзя удалять встроенные свойства.

> [!NOTE]
> Объект определяемого пользователем **Свойства** связан только с определенным экземпляром объекта. Свойство не определено для всех экземпляров объектов выбранного типа.

Чтобы сослаться на встроенный объект **Property** в коллекции по его порядковому номеру или по его свойству **Name** , используйте любую из следующих синтаксических форм:

- объектам. **Свойства** нуль

- объектам. **Свойства** ("имя")

- объектам. **Свойства** \! \[\]

Для встроенного свойства также можно использовать следующий синтаксис:

- Object.Name

> [!NOTE]
> Для свойства, определяемого пользователем, необходимо использовать весь объект. **Свойства** ("имя") синтаксис.

Используя те же формы синтаксиса, вы также можете ссылаться на свойство **value** объекта **Property** . Контекст ссылки определяет, будет ли ссылка на сам объект **Property** или свойство **value** объекта **Property** .

## <a name="example"></a>Пример

В этом примере создается пользовательское свойство для текущей базы данных, задаются его свойства **Type** и **value** , а затем она добавляется в коллекцию **свойств** базы данных. Затем в примере перечисляются все свойства в базе данных.

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

В этом примере предпринимается попытка задать значение определяемого пользователем свойства. Если свойство не существует, оно использует метод **CreateProperty** , чтобы создать и задать значение нового свойства. Для выполнения этой процедуры требуется процедура SetProperty.

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
