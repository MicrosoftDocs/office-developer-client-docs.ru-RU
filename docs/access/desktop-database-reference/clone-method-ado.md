---
title: Клонирование метод - ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 857a007d1b3bfe2665eea1284bc41cc9c67ccd46
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944440"
---
# <a name="clone-method-ado"></a>Метод Clone (ADO)


**Применимо к**: Access 2013, Office 2013



Создает объект повторяющихся [записей](recordset-object-ado.md) из существующего объекта **набора записей** . При необходимости указывает копию только для чтения.

## <a name="syntax"></a>Синтаксис

**Установка** *rstDuplicate*  =  *rstOriginal*. Копия (*LockType для*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на объект **набора записей** .

## <a name="parameters"></a>Параметры

- *rstDuplicate*

  - Объектная переменная, которая определяет повторяющихся **записей** объект будет создан.

- *rstOriginal*

  - Объектная переменная, которая определяет объект **набора записей** дублирование.

- *LockType для*

  - Необязательно указывать. [LockTypeEnum](locktypeenum.md) значение, задающее тип блокировки исходного **набора записей**или только для чтения **набора записей**. Допустимые значения: **adLockUnspecified** или **adLockReadOnly**.

## <a name="remarks"></a>Примечания

Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** , особенно в том случае, если вы хотите поддерживать более одного текущей записи в данного набора записей. С помощью метода **клонированной** эффективнее, чем создания и открытия нового объекта **набора записей** с тем же определением, что и исходный.

Свойства [фильтра](filter-property-ado.md) из исходного **набора записей**при их наличии, не применяются к копии. Свойства **фильтра** нового **набора записей** для фильтрации результатов. Чтобы скопировать все существующие значения **фильтра** проще всего напрямую, назначьте его следующим образом:

Текущая запись только что созданный клонированной присвоено значение первой записи.

Изменения, внесенные на **один Recordset** видны во всех его копирует вне зависимости от типа курсора. Тем не менее после выполнения [запроса](requery-method-ado.md) на исходный **набора записей**копирует больше не синхронизируются с исходным.

Закрытие исходного **набора записей** не закрывайте его копии, а также закрывая копии закрыть исходной или любых других копий.

Можно только клонирование объекта **набора записей** , который поддерживает закладки. Значения закладки являются взаимозаменяемыми; Таким образом закладка ссылку из одного объекта **набора записей** относится к одной и той же записи в любом из его копирует.

Некоторые события **набора записей** , которые запускаются также будет срабатывать в копирует все **набора записей** . Тем не менее так как текущей записи может отличаться от клонирования **наборов записей**, события могут быть допустимый для копии.

Например, при изменении значения поля [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) событие происходит в измененных **записей** и копирует все. Параметр *поля* событие **WillChangeField** клонирования **записей** (где не изменения) просто будет ссылаться на поля текущей записи копии, может быть другой записи превышает текущий запись где произошло изменение исходного **набора записей** .

В следующей таблице предоставляются полный список всех **записей** событий и указывает, являются ли они действительный и включаемая для любого копирует набора записей, созданных с помощью метода **клонирования** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Событие</p></th>
<th><p>Запущено копирует?</p></th>
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

