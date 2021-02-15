---
title: Метод Clone — ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296348"
---
# <a name="clone-method-ado"></a>Метод Clone (ADO)

**Область применения**: Access 2013, Office 2013

Создает дубликат [объекта Recordset](recordset-object-ado.md) из существующего объекта **Recordset.** При желании указывает, что клон должен быть только для чтения.

## <a name="syntax"></a>Синтаксис

**Set** *rstDuplicate*  =  *rstOriginal*. Clone *(LockType)*

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку **на объект Recordset.**

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*rstDuplicate* |Объектная переменная, идентифицирует **дубликат объекта Recordset,** который необходимо создать.|
|*rstOriginal* |Объектная переменная, определяя объект **Recordset** для дублирования.|
|*LockType* |Необязательный параметр. Значение [LockTypeEnum,](locktypeenum.md) которое указывает тип блокировки исходного **recordset** или только для **чтения.** Допустимые **значения: adLockUnspecified** или **adLockReadOnly.**|

## <a name="remarks"></a>Заметки

Используйте метод **Clone** для создания нескольких повторяюных объектов **Recordset,** особенно если вы хотите сохранить несколько текущих записей в заданный набор записей. Использование метода **Clone** более эффективно, чем создание и открытие объекта **Recordset** с тем же определением, что и у исходного объекта.

Свойство [Filter](filter-property-ado.md) исходного объекта **Recordset**(если таково) не будет применено к клону. Установите свойство **Filter** нового набора **записей для** фильтрации результатов. Самый простой способ скопировать любое существующее значение **Filter** — назначить его напрямую, как по этому:

Для текущей записи только что созданного клона устанавливается первая запись.

Изменения, внесенные в один **объект Recordset,** видны во всех его клонах независимо от типа курсора. Однако после выполнения [Requery](requery-method-ado.md) в исходном наборе **записей** клоны больше не будут синхронизироваться с исходным набором.

Закрытие **исходного наборов записей** не закрывает копии и не закрывает исходную или любую из других копий.

Клонировать можно только объект **Recordset,** который поддерживает закладки. Значения закладок являются взаимозаменяемыми; то есть ссылка на закладку из одного объекта **Recordset** ссылается на ту же запись в любом из его клонов.

Некоторые активированные события **Recordset** также будут запускаться во всех **клонах recordset.** Однако так как текущая запись может отличаться для клонированных записей, события могут быть не допустимы для клона.

Например, если изменить значение поля, событие [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) будет происходить в измененных **наборе записей** и во всех клонах. Параметр *Fields* события **WillChangeField** клонированного наборов записей **(в** котором изменение не было выполнено) будет просто ссылаться на поля текущей записи  клона, которая может быть отличается от текущей записи исходного наборов записей, где произошло изменение.

В следующей таблице представлен полный список всех событий **Recordset,** а также указано, являются ли они допустимами и активированными для всех клонов наборов записей, созданных с помощью метода **Clone.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Событие</p></th>
<th><p>Активирован в клонах?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>Нет</p></td>
</tr>
</tbody>
</table>

