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
ms.openlocfilehash: b19cf0819353dbe4d6cdb017faf0e38b3bfb7757
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997009"
---
# <a name="tabledefcreatefield-method-dao"></a>Метод TableDef.CreateField (DAO)

**Применимо к:** Access 2013 | Office 2013

Создает новый объект **[поля](field-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . CreateField (_**имя**_, _**Тип**_, _**размер**_)

*выражение* Переменная, которая представляет собой объект- **TableDef** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строка, уникальным образом новый объект <strong>поля</strong> . Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см на допустимый имена <strong>полей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>Тип</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа, которая определяет тип данных на новый объект <strong>поля</strong> . В разделе свойства <strong><a href="field-type-property-dao.md">Type</a></strong> для типов данных.</p></td>
</tr>
<tr class="odd">
<td><p><em>Размер</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Целое число, которое указывает максимальный размер в байтах, объект <strong>поля</strong> , который содержит текст. В разделе <strong><a href="field-size-property-dao.md">свойства Size для значений допустимый размер</a></strong> . Этот аргумент игнорируется для полей числовые и половинной ширины.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Поле

## <a name="remarks"></a>Примечания

Чтобы создать новое поле, а также указать имя, тип данных и размер поля можно использовать метод **CreateField** . Если опустить одно или несколько частей необязательно при использовании **CreateField**, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию. После добавления нового объекта, можно изменить некоторые, но не для всех параметров его свойств. Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.

Тип и размер аргументов применяются только к объектам **поля** в объекте **TableDef** . Пропускать следующие аргументы объекта **поля** связан с объектом **индекса** или **связи** .

Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .

Чтобы удалить объект **поля** из коллекции **полей** , используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов. Невозможно удалить объект **поля** из коллекции **полей** объектов **TableDef** после создания индекса, которая ссылается на поле.

**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества. UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.

- [Добавление поля гиперссылки в существующую таблицу с DAO](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a>Пример

Следующий пример демонстрирует создание вычисляемого поля. Метод CreateField создает поле с именем **полное имя**. Выражение затем задано значение выражения, вычисляющий значение поля.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

