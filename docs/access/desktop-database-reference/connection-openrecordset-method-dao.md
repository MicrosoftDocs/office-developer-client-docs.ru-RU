---
title: Метод Connection. OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abbb7a4f58714aef0e085d0f37b5ee49378e0f51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295851"
---
# <a name="connectionopenrecordset-method-dao"></a>Метод Connection. OpenRecordset (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.

## <a name="syntax"></a>Синтаксис

*Expression* . OpenRecordset (***имя***, ***Тип***, ***Параметры***, ***локкедит***)

*выражение*: переменная, представляющая объект **Connection**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Источник записей для нового объекта <strong>Recordset</strong>. Источником может быть имя таблицы, имя запроса или оператор SQL, возвращающий записи. Для объектов <strong>Recordset</strong> табличного типа в базах данных ядра СУБД Microsoft Access источником может быть только имя таблицы.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</p><p><strong>ПРИМЕЧАНИЕ</strong>: при открытии <strong>Recordset</strong> в рабочей области Microsoft Access, если вы не указали тип, <strong>OpenRecordset</strong> создает табличный тип <strong>Recordset</strong>, если возможно. Вы укажете связанную таблицу или запрос, <strong>OpenRecordset</strong> создаст объект <strong>Recordset</strong> типа dynaset.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</p><p><strong>ПРИМЕЧАНИЕ</strong>. Константы <strong>dbConsistent</strong> и <strong>dbInconsistent</strong> являются взаимоисключающими, и использование обеих констант вызывает ошибку. Если параметры используют константу <strong>dbReadOnly</strong> , можно указать аргумент LockEdits, что приводит к ошибке.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</p><p><strong>NOTE</strong>: вы можете использовать <strong>dbReadOnly</strong> или в аргументе параметров или в аргументе lockedits, но не одновременно. Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Recordset

## <a name="remarks"></a>Примечания

Обычно если у пользователя возникает эта ошибка во время обновления записи, код должен обновлять содержимое полей и возвращать измененные значения. Если ошибка возникает при удалении записи, код может отобразить для пользователя данные новой записи и сообщение о недавнем изменении данных. В этот момент код может запросить у пользователя подтверждение удаления записи.

Вы также можете использовать константу **dbSeeChanges** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.

Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершению работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**. Один из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **MoveLast** непосредственно после открытия **Recordset**.

Закрытие **Recordset** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет его из коллекции **Recordsets**.

> [!NOTE]
> Если *источник* ссылается на оператор SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**. Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.


