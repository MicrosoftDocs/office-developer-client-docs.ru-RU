---
title: Свойство Field.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ef68db39b7dcad380eae16f789f4dd5b0eab75f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292946"
---
# <a name="fieldvalidationrule-property-dao"></a>Свойство Field.ValidationRule (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только для рабочей области Microsoft Access). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражение .* ValidationRule

*выражение* Выражение, которое возвращает объект **Field.**

## <a name="remarks"></a>Заметки

Параметры или возвращаемые значения — это строка, описываемая сравнение в виде предложения SQL WHERE без зарезервированного слова WHERE. Для объекта, еще не примежаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство доступно для чтения и записи.

Свойство **ValidationRule** определяет, содержит ли поле допустимые данные. Если данные не являются допустимыми, возникает захватимая ошибка времени запуска. Возвращенное сообщение об ошибке — это текст свойства **[ValidationText(если](field-validationtext-property-dao.md)** он указан) или текст выражения, указанного **в ValidationRule.**

Для объекта **[Field](field-object-dao.md)** использование свойства **ValidationRule** зависит от объекта, который содержит коллекцию **Fields,** к которой применится объект **Field.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, к</p></th>
<th><p>Использование</p></th>
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
<td><p><strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


Проверка поддерживается только для баз данных, которые используют ядер баз данных Microsoft Access.

Строка выражения, заданного **свойством ValidationRule** объекта **Field,** может ссылаться только на это **поле.** Выражение не может ссылаться на пользовательские функции, SQL агрегатные функции или запросы. Чтобы установить свойство **ValidationRule** объекта **Field,** если его свойство **ValidateOnSet** имеет свойство **True,** выражение должно успешно синтаксировать (с именем поля в качестве подразумеваемого операнда) и оцениваться как **True**. Если его **свойство ValidateOnSet** имеет свойство **False,** параметр **свойства ValidationRule** игнорируется.


> [!NOTE]
> Если для свойства задана строка, совмещенная с неиссякаемым значением, а системные параметры указывают не из США. десятичная символка, например запятая (например, strRule = &gt; "PRICE" &amp; lngPrice и lngPrice = 125,50), при попытке кода проверить любые данные будет выявить ошибку. Это необходимо, так как во время конкатенации номер преобразуется в строку с помощью десятичных знаков системы по умолчанию, а подсистема баз данных Microsoft Access SQL принимает только десятичных знаков в США.


