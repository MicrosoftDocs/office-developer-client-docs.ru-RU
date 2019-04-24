---
title: Свойство Field. ValidationRule (DAO)
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
# <a name="fieldvalidationrule-property-dao"></a>Свойство Field. ValidationRule (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое проверяет данные в поле по мере их изменения или добавления в таблицу (только для рабочих областей Microsoft Access). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*Expression* . ValidationRule

*Expression (выражение* ) Выражение, возвращающее объект **field** .

## <a name="remarks"></a>Замечания

Параметры или возвращаемые значения — это строка, описывающая сравнение в форме предложения WHERE SQL без зарезервированного слова WHERE. Для объекта, который еще не добавлен в коллекцию **[Fields](fields-collection-dao.md)** , это свойство доступно для чтения и записи.

Свойство **ValidationRule** определяет, содержит ли поле допустимые данные. Если данные не являются допустимыми, возникает перехватываемая ошибка времени выполнения. Возвращаемое сообщение об ошибке — это текст свойства **[ValidationText](field-validationtext-property-dao.md)** , если он указан, или текст выражения, указанного с помощью параметра **ValidationRule**.

Для объекта **[field](field-object-dao.md)** использование свойства **ValidationRule** зависит от объекта, содержащего коллекцию Fields, к которой **** прикрепляется объект **field** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, добавленный в</p></th>
<th><p>Использование</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
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


Проверка поддерживается только для баз данных, использующих ядро СУБД Microsoft Access.

Строковое выражение, заданное свойством **ValidationRule** объекта **field** , может ссылаться только на это **поле**. Выражение не может ссылаться на пользовательские функции, статистические функции SQL или запросы. Чтобы задать свойство **ValidationRule** объекта **поля** , если для его свойства **валидатеонсет** задано **значение true**, выражение должно успешно анализироваться (с именем поля в качестве подразумеваемОго операнда) и оцениваться как **true**. Если для свойства **валидатеонсет** задано **значение false**, то значение свойства **ValidationRule** игнорируется.


> [!NOTE]
> Если присвоить свойству строку, Объединенную со значением, не являющимся целым числом, а системные параметры указывают символ, отличный от U. S. Decimal, такой как запятая (например, стрруле = "Price &gt; " &amp; лнгприце и лнгприце = 125, 50), то ошибка будет возникать при код пытается проверить какие бы то ни было данные. Это вызвано тем, что во время сцепления число преобразуется в строку с использованием десятичного знака системы, а SQL ядра СУБД Microsoft Access принимает только десятичные знаки США.


