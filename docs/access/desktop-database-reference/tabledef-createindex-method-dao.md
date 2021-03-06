---
title: Метод TableDef.CreateIndex (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: baa82b659cc2260d4a003c644b2d03d6c897fd21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314373"
---
# <a name="tabledefcreateindex-method-dao"></a>Метод TableDef.CreateIndex (DAO)

**Область применения**: Access 2013, Office 2013 

Создает новый объект **[Index](index-object-dao.md)** (только рабочие пространства Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражения* . CreateIndex ***(Имя)***

*выражение*: переменная, представляющая объект **TableDef**.

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Строка,</strong> уникально именуемая новым объектом <strong>Index.</strong> Сведения о <strong>действительных</strong> именах Index см. в свойстве <strong>Name.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Index

## <a name="remarks"></a>Примечания

Вы можете использовать **метод CreateIndex** для создания нового объекта **Index** для объекта **TableDef.** Если при использовании **CreateIndex** не используется необязательная часть имени, можно использовать соответствующее заявление о назначении для настройки или сброса свойства **Name** перед тем, как примковать новый объект к коллекции. После придания объекта вы можете или не сможете установить его свойство **Name** в зависимости от типа объекта, который содержит коллекцию **Indexes.** Дополнительные **сведения см.** в разделе Свойство Name.

Если имя относится к объекту, который уже входит в коллекцию, при использовании метода **[Append](fields-append-method-dao.md)** возникает ошибка времени запуска.

Чтобы удалить **объект Index** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.

## <a name="example"></a>Пример

В этом примере метод **CreateIndex** создает два новых объекта **Index** и затем привносим их в коллекцию **Indexes** объекта **Employees TableDef.** Затем он включает коллекцию Indexes объекта **TableDef,**  коллекцию Поля новых объектов **Index** и коллекцию Свойств новых объектов **Index.** Для запуска этой процедуры требуется функция CreateIndexOutput.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
