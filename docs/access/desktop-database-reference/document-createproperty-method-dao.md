---
title: Document.CreateProperty Method (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 834fda60-1edf-38df-a9a5-d9d15e55e425
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196739(v=office.15)
ms:contentKeyID: 48546003
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052967
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4bcd98c41fe6961112758a284aadb3806754bb77
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863327"
---
# <a name="documentcreateproperty-method-dao"></a>Document.CreateProperty Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Создание пользовательских **[свойств](property-object-dao.md)** объекта (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . CreateProperty (***имя***, ***Тип***, ***значение***, ***DDL***)

*выражение* Переменная, которая представляет собой объект- **документов** .

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
<td><p><strong>Строка</strong> , уникальным образом новый объект <strong>свойство</strong> . Свойство <strong>Name</strong> для получения дополнительных сведений см на допустимый имена <strong>свойств</strong> .</p></td>
</tr>
<tr class="even">
<td><p>Тип</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа, которая определяет тип данных нового <strong>Свойства</strong> объекта. В разделе свойства <strong><a href="field-type-property-dao.md">Type</a></strong> для типов данных.</p></td>
</tr>
<tr class="odd">
<td><p>Значение</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> содержащий исходное значение свойства. Свойство <strong><a href="field-value-property-dao.md">Value</a></strong> для получения дополнительных сведений см.</p></td>
</tr>
<tr class="even">
<td><p>DDL</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>логическое</strong> подтип), которое указывает, является ли <strong>свойство</strong> объектом DDL. Значение по умолчанию — <strong>False</strong>. Если DDL имеет <strong>значение True</strong>, пользователи не могут изменить и удалить этот объект <strong>Свойства</strong> , если у них есть разрешение <strong>dbSecWriteDef</strong> .</p></td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Возвращаемое значение
=======
### <a name="return-value"></a>Возвращаемое значение
>>>>>>> образец

Свойство

## <a name="remarks"></a>Замечания

Объект пользовательских **свойств** можно создать только в коллекции **[свойств](properties-collection-dao.md)** объекта, который является постоянным.

Если при использовании **CreateProperty**опустить одно или несколько частей необязательно, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию. После добавления объекта, можно изменить некоторые, но не для всех параметров его свойств. Обратитесь к соответствующим разделам **имя**, **Тип**и **значение** свойства для получения дополнительных сведений.

Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .

Чтобы удалить объект пользовательских **свойств** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** на **Properties** collection. Не удается удалить встроенные свойства.


> [!NOTE]
> Если опустить аргумент DDL по умолчанию используется значение False (не являющиеся DDL). Так как не соответствующее свойство DDL предоставляется, необходимо удалить и повторно создать объект **свойств** , чтобы перейти с DDL не DDL.


