---
title: Field2.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b8ce99f7fbedc487f5c5bae98745f1d446c2da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867148"
---
# <a name="field2validationtext-property-dao"></a>Field2.ValidationText Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение объекта **поле2** не соответствует правило проверки, указанного идентификатором **условие на значение** свойства поля (Microsoft Access рабочие области только ). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Сообщение об ошибке

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение — это **строка** , которая определяет текст, который отображается, если пользователь пытается ввести недопустимое значение для поля. Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи.

Для объекта **поле2** использование свойства **сообщение об ошибке** зависит от объекта, который содержит коллекцию **[полей](fields-collection-dao.md)** , к которому добавляется объект **поле2** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, добавляемый в конец</p></th>
<th><p>Применение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Индекс</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><strong>Набор записей</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Связь</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>

