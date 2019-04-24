---
title: Метод index. CreateProperty (DAO)
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
# <a name="indexcreateproperty-method-dao"></a>Метод index. CreateProperty (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект определяемого пользователем **[Свойства](property-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . CreateProperty (***имя***, ***Тип***, ***значение***, ***DDL***)

*Expression (выражение* ) Переменная, представляющая объект **индекса** .

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
<td><p><strong>Variant</strong> (<strong>логический</strong> подтип), указывающий, является ли <strong>свойство</strong> объектом DDL. По умолчанию используется значение <strong>False</strong>. Если DDL имеет <strong>значение true</strong>, пользователи не могут изменить или удалить этот объект <strong>Property</strong> , если у них нет разрешения <strong>дбсеквритедеф</strong> .</p></td>
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
> Если опустить аргумент DDL, по умолчанию используется значение false (не для DDL). Так как соответствующее свойство DDL не предоставлено, необходимо удалить и повторно создать объект **Свойства** , который нужно изменить из DDL, на не-DDL.


