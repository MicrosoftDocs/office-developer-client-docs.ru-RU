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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293198"
---
# <a name="fetchoptions-property-rds"></a>Свойство FetchOptions (RDS)


**Область применения**: Access 2013, Office 2013

Указывает тип асинхронного извлечения.

## <a name="setting-and-return-values"></a>Установка и возврат значений

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
<td><p>Все записи <a href="recordset-object-ado.md">recordset</a> извлекаются перед возвратом управления в приложение. Полный набор <strong>записей получается</strong> до того, как приложению будет разрешено что-либо делать с ним.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcFetchBackground</strong></p></td>
<td><p>Управление может возвращаться в приложение сразу после получения первого пакета записей. Последующее чтение <strong></strong> наборов записей, пытающаяся получить доступ к записи, не извлеченной в первом пакете, будет отложена до тех пор, пока не будет фактически извлечена искомая запись, после чего контроль времени возвращается в приложение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcFetchAsync</strong></p></td>
<td><p>Значение, используемое по умолчанию. При извлечении записей в фоновом режиме управление немедленно возвращается в приложение. Если приложение пытается прочитать еще не извлеченную запись, запись, ближе всего к искомой записи, будет прочитана, а управление будет возвращено немедленно, что указывает на то, что текущий конец <strong>recordset</strong> был достигнут. Например, вызов <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> переместит текущую позицию записи в последнюю фактически извлеченную запись, несмотря на то что другие записи продолжат заполнять <strong>набор записей.</strong></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Каждый исполняемый файл на стороне клиента, использующий эти константы, должен предоставлять для них объявления. Вы можете вырезать и ввести нужные объявления констант из файла Adcvbs.inc, расположенного в папке C:\Program Files\Common Files\System\MSADC.



## <a name="remarks"></a>Заметки

В веб-приложении обычно необходимо использовать **adcFetchAsync** (значение по умолчанию), так как оно обеспечивает лучшую производительность. В скомпилном клиентском приложении обычно необходимо использовать **adcFetchBackground.**

