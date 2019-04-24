---
title: Свойство Database. Коллатингордер (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21d775c0abac5d2afddd6b0930816c8d6d381ff0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295018"
---
# <a name="databasecollatingorder-property-dao"></a>Свойство Database. Коллатингордер (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, задающее последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочих областей Microsoft Access). Только для чтения, **Long**.

## <a name="syntax"></a>Синтаксис

*Expression* . Коллатингордер

*выражение*: переменная, представляющая объект **Database**.

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


Значение свойства **коллатингордер** соответствует аргументу языкового стандарта метода **CreateDatabase** при создании базы данных или методе **CompactDatabase** при последнем сжатии базы данных.

Проверьте значение свойства **коллатингордер** объекта **базы данных** или **поля** , чтобы определить метод сравнения строк для базы данных или поля. Вы можете задать свойство **коллатингордер** нового, неприсоединенного объекта **field** , если необходимо, чтобы параметр объекта **field** отличался от того объекта **базы данных** , который содержит его.

