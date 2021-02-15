---
title: Свойство Field2.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02711fbbf39b058bb88e9568716169825ae4a923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292869"
---
# <a name="field2collatingorder-property-dao"></a>Свойство Field2.CollatingOrder (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочей области Microsoft Access). Только для чтения, **Long**.

## <a name="syntax"></a>Синтаксис

*выражение .* CollatingOrder

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Заметки

Возвращаемая величина — это **длинное** значение или константа, которые могут быть одним из следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Порядок сортировки</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbSortGeneral</strong></p></td>
<td><p>Общие (английский, французский, немецкий, португальский, итальянский и современный испанский)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortArabic</strong></p></td>
<td><p>Арабский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortChineseSimplified</strong></p></td>
<td><p>Китайский (упрощенное письмо)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortChineseTraditional</strong></p></td>
<td><p>Китайский (традиционное письмо)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortCyrillic</strong></p></td>
<td><p>Русский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortCzech</strong></p></td>
<td><p>Чешский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortDutch</strong></p></td>
<td><p>Голландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortGreek</strong></p></td>
<td><p>Греческий</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortHebrew</strong></p></td>
<td><p>Иврит</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortHung де</strong></p></td>
<td><p>Венгерский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortIcelandic</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortJapanese</strong></p></td>
<td><p>Японский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortKorean</strong></p></td>
<td><p>Корейский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortNeutral</strong></p></td>
<td><p>Нейтральный</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortNorw Демили</strong></p></td>
<td><p>Норвежский или датский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXIntl</strong></p></td>
<td><p>Paradox International</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPDXNor</strong></p></td>
<td><p>Норвежский или датский (норвежский)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXSwe</strong></p></td>
<td><p>Paradox Шведский или финский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSort Дефис</strong></p></td>
<td><p>Польский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSlovenian</strong></p></td>
<td><p>Словенский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortSpanish</strong></p></td>
<td><p>Испанский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSwedFin</strong></p></td>
<td><p>Шведский или финский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortThai</strong></p></td>
<td><p>Тайский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortTurkish</strong></p></td>
<td><p>Турецкий</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortUndefined</strong></p></td>
<td><p>Неопределенный или неизвестный</p></td>
</tr>
</tbody>
</table>


Доступность свойства **CollatingOrder** зависит от объекта, содержающего коллекцию **Fields,** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к</p></th>
<th><p>Затем CollatingOrder</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Index</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
</tbody>
</table>


Параметр **свойства CollatingOrder** соответствует аргументу locale метода **CreateDatabase** при создании базы данных или **методу CompactDatabase** при последней сжатии базы данных.

Параметры **свойства CollatingOrder** и **Attributes** объекта **Field2** в коллекции **Fields** объекта **Index** вместе определяют последовательность и направление порядка сортировки в индексе. Однако вы не можете настроить порядок совмества для отдельного индекса— вы можете настроить его только для всей таблицы.

