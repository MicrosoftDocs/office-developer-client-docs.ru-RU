---
title: Метод Recordset2.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8dff02bcdd488edab33251b4d1184d2ede387876
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925767"
---
# <a name="recordset2openrecordset-method-dao"></a>Метод Recordset2.OpenRecordset (DAO)


**Применимо к**: Access 2013, Office 2013

Создает новый объект **[набора записей](recordset-object-dao.md)** и добавляет его в коллекцию **наборов записей** .

## <a name="syntax"></a>Синтаксис

*выражение* . OpenRecordset (***Тип***, ***Параметры***)

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Источник записей для нового <strong>набора записей</strong>. Источник может быть имя таблицы, имя запроса или инструкции SQL, которая возвращает записи. Для объектов <strong>наборов записей</strong> в таблице типа в базами данных, ядро базы данных Microsoft Access источник может быть только имя таблицы.</p></td>
</tr>
<tr class="even">
<td><p>Тип</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> , указывающая тип <strong>набора записей</strong> , чтобы открыть.</p>

> [!NOTE]
> <P>При открытии <STRONG>набора записей</STRONG> в рабочей области Microsoft Access и тип не указан, <STRONG>OpenRecordset</STRONG> создает табличного типа <STRONG>записей</STRONG>, если это возможно. При указании связанной таблицы или запроса, <STRONG>OpenRecordset</STRONG> создает добавляющий <STRONG>набора записей</STRONG>.</P>


</td>
</tr>
<tr class="odd">
<td><p>Options</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Сочетание констант <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> , которые задают характеристики нового <strong>набора записей</strong>.</p>

> [!NOTE]
> <P>Константы <STRONG>dbConsistent</STRONG> и <STRONG>dbInconsistent</STRONG> являются взаимоисключающими и использовании обоих приводит к ошибке. Также указав аргумент lockedits при параметры использует константу <STRONG>dbReadOnly</STRONG> приводит к ошибке.</P>


</td>
</tr>
<tr class="even">
<td><p>LockEdit</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> , определяющая блокировки для <strong>набора записей</strong>.</p>

> [!NOTE]
> <P>Можно использовать <STRONG>dbReadOnly</STRONG> в аргументе параметры или аргумент lockedits, но не оба. При использовании обоих аргументов, возникает ошибка времени выполнения.</P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Набор записей

## <a name="remarks"></a>Примечания

Как правило если пользователь получает Эта ошибка при обновлении записи, код должен обновить содержимое полей и извлечение измененные значения. Если ошибка возникает при удалении записи, кода удалось отобразить новые записи данных для пользователя и сообщение, указывающее, что недавно были изменены данные. На этом этапе кода можно запросить подтверждения, что по-прежнему требуется удалить эту запись.

Константа **dbSeeChanges** также следует использовать при открытии **набора записей** в таблице Microsoft Access базы данных подключен модуль ODBC рабочей области для Microsoft SQL Server 6.0 (или более поздней версии), которая имеет столбец ИДЕНТИФИКАТОРОВ, в противном случае может возникнуть ошибка.

Открытие более одного **набора записей** в источник данных ODBC могут завершиться с ошибкой из-за занятости с предыдущего вызова **OpenRecordset** подключение. Один способ, является полностью заполнить **набора записей** с помощью метода **MoveLast** сразу же после открытия **набора записей** .

Закрытие набора **записей** с помощью метода **[Close](connection-close-method-dao.md)** автоматически удаляет из коллекции **наборов записей** .


> [!NOTE]
> <P>Если <EM>источник</EM> относится к инструкции SQL состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE &gt; " &amp; lngPrice и lngPrice = 125,50), возникает ошибка при попытке открыть <STRONG>набора записей</STRONG>. Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и SQL принимает только США десятичных знаков.</P>


