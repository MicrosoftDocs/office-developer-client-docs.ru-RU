---
title: Метод Recordset2. OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08120f4ebb6b2d9989051171a0c71b6d9fcf6e5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307254"
---
# <a name="recordset2openrecordset-method-dao"></a>Метод Recordset2. OpenRecordset (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.

## <a name="syntax"></a>Синтаксис

*Expression* . OpenRecordset (***тип***, ***Параметры***)

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Источник записей для нового объекта <strong>Recordset</strong>. Источником может быть имя таблицы, имя запроса или инструкция SQL, возвращающая записи. Для объектов <strong>Recordset</strong> табличного типа в базах данных ядра СУБД Microsoft Access источник может быть только именем таблицы.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</p><p><strong>ПРИМЕЧАНИЕ</strong>: при открытии <STRONG>Recordset</STRONG> в рабочей области Microsoft Access, если вы не указали тип, <STRONG>OpenRecordset</STRONG> создает табличный тип <STRONG>Recordset</STRONG>, если возможно. Вы укажете связанную таблицу или запрос, <STRONG>OpenRecordset</STRONG> создаст объект <STRONG>Recordset</STRONG> типа dynaset.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</p><p><strong>ПРИМЕЧАНИЕ</strong>: Константы <STRONG>dbConsistent</STRONG> и <STRONG>dbInconsistent</STRONG> являются взаимоисключающими, и использование обоих констант вызывает ошибку. Предоставление аргумента lockedits, когда опции используют константы <STRONG>dbReadOnly</STRONG>, также приводит к возникновению ошибки.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</p><p><strong>NOTE</strong>: вы можете использовать <STRONG>dbReadOnly</STRONG> или в аргументе параметров или в аргументе lockedits, но не одновременно. Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Recordset

## <a name="remarks"></a>Комментарии

Как правило, если пользователь получает это сообщение об ошибке при обновлении записи, код должен обновлять содержимое полей и получать только что измененные значения. Если при удалении записи возникла ошибка, код может отобразить данные новой записи и сообщение о том, что данные были недавно изменены. На этом шаге ваш код может запросить подтверждение того, что пользователь по-прежнему хочет удалить запись.

Вы также можете использовать константу **dbSeeChanges** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.

Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершении работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**. Одним из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **MoveLast** непосредственно после открытия **Recordset**.

Закрытие объекта **Recordset** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет его из коллекции **наборов записей** .

> [!NOTE]
> Если *источник* ссылается на оператора SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**. Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.


