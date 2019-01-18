---
title: Свойство FetchOptions (RDS)
TOCTitle: FetchOptions property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd2ecf0d7d3df6d1caffd906cf318916a2a8882
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703743"
---
# <a name="fetchoptions-property-rds"></a>Свойство FetchOptions (RDS)


**Применимо к**: Access 2013, Office 2013

Указывает тип асинхронной выборки.

## <a name="setting-and-return-values"></a>Задание и возвращаемые значения

Задает или возвращает одно из следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcFetchUpFront</strong></p></td>
<td><p>Все записи из <a href="recordset-object-ado.md">набора записей</a> будут выбраны до возврата управления к приложению. Полный <strong>набор записей</strong> извлекается перед приложение может выполнять любые действия с ним.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcFetchBackground</strong></p></td>
<td><p>Элемент управления может вернуть приложению сразу после первого пакета записей будут выбраны. Последующие чтение <strong>записей</strong> , что будет отложено попытки доступа к записи, не извлечь в первого пакета, пока искомому запись фактически выбраны, в какой момент элемент управления возвращает приложению.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcFetchAsync</strong></p></td>
<td><p>Значение, используемое по умолчанию. Управление немедленно возвращается приложению во время записи получены в фоновом режиме. Если приложение пытается считать запись, которая еще не выбраны, наиболее близкого к искомому запись запись будет считывать и элемент управления будет возвращать немедленно, указывающего на то, что достигнут конец текущего <strong>набора записей</strong> . К примеру вызов <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> будут перемещаться положения текущей записи последней записи фактически извлечь несмотря на то, что будет предоставляться несколько записей для заполнения <strong>записей</strong>.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Каждый исполняемый файл со стороны клиента, который использует эти константы необходимо предоставить объявления для них. Можно вырежьте и вставьте объявлений констант из файла Adcvbs.inc, находящийся в папке C:\Program Files\Common Files\System\MSADC.



## <a name="remarks"></a>Замечания

В веб-приложении обычно требуется использовать **adcFetchAsync** (значение по умолчанию), так как он обеспечивает более высокую производительность. В скомпилированном клиентское приложение, которое обычно требуется использовать **adcFetchBackground**.

