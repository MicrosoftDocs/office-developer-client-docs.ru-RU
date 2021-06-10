---
title: Метод Index.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 712bccd2-c8a8-cc96-6f77-6d93d92320d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195775(v=office.15)
ms:contentKeyID: 48545578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1d7fcaa959c0fa5f8d42d9b00a920e987ca2f126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291840"
---
# <a name="indexcreateproperty-method-dao"></a>Метод Index.CreateProperty (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект Свойства, определенный **[пользователем](property-object-dao.md)** (только рабочие пространства Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . CreateProperty(Имя , ***Тип***, ***Значение***, ***DDL***)

*выражение* Переменная, представляюная объект **Index.**

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
<td><p><strong>Строка,</strong> уникально именуемая новым <strong>объектом Свойства.</strong> Сведения о <strong>допустимом</strong> имени свойства см. в свойстве <strong>Name.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа, определяемая типом данных нового объекта <strong>Property.</strong> Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Вариант,</strong> содержащий начальное значение свойства. Сведения <strong><a href="field-value-property-dao.md">см.</a></strong> в свойстве Value.</p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Подтип</strong> <strong>Variant (Boolean),</strong> который указывает, является ли <strong>свойство</strong> объектом DDL. Значение по умолчанию - <strong>false</strong>. Если DDL является <strong>true,</strong>пользователи не могут изменить или удалить этот объект <strong>Property,</strong> если у них нет <strong>разрешения dbSecWriteDef.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Свойство

## <a name="remarks"></a>Примечания

Вы можете создать объект **Свойства,** определенный пользователем, только в коллекции **[Свойств](properties-collection-dao.md)** сохраняемого объекта.

Если при использовании **CreateProperty** вы опустить одну или несколько необязательных частей, можно использовать соответствующее заявление о назначении, чтобы задать или сбросить соответствующее свойство, прежде чем примкнуть новый объект к коллекции. После приложения объекта можно изменить некоторые параметры свойств, но не все. Дополнительные сведения см. в разделы **Имя,** **Тип** и **Значение** свойств.

Если имя относится к объекту, который уже входит в коллекцию, при использовании метода **[Append](fields-append-method-dao.md)** возникает ошибка времени запуска.

Чтобы удалить определенный пользователем **объект Property** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции **Свойств.** Вы не можете удалить встроенные свойства.

> [!NOTE]
> Если упустить аргумент DDL, он по умолчанию будет ложным (не-DDL). Так как соответствующее свойство DDL не подвергается воздействию, необходимо удалить и повторно создать объект **Property,** который необходимо изменить с DDL на non-DDL.


