---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300695"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**Область применения**: Access 2013, Office 2013

Указывает, следует ли открыть существующую **запись** или создать новую **запись** для метода [Open](open-method-ado-record.md) объекта [Record](record-object-ado.md) . Значения можно сочетать с помощью оператора AND.

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
<td><p><strong>Адкреатеколлектион</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Создает новую <strong>запись</strong> в узле, указанном с помощью параметра <em>Source</em> , вместо того, чтобы открывать существующую <strong>запись</strong>. Если источник указывает на существующий узел, возникнет ошибка во время выполнения, если <strong>адкреатеколлектион</strong> не объединен с <strong>адопенифексистс</strong> или <strong>адкреатеоверврите</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адкреатенонколлектион</strong></p></td>
<td><p>нуль</p></td>
<td><p>Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">адсимплерекорд</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адкреатеоверврите</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Изменяет флаги создания <strong>адкреатеколлектион</strong>, <strong>адкреатенонколлектион</strong>и <strong>адкреатеструктдок</strong>. Когда или используется с этим значением и одним из значений флагов создания, если URL-адрес источника указывает на существующий узел или <strong>запись</strong>, то существующая <strong>запись</strong> перезаписывается, а вместо нее создается новая. Это значение не может использоваться вместе с <strong>адопенифексистс</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адкреатеструктдок</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">адструктдок</a>, а не открывает существующую <strong>запись</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфаилифнотексистс</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Приводит к ошибке во время выполнения, если <em>источник</em> указывает на несуществующий узел.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенифексистс</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Изменяет флаги создания <strong>адкреатеколлектион</strong>, <strong>адкреатенонколлектион</strong>и <strong>адкреатеструктдок</strong>. Когда или используется с этим значением и одним из значений флагов создания, если URL-адрес источника указывает на существующий узел или объект <strong>Record</strong> , то поставщик должен открыть существующую <strong>запись</strong> вместо создания новой. Это значение не может использоваться вместе с <strong>адкреатеоверврите</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

