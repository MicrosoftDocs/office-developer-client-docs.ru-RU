---
title: Курсорлокатионенум (Справочник по базам данных Access на компьютере)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295214"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Область применения**: Access 2013, Office 2013

Указывает расположение службы курсора.

<br/>

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
<td><p><strong>Адусеклиент</strong></p></td>
<td><p>4</p></td>
<td><p>Использует курсоры на стороне клиента, предоставляемые библиотекой локальных курсоров. Службы локальных курсоров часто поддерживают множество функций, которые могут быть недоступны в драйверах, поэтому использование этого параметра может привести к преимуществам в отношении функций, которые будут включены. Для обеспечения обратной совместимости также поддерживается <strong>адусеклиентбатч</strong> синонимов.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адусеноне</strong></p></td>
<td><p>1,1</p></td>
<td><p>Не использует службы курсоров. (Эта константа является устаревшей и отображается исключительно в целях обратной совместимости.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адусесервер</strong></p></td>
<td><p>2</p></td>
<td><p>Значение, используемое по умолчанию. Использует курсоры, предоставляемые поставщиком данных или драйверами. В некоторых случаях эти курсоры являются очень гибкими и позволяют изменять другие чувствительность к источнику данных. Однако некоторые функции <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">службы курсора Майкрософт для OLE DB</a> (например, несвязанные объекты <a href="recordset-object-ado.md">Recordset</a> ) не могут быть смоделированы с помощью серверных курсоров, и эти функции будут недоступны в этом параметре.</p></td>
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
<td><p>Адоенумс. CursorLocation. CLIENT</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. CursorLocation. NONE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. CursorLocation. SERVER</p></td>
</tr>
</tbody>
</table>

