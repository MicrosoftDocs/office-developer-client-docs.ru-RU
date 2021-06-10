---
title: Блок данных ForEachRecord
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292330"
---
# <a name="foreachrecord-data-block"></a>Блок данных ForEachRecord

**Область применения**: Access 2013, Office 2013

Блок **данных ForEachRecord** повторяет набор заявлений для каждой записи в домене.

> [!NOTE]
> Блок **данных ForEachRecord** доступен только в макросах данных.

## <a name="setting"></a>Параметр

Действие **ForEachRecord имеет** следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>В</strong></p></td>
<td><p>Да</p></td>
<td><p>Строка, определяемая доменом записей для работы. Аргумент <em>In</em> может содержать имя таблицы, выбранный запрос или SQL.</p><p><strong>ПРИМЕЧАНИЕ.</strong>Указанный домен не может включать данные, хранимые в связанной таблице или источнике данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Где состояние</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строковая экспрессия, используемая для ограничения диапазона данных, на которых выполняется блок данных <strong>ForEachRecord.</strong> Например, критерии часто эквивалентны пункту WHERE в SQL, без слова WHERE. Если критерии не указаны, блок <strong>данных ForEachRecord</strong> работает на всем домене, указанном аргументом <em>In.</em> Любое поле, включенное в критерии, также должно быть полем <em>в In</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строка, которая предоставляет альтернативное имя для домена, указанного аргументом <em>In.</em> Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки. Если <em>псевдоним не</em> указан, в качестве псевдонима будет использоваться таблица или имя запроса.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Чтобы немедленно выйти из блока данных **ForEachRecord, используйте действие ExitForEachRecord.** **[](exitforeachrecord-macro-action.md)**

