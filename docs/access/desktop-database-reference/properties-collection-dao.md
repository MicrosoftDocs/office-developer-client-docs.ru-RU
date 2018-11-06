---
title: Коллекция Properties (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cd2198d0578c6ec42e4bf800d95e1d7afe22786
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998345"
---
# <a name="properties-collection-dao"></a>Коллекция Properties (DAO)

**Применимо к**: Access 2013, Office 2013

Коллекция **свойств** содержит все объекты **[Свойства](property-object-dao.md)** для указанного экземпляра объекта.

## <a name="remarks"></a>Примечания

Каждый объект DAO, за исключением **подключения** и объектов **ошибок** содержит коллекцию **свойств** , которая имеет определенных встроенных **свойств** объектов. Эти объекты **свойство** (которые часто просто называются свойства) однозначно Создание характеристик этого экземпляра объекта.

Кроме встроенных свойств можно также создать и добавить свои собственные пользовательские свойства. Чтобы добавить пользовательские свойства существующего экземпляра объекта, сначала определите его характеристики с помощью метода **CreateProperty** , а затем добавить его в коллекцию с помощью метода **Append** . Создание ссылок на объект пользовательские **Свойства** , который еще не была добавлена к коллекции **свойств** вызовет ошибку, как и добавление объект пользовательских **свойств** в коллекцию **свойств** , содержащую ** Свойство** объект с таким же именем.

Можно использовать метод **Delete** для удаления пользовательских свойств из коллекции **свойств** , но вы не можете удалить встроенных свойств.

> [!NOTE]
> Объект пользовательских **свойств** сопоставляется только с определенный экземпляр объекта. Свойство не определено для всех экземпляров объектов выбранного типа.

Для ссылки на объект встроенных **свойств** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:

- объект. **Свойства** (0)

- объект. **Свойства** («имя»)

- объект. **Свойства** \! \[имя\]

Для встроенных свойств можно также используйте следующий синтаксис:

- Object.Name

> [!NOTE]
> Пользовательские свойства необходимо использовать полный объект. **Свойства** синтаксис («имя»).

С помощью одной синтаксиса форм можно найти в свойство **Value** объекта **Property** . Контекст ссылки определяет, будет ли вы ссылаетесь на объект **свойств** , самого или свойство **Value** объекта **Property** .

## <a name="example"></a>Пример

В этом примере создается пользовательское свойство в текущей базе данных, задает его **Тип** и **значение** свойства и добавляет его в коллекцию **свойств** базы данных. Затем в примере перечисляются все свойства в базе данных.

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

В этом примере предпринимается попытка задать значение свойства пользовательских. Если свойство не существует, метод **CreateProperty** используется для создания и установите значение нового свойства. Процедура SetProperty является обязательным для выполнения этой процедуры.

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
