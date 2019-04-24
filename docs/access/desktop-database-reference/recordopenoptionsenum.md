---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300688"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**Область применения**: Access 2013, Office 2013

Задает параметры открытия [записи](record-object-ado.md). Эти значения можно объединять с помощью или.

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
<td><p><strong>Адделайфетчфиелдс</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Указывает поставщику, что поля, связанные с <strong>записью</strong> , не должны извлекаться изначально, но их можно получить при первой попытке доступа к полю. Поведение по умолчанию, определяемое отсутствием этого флага, — получение всех полей объекта <strong>Record</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>Адделайфетчстреам</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает поставщику, что по умолчанию не требуется извлекать поток, связанный с <strong>записью</strong> . Поведение по умолчанию, определяемое отсутствием этого флага, заключается в получении потока по умолчанию, связанного с объектом <strong>Record</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адопенасинк</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что объект <strong>Record</strong> открыт в асинхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенексекутекомманд</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что строка источника содержит текст команды, которую необходимо выполнить. Это значение эквивалентно параметру <strong>адкмдтекст</strong> для объекта <strong>Recordset. Open</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>АдопенрекордунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что параметры не указаны.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенаутпут</strong></p></td>
<td><p>0x800000</p></td>
<td><p>Указывает, что если источник указывает на узел, содержащий исполняемый скрипт (например,. Страница ASP), тогда открытая <strong>запись</strong> будет содержать результаты выполненного скрипта. Это значение является допустимым только для записей, не являющихся коллекциями.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

