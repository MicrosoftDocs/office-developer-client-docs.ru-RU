---
title: Инхериттипинум (Справочник по базам данных Access на компьютере)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291416"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает, как объекты наследуют разрешения, заданные с помощью [SetPermissions](setpermissions-method-adox.md).

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
<td><p><strong>Адинхеритбос</strong></p></td>
<td><p>4</p></td>
<td><p>Записи наследуют оба объекта и других контейнеров, содержащихся в первичном объекте.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адинхеритконтаинерс</strong></p></td>
<td><p>2</p></td>
<td><p>Другие контейнеры, которые находятся в основном объекте, наследуют эту запись.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адинхеритноне</strong></p></td>
<td><p>нуль</p></td>
<td><p>Значение, используемое по умолчанию. Наследование не выполняется.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адинхеритнопропагате</strong></p></td>
<td><p>SP4</p></td>
<td><p>Флаги <strong>адинхеритобжектс</strong> и <strong>адинхеритконтаинерс</strong> не распространяются на наследуемую запись.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адинхеритобжектс</strong></p></td>
<td><p>1,1</p></td>
<td><p>Объекты, не являющиеся контейнерами в контейнере, наследуют разрешения.</p></td>
</tr>
</tbody>
</table>

