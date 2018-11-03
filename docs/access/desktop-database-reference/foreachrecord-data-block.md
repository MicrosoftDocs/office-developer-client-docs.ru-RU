---
title: Блок данных ДляКаждойЗаписи
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09a09a80773adecf760ae4610df30bbd5f36f3d6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937528"
---
# <a name="foreachrecord-data-block"></a>Блок данных ДляКаждойЗаписи


**Применимо к**: Access 2013, Office 2013

Блок данных **ДляКаждойЗаписи** повторяет набор инструкций для каждой записи в домене.

> [!NOTE]
> Блок данных **ДляКаждойЗаписи** доступна только в макросов данных.

## <a name="setting"></a>Параметр

Действие **ДляКаждойЗаписи** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>В</strong></p></td>
<td><p>Да</p></td>
<td><p>Строка, идентифицирующая домена записей для работы с. Аргумент <em>в</em> может содержать имя таблицы, запроса или инструкции SQL.</p>

> [!NOTE]
> Указанный домен не может включать данные, хранящиеся в связанной таблице или источник данных ODBC.


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Условие отбора</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строковое выражение, используемое для ограничения диапазона данных, на котором блок данных <strong>ДляКаждойЗаписи</strong> выполняется. К примеру, критерии эквивалентен часто предложение WHERE в выражении SQL без слова ГДЕ. Если критерии опущен, блок данных <strong>ДляКаждойЗаписи</strong> действует на весь домен, указанный в аргументе <em>в</em> . Поля, который включен в условия также должны входить в <em>в</em>поле.</p></td>
</tr>
<tr class="odd">
<td><p><strong>псевдоним;</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строка, которая предоставляет альтернативное имя для домена, указанный в аргументе <em>в</em> . Позволяет сократить имя таблицы для последующих ссылок избежать возможных неоднозначных ссылок. Если <em>псевдоним</em> не указан, будут использовать имя таблицы или запроса в качестве псевдоним.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Действие **[ExitForEachRecord](exitforeachrecord-macro-action.md)** используется для выхода из блока **ДляКаждойЗаписи** данных немедленно.

