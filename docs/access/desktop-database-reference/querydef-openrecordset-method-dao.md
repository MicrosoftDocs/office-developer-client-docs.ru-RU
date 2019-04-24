---
title: Метод QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302851"
---
# <a name="querydefopenrecordset-method-dao"></a>Метод QueryDef.OpenRecordset (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[Recordset](recordset-object-dao.md)** и добавляет его в коллекцию **Recordsets**.

## <a name="syntax"></a>Синтаксис

*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)

*выражение*: переменная, представляющая объект **QueryDef**.

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
<td><p><em>Type</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>, которая указывает на то, какой тип объекта <strong>Recordset</strong> нужно открыть.</p><p><strong>ПРИМЕЧАНИЕ</strong>: при открытии <STRONG>Recordset</STRONG> в рабочей области Microsoft Access, если вы не указали тип, <STRONG>OpenRecordset</STRONG> создает табличный тип <STRONG>Recordset</STRONG>, если возможно. Вы укажете связанную таблицу или запрос, <STRONG>OpenRecordset</STRONG> создаст объект <STRONG>Recordset</STRONG> типа dynaset.</p>
</td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>, которые указывают характеристики нового объекта <strong>Recordset</strong>.</p></p><p><strong>ПРИМЕЧАНИЕ</strong>: Константы <STRONG>dbConsistent</STRONG> и <STRONG>dbInconsistent</STRONG> являются взаимоисключающими, и использование обоих констант вызывает ошибку. Предоставление аргумента lockedits, когда опции используют константы <STRONG>dbReadOnly</STRONG>, также приводит к возникновению ошибки.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>LockEdit</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>, определяющая блокировку <strong>Recordset</strong>.</p></p><p><strong>NOTE</strong>: вы можете использовать <STRONG>dbReadOnly</STRONG> или в аргументе параметров или в аргументе lockedits, но не одновременно. Если вы используете его для обоих аргументов, возникает ошибка во время выполнения.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Recordset

## <a name="remarks"></a>Комментарии

Вы также можете использовать константу **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** при открытии **Recordset** в рабочей области ODBC, подключенной к ядру СУБД Microsoft Access для таблицы Microsoft SQL Server 6.0 (или более поздней версии), содержащей столбец IDENTITY, в противном случае может возникать ошибка.

Открытие нескольких объектов **Recordset** для источника данных ODBC может привести к завершении работы, так как подключение будет занято предыдущим вызовом **OpenRecordset**. Одним из способов решения этой проблемы состоит в полном заполнении **Recordset** с помощью метода **[MoveLast](recordset-movelast-method-dao.md)** непосредственно после открытия **Recordset**.

Закрытие **Recordset** с помощью метода **Close** автоматически удаляет его из коллекции **Recordsets**.

> [!NOTE]
> Если *источник* ссылается на оператора SQL, состоящий из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия **Recordset**. Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL поддерживает только десятичные символы, используемые в США.


