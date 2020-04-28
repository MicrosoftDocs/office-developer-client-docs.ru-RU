---
title: Ексекутеоптионенум (Справочник по базам данных Access на компьютере)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293247"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**Область применения**: Access 2013, Office 2013

Указывает, как поставщик должен выполнять команду.

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
<td><p><strong>адасинцексекуте</strong></p></td>
<td><p>0x10</p></td>
<td><p>Указывает, что команда должна выполняться асинхронно. Это значение не может сочетаться со <a href="commandtypeenum.md">CommandTypeEnum</a> значением коммандтипинум <strong>адкмдтабледирект</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>адасинкфетч</strong></p></td>
<td><p>0x20</p></td>
<td><p>Указывает, что оставшиеся строки после начального количества, указанного в свойстве <a href="cachesize-property-ado.md">CacheSize</a> , должны быть получены асинхронно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адасинкфетчнонблоккинг</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что главный поток никогда не блокируется при извлечении. Если запрашиваемая строка не была получена, текущая строка автоматически перемещается в конец файла.</p><p>Если вы откроете <a href="recordset-object-ado.md">набор записей</a> из <a href="stream-object-ado.md">потока</a> , содержащего сохраняемый <strong>набор записей</strong>, <strong>адасинкфетчнонблоккинг</strong> не будет оказывать никакого результата; операция будет синхронной и блокирующей. <strong>адасинчфетчнонблоккинг</strong> не оказывает никакого действия, если для открытия объекта <strong>Recordset</strong>используется параметр <a href="commandtypeenum.md">адкмдтабледирект</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>адексекутенорекордс</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что текст команды — это команда или хранимая процедура, не возвращающая строки (например, команда, которая вставляет только данные). Если извлекаются какие бы то ни было строки, они отбрасываются и не возвращаются. <strong>адексекутенорекордс</strong> можно передать только как необязательный параметр для метода <strong>или</strong> метода <strong>подключения</strong> <strong>EXECUTE</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>адексекутестреам</strong></p></td>
<td><p>0x400</p></td>
<td><p>Указывает, что результаты выполнения команды должны возвращаться в виде потока. <strong>адексекутестреам</strong> можно передавать в качестве необязательного параметра методу <strong>Command</strong> <strong>EXECUTE</strong> Command.</p></td>
</tr>
<tr class="even">
<td><p><strong>адексекутерекорд</strong></p></td>
<td><p><br />
</p></td>
<td><p>Указывает, что <strong>CommandText</strong> — это команда или хранимая процедура, возвращающая одну строку, которая должна возвращаться как объект <strong>Record</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>адоптионунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Указывает, что команда не задана.</p></td>
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
<td><p>Адоенумс. Ексекутеоптион. АСИНЦЕКСЕКУТЕ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Ексекутеоптион. АСИНКФЕТЧ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Ексекутеоптион. АСИНКФЕТЧНОНБЛОККИНГ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Ексекутеоптион. unrecords</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Ексекутеоптион. unspecifieded</p></td>
</tr>
</tbody>
</table>

