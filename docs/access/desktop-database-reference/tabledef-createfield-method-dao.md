---
title: Метод TableDef.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 713f2530369a824a6d7204655ded4333f7fe2765
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308444"
---
# <a name="tabledefcreatefield-method-dao"></a>Метод TableDef.CreateField (DAO)

**Область применения**: Access 2013 | Office 2013

Создает новый объект **[Field](field-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* .CreateField(_**Name**_, _**Type**_, _**Size**_)

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
<td><p>Строка, присваивающая уникальное имя новому объекту <strong>Field</strong>. См. свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения более подробных сведений о допустимых именах <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа, определяющая тип данных нового объекта <strong>Field</strong>. Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Целое число, указывающее максимальный размер в байтах объекта <strong>Field</strong>, содержащего текст. Допустимые значения размеров см. в свойстве <strong><a href="field-size-property-dao.md">Size</a></strong>. Этот аргумент игнорируется для числовых полей и полей фиксированного размера.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Поле

## <a name="remarks"></a>Примечания

Можно использовать метод **CreateField**, чтобы создать новое поле, а также указать имя, тип данных и размер поля. Если опустить одну или несколько необязательных частей при использовании метода **CreateField**, вы можете воспользоваться соответствующим оператором присваивания, чтобы задать или сбросить соответствующее свойство перед добавлением нового объекта в коллекцию. После добавления нового объекта вы можете изменять некоторые, но не все параметры его свойств. См. разделы для отдельных свойств для получения дополнительных данных.

Аргументы Type и Size применяются только для объектов **Field** в объекте **TableDef**. Эти аргументы игнорируются, если объект **Field** связан с объектом **Index** или **Relation**.

Если аргумент Name ссылается на объект, который уже являются элементом коллекции, возникает ошибка выполнения при использовании метода **[Append](fields-append-method-dao.md)**.

Чтобы удалить объект **Field** из коллекции **Fields**, используйте метод **[Delete](fields-delete-method-dao.md)** для коллекции. Вы не можете удалить объект **Field** из коллекции **Fields** объекта **TableDef** после создания индекса, ссылающегося на поле.

**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com). UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.

- [Добавление поля гиперссылки в существующую таблицу с помощью DAO](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a>Пример

В приведенном ниже примере показано, как создать вычисляемое поле. Метод CreateField создает поле с именем **FullName**. Затем для свойства Expression устанавливается выражение, вычисляющее значение поля.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

