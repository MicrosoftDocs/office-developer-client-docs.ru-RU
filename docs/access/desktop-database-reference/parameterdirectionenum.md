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

Указывает, представляет [](parameter-object-ado.md) ли параметр входной параметр, выходной параметр, входной и выходной параметры, или возвращаемого значения из хранимой процедуры.

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
<td><p><strong>adParamInput</strong></p></td>
<td><p>1 </p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что параметр представляет входной параметр.</p></td>
</tr>
<tr class="even">
<td><p><strong>adParamInputOutput</strong></p></td>
<td><p>3 </p></td>
<td><p>Указывает, что параметр представляет как входной, так и выходной параметр.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adParamOutput</strong></p></td>
<td><p>2 </p></td>
<td><p>Указывает, что параметр представляет выходной параметр.</p></td>
</tr>
<tr class="even">
<td><p><strong>adParamReturnValue</strong></p></td>
<td><p>4 </p></td>
<td><p>Указывает, что параметр представляет возвращаемую величину.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adParamUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>Указывает, что направление параметра неизвестно.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

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
<td><p>AdoEnums.ParameterDirection.INPUT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ParameterDirection.INPUTOUTPUT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.OUTPUT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ParameterDirection.RETURNVALUE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.UNKNOWN</p></td>
</tr>
</tbody>
</table>

