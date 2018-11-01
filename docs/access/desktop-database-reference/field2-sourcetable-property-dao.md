---
title: Field2.SourceTable Property (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb0c7b57b8ad5c0a1c202197e14fdaefd9a1103f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881022"
---
# <a name="field2sourcetable-property-dao"></a>Field2.SourceTable Property (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта **поле2** . Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Таблица

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Для объекта **поле2** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , добавляется объект **поле2** , как показано в следующей таблице.

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
<td><p>Только для чтения</p></td>
</tr>
</tbody>
</table>


Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поле2** . Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.


> [!NOTE]
> <P>Свойство <STRONG>Таблица</STRONG> не возвращает имя удобной для восприятия таблицы при использовании объекта <STRONG>поле2</STRONG> в коллекции <STRONG>полей</STRONG> объекта <STRONG>набора записей</STRONG> в таблице тип.</P>


