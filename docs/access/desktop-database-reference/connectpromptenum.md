---
title: ConnectPromptEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295669"
---
# <a name="connectpromptenum"></a>ConnectPromptEnum

**Область применения**: Access 2013, Office 2013

Указывает, должно ли отображаться диалоговое окно с запросом отсутствующих параметров при открытии подключения к источнику данных.

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
<td><p><strong>adPromptAlways</strong></p></td>
<td><p>1 </p></td>
<td><p>Запросы всегда.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptComplete</strong></p></td>
<td><p>2 </p></td>
<td><p>Запрос, если требуются дополнительные сведения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>3 </p></td>
<td><p>Запросы, если требуются дополнительные сведения, но необязательные параметры не разрешены.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptNever</strong></p></td>
<td><p>4 </p></td>
<td><p>Никогда не выговоров.</p></td>
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
<td><p>AdoEnums.ConnectPrompt.ALWAYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.COMPLETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectPrompt.COMPLETEREQUIRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.NEVER</p></td>
</tr>
</tbody>
</table>

