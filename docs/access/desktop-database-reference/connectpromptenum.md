---
title: ConnectPromptEnum (Справочник по для настольных баз данных Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e405b1eb3a1326d56a32c432fb212de417cf3469
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482914"
---
# <a name="connectpromptenum"></a>ConnectPromptEnum


**Применимо к**: Access 2013 | Office 2013

Указывает, следует ли отображать диалоговое окно запрашивать отсутствующие параметры при открытии подключения к источнику данных.

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
<td><p>1</p></td>
<td><p>Выдает запрос всегда.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptComplete</strong></p></td>
<td><p>2</p></td>
<td><p>Выдает запрос, если требуются дополнительные сведения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>3</p></td>
<td><p>Выдает запрос, если требуется Дополнительные сведения, но не разрешены необязательных параметров.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptNever</strong></p></td>
<td><p>4</p></td>
<td><p>Никогда не запросы.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
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

