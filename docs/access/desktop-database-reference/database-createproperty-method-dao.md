---
title: Метод Database. CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f966e041a6d2aff773f6c3849c0846ef362d1142
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294976"
---
# <a name="databasecreateproperty-method-dao"></a>Метод Database. CreateProperty (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект определяемого пользователем **[Свойства](property-object-dao.md)** (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*Expression* . CreateProperty (***имя***, ***Тип***, ***значение***, ***DDL***)

*выражение*: переменная, представляющая объект **Database**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Строка</strong> , которая уникально названа нового объекта <strong>Property</strong> . Сведения о допустимых именах <strong>свойств</strong> приведены в свойстве <strong>Name</strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа, определяющая тип данных нового объекта <strong>Property</strong> . В разделе свойство <strong><a href="field-type-property-dao.md">Type</a></strong> для допустимых типов данных.</p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Переменная Variant</strong> , содержащая начальное значение свойства. Для получения подробных сведений просмотрите свойство <strong><a href="field-value-property-dao.md">value</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>DLL</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>логический</strong> подтип), указывающий, является ли <strong>свойство</strong> объектом DDL. Значение по умолчанию — false. Если DDL имеет значение true, пользователи не могут изменить или удалить этот объект <strong>Property</strong> , если у них нет разрешения дбсеквритедеф.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Свойство

## <a name="remarks"></a>Замечания

Пользовательский объект **Свойства** можно создать только в коллекции **[свойств](properties-collection-dao.md)** сохраняемого объекта.

Если опустить одну или несколько дополнительных частей при использовании **CreateProperty**, можно использовать соответствующий оператор присвоения для установки или сброса соответствующего свойства перед добавлением нового объекта в коллекцию. После добавления объекта можно изменить не все параметры его свойств. Для получения дополнительных сведений ознакомьтесь с разделами свойства " **имя**", " **Тип**" и " **значение** ".

Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[append](fields-append-method-dao.md)** возникает ошибка во время выполнения.

Чтобы удалить объект определяемого пользователем **Свойства** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции **свойств** . Невозможно удалить встроенные свойства.

> [!NOTE]
> Если опустить аргумент DDL, по умолчанию используется значение false (не для DDL). Так как соответствующее свойство DDL не предоставлено, необходимо удалить и повторно создать объект **Свойства** , который нужно изменить с DDL на non-DDL.


## <a name="example"></a>Пример

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
             If prpLoop <> "" Then Debug.Print "  " & _ 
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
