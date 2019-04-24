---
title: Свойство field2. Коллатингордер (DAO)
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
# <a name="field2collatingorder-property-dao"></a>Свойство field2. Коллатингордер (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, задающее последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочих областей Microsoft Access). Только для чтения, **Long**.

## <a name="syntax"></a>Синтаксис

*Expression* . Коллатингордер

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Замечания

Возвращаемое значение — это **длинное** значение или константа, которая может принимать одно из следующих значений.

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
<td><p><strong>Дбсортженерал</strong></p></td>
<td><p>Общие (английский, французский, немецкий, португальский, итальянский и современная Испанская)</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортарабик</strong></p></td>
<td><p>арабский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортчинесесимплифиед</strong></p></td>
<td><p>китайский (упрощенное письмо)</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортчинесетрадитионал</strong></p></td>
<td><p>китайский (традиционное письмо)</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортцириллик</strong></p></td>
<td><p>русский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсорткзеч</strong></p></td>
<td><p>чешский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортдутч</strong></p></td>
<td><p>голландский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортгрик</strong></p></td>
<td><p>греческий;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсорсебрев</strong></p></td>
<td><p>иврит;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсорсунгариан</strong></p></td>
<td><p>венгерский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортицеландик</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортжапанесе</strong></p></td>
<td><p>японский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсорткореан</strong></p></td>
<td><p>корейский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортнеутрал</strong></p></td>
<td><p>Нейтральный</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортнорвдан</strong></p></td>
<td><p>Норвежский или датский</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортпдксинтл</strong></p></td>
<td><p>Международная связь Paradox</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортпдкснор</strong></p></td>
<td><p>Paradox норвежский или датский</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортпдкссве</strong></p></td>
<td><p>Paradox шведский или Финский</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортполиш</strong></p></td>
<td><p>польский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортсловениан</strong></p></td>
<td><p>словенский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортспаниш</strong></p></td>
<td><p>испанский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсортсведфин</strong></p></td>
<td><p>Шведский или Финский</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортсаи</strong></p></td>
<td><p>тайский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбсорттуркиш</strong></p></td>
<td><p>турецкий;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбсортундефинед</strong></p></td>
<td><p>Неопределенное или неизвестное</p></td>
</tr>
</tbody>
</table>


Доступность свойства **коллатингордер** зависит от объекта, содержащего коллекцию Fields, как **** показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к элементу</p></th>
<th><p>Затем Коллатингордер</p></th>
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


Значение свойства **коллатингордер** соответствует аргументу языкового стандарта метода **CreateDatabase** при создании базы данных или методе **CompactDatabase** при последнем сжатии базы данных.

Параметры свойств **коллатингордер** и **Attributes** объекта **field2** в коллекции Fields **** объекта **index** вместе определяют последовательность и направление порядка сортировки в индексе. Однако вы не можете задать порядок сортировки для отдельного индекса — его можно задать только для всей таблицы.

