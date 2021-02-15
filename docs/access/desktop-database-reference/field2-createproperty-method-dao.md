---
title: Метод Field2.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: bdbd6bec-216f-138e-78df-9c3221692aa4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822737(v=office.15)
ms:contentKeyID: 48547446
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf35138a4782e1f16d230ba120bf5482a9a8ce40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292848"
---
# <a name="field2createproperty-method-dao"></a>Метод Field2.CreateProperty (DAO)

**Область применения**: Access 2013, Office 2013

Создает объект Property, определенный **[пользователем](property-object-dao.md)** (только для рабочих пространств Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)

*expression* — переменная, представляющая объект **Field2**.

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
<td><p><strong>Строка,</strong> однозначно именовав новый <strong>объект Property.</strong> Сведения о <strong>допустимом</strong> имени свойства см. в свойстве <strong>Name.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа, которая определяет тип данных нового объекта <strong>Property.</strong> Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Вариант,</strong> содержащий начальное значение свойства. Подробные <strong><a href="field-value-property-dao.md">сведения см.</a></strong> в свойстве Value.</p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Variant <strong></strong> (<strong>Boolean</strong> subtype), который указывает, является ли <strong>свойство</strong> объектом DDL. Значение по умолчанию - <strong>false</strong>. Если DDL <strong>имеет</strong>true, пользователи не могут изменить или удалить этот объект <strong>Property,</strong> если у них нет разрешения <strong>dbSecWriteDef.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Свойство

## <a name="remarks"></a>Заметки

Пользовательский объект **Property** можно создать только в коллекции **[свойств](properties-collection-dao.md)** сохраняемого объекта.

Если при использовании **CreateProperty** опустить одну или несколько необязательных частей, можно использовать соответствующий отчет о назначении, чтобы установить или сбросить соответствующее свойство перед тем, как приместь новый объект в коллекцию. После того как вы примесь к объекту, вы можете изменить некоторые, но не все параметры его свойств. Дополнительные сведения **см.** в под темах свойств **Name,** Type и **Value.**

Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[Append](fields-append-method-dao.md)** возникает ошибка во время работы.

Чтобы удалить пользовательский объект **Property** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в **[коллекции Properties.](properties-collection-dao.md)** Встроенные свойства удалить нельзя.


> [!NOTE]
> Если опустить аргумент DDL, по умолчанию будет засвеяно значение False (не DDL). Так как соответствующее свойство DDL не выявилось, необходимо удалить и повторно создать объект **Property,** который нужно изменить с DDL на non-DDL.


