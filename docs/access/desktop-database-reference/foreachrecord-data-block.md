---
title: Блок данных ForEachRecord
TOCTitle: ForEachRecord Data Block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dffb433d8a7023b725ebcb5c1e5f651d86f9dbd7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886552"
---
# <a name="foreachrecord-data-block"></a>Блок данных ForEachRecord


**Применимо к**: Access 2013, Office 2013

Блок данных **ДляКаждойЗаписи** повторяет набор инструкций для каждой записи в домене.


> [!NOTE]
> <P>Блок данных <STRONG>ДляКаждойЗаписи</STRONG> доступна только в макросов данных.</P>



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
> <P>Указанный домен не может включать данные, хранящиеся в связанной таблице или источник данных ODBC.</P>


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


## <a name="remarks"></a>Замечания

Действие **[ExitForEachRecord](exitforeachrecord-macro-action.md)** используется для выхода из блока **ДляКаждойЗаписи** данных немедленно.

