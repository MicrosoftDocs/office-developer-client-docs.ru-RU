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

*Expression* . коллатингордер

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Примечания

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
<td><p><strong>дбсортженерал</strong></p></td>
<td><p>Общие (английский, французский, немецкий, португальский, итальянский и современная Испанская)</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортарабик</strong></p></td>
<td><p>Арабский</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортчинесесимплифиед</strong></p></td>
<td><p>Китайский (упрощенное письмо)</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортчинесетрадитионал</strong></p></td>
<td><p>Китайский (традиционное письмо)</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортцириллик</strong></p></td>
<td><p>Русский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсорткзеч</strong></p></td>
<td><p>Чешский</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортдутч</strong></p></td>
<td><p>Голландский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортгрик</strong></p></td>
<td><p>Греческий</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсорсебрев</strong></p></td>
<td><p>Иврит</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсорсунгариан</strong></p></td>
<td><p>Венгерский</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортицеландик</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортжапанесе</strong></p></td>
<td><p>Японский</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсорткореан</strong></p></td>
<td><p>Корейский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортнеутрал</strong></p></td>
<td><p>Нейтральный</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортнорвдан</strong></p></td>
<td><p>Норвежский или датский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортпдксинтл</strong></p></td>
<td><p>Международная связь Paradox</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортпдкснор</strong></p></td>
<td><p>Paradox норвежский или датский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортпдкссве</strong></p></td>
<td><p>Paradox шведский или Финский</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортполиш</strong></p></td>
<td><p>Польский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортсловениан</strong></p></td>
<td><p>Словенский</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортспаниш</strong></p></td>
<td><p>Испанский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсортсведфин</strong></p></td>
<td><p>Шведский или Финский</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортсаи</strong></p></td>
<td><p>Тайский</p></td>
</tr>
<tr class="even">
<td><p><strong>дбсорттуркиш</strong></p></td>
<td><p>Турецкий</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбсортундефинед</strong></p></td>
<td><p>Неопределенное или неизвестное</p></td>
</tr>
</tbody>
</table>


Значение свойства **коллатингордер** соответствует аргументу языкового стандарта метода **CreateDatabase** при создании базы данных или методе **CompactDatabase** при последнем сжатии базы данных.

Проверьте значение свойства **коллатингордер** объекта **базы данных** или **поля** , чтобы определить метод сравнения строк для базы данных или поля. Вы можете задать свойство **коллатингордер** нового, неприсоединенного объекта **field** , если необходимо, чтобы параметр объекта **field** отличался от того объекта **базы данных** , который содержит его.

