---
title: Метод клонирования — ActiveX объектов данных (ADO)
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
# <a name="clone-method-ado"></a>Метод клонирования (ADO)

**Область применения**: Access 2013, Office 2013

Создает дубликат [объекта Recordset](recordset-object-ado.md) из существующего объекта **Recordset.** Необязательно указывает, что клон должен быть только для чтения.

## <a name="syntax"></a>Синтаксис

**Установите** *rstDuplicate*  =  *rstOriginal*. Клон *(LockType)*

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку **на объект Recordset.**

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*rstDuplicate* |Переменная объекта, идентифицирует созданный объект **Recordset.**|
|*rstOriginal* |Переменная объекта, идентифицирует объект **Recordset,** который будет дублироваться.|
|*LockType* |Необязательный параметр. Значение [LockTypeEnum,](locktypeenum.md) которое указывает тип блокировки исходного **набора записей** или только для **чтения.** Допустимые значения **adLockUnspecified** или **adLockReadOnly.**|

## <a name="remarks"></a>Примечания

Используйте метод **Клона** для создания нескольких дублирующихся объектов **Recordset,** особенно если вы хотите сохранить несколько текущих записей в определенном наборе записей. Использование метода **Клона** является более эффективным, чем создание и открытие нового объекта **Recordset** с тем же определением, что и оригинал.

Свойство [Filter](filter-property-ado.md) исходного **набора записей,** если таково, не будет применено к клону. Установите свойство **Filter** нового **набора записей** для фильтрации результатов. Самый простой способ скопировать существующее значение **Filter** — назначить его напрямую, например:

Текущая запись только что созданного клона установлена к первой записи.

Изменения, внесенные в один **объект Recordset,** видны во всех его клонах независимо от типа курсора. Однако после выполнения [Requery](requery-method-ado.md) в исходном **Наборе записей** клоны больше не будут синхронизированы с оригиналом.

Закрытие **исходного набора записей** не закрывает его копии и не закрывает копию оригинала или других копий.

Клонировать можно только объект **Recordset,** который поддерживает закладки. Значения закладок взаимозаменяемы; то есть ссылка на закладки с одного объекта **Recordset** относится к одной записи в любом из его клонов.

Некоторые  срабатываемые события Recordset также будут запускать во всех **клонах Recordset.** Однако, поскольку текущая запись может отличаться между клонированными записями, события могут быть не допустимы для клона.

Например, при изменении значения поля событие [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) будет происходить  в измененной записи и во всех клонах. Параметр *Fields* события **WillChangeField** клонированной записи (где изменение не было сделано) будет просто ссылаться на поля текущей записи клона, которая может быть другой записью, чем текущая запись исходного **recordset,** где произошли изменения. 

В следующей таблице представлен полный список всех событий **Recordset** и указывается, являются ли они допустимы и запускаются для всех клонов наборов записей, созданных с помощью метода **Клона.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Событие</p></th>
<th><p>Срабатывает в клонах?</p></th>
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

