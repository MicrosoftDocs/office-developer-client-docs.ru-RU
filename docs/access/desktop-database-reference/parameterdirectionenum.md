---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fac07165416841691ee7bc3ca5dfcdc366861023
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287974"
---
# <a name="parameterdirectionenum"></a>ParameterDirectionEnum


**Область применения**: Access 2013, Office 2013

Указывает, представляет ли [параметр](parameter-object-ado.md) входной параметр, выходной параметр, входной и выходной параметры, а также возвращаемое значение из хранимой процедуры.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>адпараминпут</strong></p></td>
<td><p>1,1</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что параметр представляет входной параметр.</p></td>
</tr>
<tr class="even">
<td><p><strong>адпараминпутаутпут</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает, что параметр представляет оба входного и выходного параметра.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адпарамаутпут</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что параметр представляет выходной параметр.</p></td>
</tr>
<tr class="even">
<td><p><strong>адпарамретурнвалуе</strong></p></td>
<td><p>4 </p></td>
<td><p>Указывает, что параметр представляет возвращаемое значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адпарамункновн</strong></p></td>
<td><p>нуль</p></td>
<td><p>Указывает, что направление параметра неизвестно.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Адоенумс. Параметердиректион. INPUT</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Параметердиректион. процессы</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Параметердиректион. OUTPUT</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Параметердиректион. RETURNVALUE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Параметердиректион. UNKNOWN</p></td>
</tr>
</tbody>
</table>

