---
title: Метод Relation.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 564cbae4669a0405a0e33d0e9770bbaa8f6c9dfb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929484"
---
# <a name="relationcreatefield-method-dao"></a>Метод Relation.CreateField (DAO)


**Применимо к**: Access 2013, Office 2013

Создает новый объект **[поля](field-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . CreateField (***имя***, ***Тип***, ***размер***)

*выражение* Переменная, которая представляет собой объект- **связи** .

### <a name="parameters"></a>Параметры

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
<td><p>Имя</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строка, уникальным образом новый объект <strong>поля</strong> . Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см на допустимый имена <strong>полей</strong> .</p></td>
</tr>
<tr class="even">
<td><p>Тип</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Аргумент не поддерживается для этого объекта.</p></td>
</tr>
<tr class="odd">
<td><p>Size</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Аргумент не поддерживается для этого объекта.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Поле

## <a name="remarks"></a>Примечания

Чтобы создать новое поле, а также указать имя, тип данных и размер поля можно использовать метод **CreateField** . Если опустить одно или несколько частей необязательно при использовании **CreateField**, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию. После добавления нового объекта, можно изменить некоторые, но не для всех параметров его свойств. Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.

Аргументы типа и размера, применяются только к объектам **поля** в объекте **TableDef** . Пропускать следующие аргументы объекта **поля** связан с объектом **индекса** или **связи** .

Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .

Чтобы удалить объект **поля** из коллекции **полей** , используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов. Невозможно удалить объект **поля** из коллекции **полей** объектов **TableDef** после создания индекса, которая ссылается на поле.

