---
title: Метод Clone — объекты данных ActiveX (ADO)
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

Создает дубликат объекта [Recordset](recordset-object-ado.md) из существующего объекта **Recordset** . При необходимости этот параметр указывает, что клон должен быть доступен только для чтения.

## <a name="syntax"></a>Синтаксис

**Set** *рстдупликате*  =  *рсторигинал*. Clone (*LockType*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на объект **Recordset** .

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Рстдупликате* |Объектная переменная, определяющая дубликат создаваемого объекта **Recordset** .|
|*Рсторигинал* |Объектная переменная, определяющая объект **Recordset** , который будет дублироваться.|
|*LockType* |Необязательный атрибут. Значение [LockTypeEnum](locktypeenum.md) , задающее либо тип блокировки исходного объекта **Recordset**, либо **набор записей**, доступное только для чтения. Допустимые значения: **адлоккунспеЦифиед** и **адлоккреадонли**.|

## <a name="remarks"></a>Замечания

Используйте метод **clone** для создания нескольких дублирующихся объектов **Recordset** , в частности, если требуется поддерживать несколько текущих записей в заданном наборе записей. Использование метода **clone** является более эффективным, чем создание и открытие нового объекта **Recordset** с тем же определением, что и исходный.

Свойство [Filter](filter-property-ado.md) исходного объекта **Recordset**(если таковое имеется) не будет применено к клону. Задайте свойство **Filter** для нового объекта **Recordset** , чтобы отфильтровать результаты. Самый простой способ скопировать любое существующее значение **фильтра** — назначить его напрямую, как показано ниже:

Для текущей записи созданного клона задается первая запись.

Изменения, вносимые в один объект **Recordset** , отображаются во всех клонах, независимо от типа курсора. Однако после выполнения командлета [Requery](requery-method-ado.md) для исходного объекта **Recordset**клоны больше не будут синхронизироваться с исходным.

Закрытие исходного объекта **Recordset** не приводит к закрытию его копий, а также закрытию копии.

Можно клонировать только объект **Recordset** , который поддерживает закладки. Значения закладок являются взаимозаменяемыми; то есть ссылка на закладку из одного объекта **Recordset** ссылается на одну и ту же запись в любом из его клонов.

Некоторые инициированные события **Recordset** также будут срабатывать во всех клонах **набора записей** . Тем не менее, поскольку текущая запись может различаться с помощью клонированных **наборов записей**, события могут быть недопустимы для клона.

Например, если изменить значение поля, событие [события willchangefield](willchangefield-and-fieldchangecomplete-events-ado.md) будет происходить в измененном **наборе записей** и всех клонах. Параметр *Fields* для события **события willchangefield** клонированного **набора записей** (если это изменение не был изменен) просто ссылается на поля текущей записи клона, которые могут отличаться от текущей записи исходный объект **Recordset** , в котором произошло изменение.

В следующей таблице представлен полный список всех событий **Recordset** и указано, являются ли они допустимыми и запущены для всех клонов наборов записей, созданных с помощью метода **clone** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Событие</p></th>
<th><p>Активировано в клонах?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">Событие endofrecordset</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchcomplete-event-ado.md">Событие fetchcomplete</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">Событие fetchprogress</a></p></td>
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
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">События willchangefield</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">События willchangerecord</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">События willchangerecordset</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">События WillMove</a></p></td>
<td><p>Нет</p></td>
</tr>
</tbody>
</table>

