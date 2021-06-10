---
title: Свойство Field2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292652"
---
# <a name="field2validationrule-property-dao"></a>Свойство Field2.ValidationRule (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только в рабочей области Microsoft Access). Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражения* . ValidationRule

*выражение* Выражение, возвращаемая **объекту Field2.**

## <a name="remarks"></a>Примечания

Параметры или значения возврата — это строка, описываемая сравнение в виде оговорки SQL WHERE без зарезервированного слова WHERE. Для объекта, еще не примыкаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство является чтением и написанием.

Свойство **ValidationRule** определяет, содержит ли поле допустимые данные. Если данные не являются допустимыми, возникает ловкая ошибка времени запуска. Возвращенное сообщение об ошибке — это текст свойства **ValidationText,** если указано, или текст выражения, указанного **в ValidationRule.**

Для объекта **Field2** использование свойства **ValidationRule** зависит от объекта,  который содержит коллекцию Полей, к которой примыкает объект **Field2.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, приданный</p></th>
<th><p>Usage</p></th>
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


Проверка поддерживается только для баз данных, которые используют двигатель базы данных Microsoft Access.

Выражение строки, указанное **свойством ValidationRule** объекта **Field2,** может ссылаться только на **это Поле2.** Выражение не может ссылаться на определенные пользователем функции, SQL совокупные функции или запросы. Чтобы установить свойство **ValidationRule** объекта **Field2** при его параметре **ValidOnSet** **True,** выражение должно успешно разузнать (с именем поля в качестве подразумеваемого операнда) и оценить до **True**. Если параметр **свойства ValidateOnSet** является **false,** параметр **ValidationRule** игнорируется.


> [!NOTE]
> Если задайте свойство строке, сопутствуемой неинтегрированному значению, а параметры системы укажите не-США. десятичных символов, таких как запятая (например, strRule = &gt; "PRICE" &amp; lngPrice и lngPrice = 125,50), ошибка приведет, когда код пытается проверить любые данные. Это потому, что во время конкатепации номер будет преобразован в строку с помощью десятичных символов вашей системы по умолчанию, а двигатель базы данных Microsoft Access SQL принимает только десятичных символов США.


