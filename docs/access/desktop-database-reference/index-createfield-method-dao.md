---
title: Метод index. CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291833"
---
# <a name="indexcreatefield-method-dao"></a>Метод index. CreateField (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[field](field-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . CreateField (***имя***, ***тип***, ***Размер***)

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
<td><p>Строка, которая уникально задает имя нового объекта <strong>field</strong> . Сведения о допустимых именах <strong>полей</strong> приведены в свойстве <strong><a href="connection-name-property-dao.md">Name</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Аргумент не поддерживается для этого объекта.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Аргумент не поддерживается для этого объекта.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Field

## <a name="remarks"></a>Замечания

С помощью метода **CreateField** можно создать новое поле, а также указать имя, тип данных и размер поля. Если опустить одну или несколько дополнительных частей при использовании **CreateField**, можно использовать соответствующий оператор присвоения для установки или сброса соответствующего свойства перед добавлением нового объекта в коллекцию. После добавления нового объекта можно изменить не все параметры его свойств. См. разделы для отдельных свойств для получения дополнительных данных.

Аргументы Type и size применяются только к объектам **field** в объекте **tabledef** . Эти аргументы игнорируются, если объект **поля** связан с объектом **index** или **relation** .

Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[append](fields-append-method-dao.md)** возникает ошибка во время выполнения.

Чтобы удалить объект **field** из коллекции **Fields** , используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции. После создания индекса, ссылающегося на поле, невозможно удалить объект **field** из коллекции **Fields** объекта **tabledef** .

