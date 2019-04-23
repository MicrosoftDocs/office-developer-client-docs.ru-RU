---
title: Савеоптионсенум (Справочник по базам данных Access на компьютере)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314744"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum

**Область применения**: Access 2013, Office 2013

Указывает, следует ли создать или перезаписать файл при сохранении из объекта [Stream](stream-object-ado.md) . Значения можно сочетать с помощью оператора AND.

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
<td><p><strong>Адсавекреатенотексист</strong></p></td>
<td><p>1,1</p></td>
<td><p>Значение, используемое по умолчанию. Создает новый файл, если файл, указанный с помощью параметра <em>filename</em> , еще не существует.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адсавекреатеоверврите</strong></p></td>
<td><p>2</p></td>
<td><p>Перезаписывает файл данными из текущего открытого объекта <strong>Stream</strong> , если файл, указанный с помощью параметра <em>filename</em> , уже существует.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

