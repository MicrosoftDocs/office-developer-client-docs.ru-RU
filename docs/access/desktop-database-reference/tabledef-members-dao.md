---
title: TableDef Members (DAO)
TOCTitle: TableDef Members
ms:assetid: bc55315e-bafe-d89e-ad31-fd4c9bb6486e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822714(v=office.15)
ms:contentKeyID: 48547408
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c597bc75f629e2f34302ecd30f3ef589ad4d4561
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885509"
---
# <a name="tabledef-members-dao"></a>TableDef Members (DAO)


**Применимо к**: Access 2013, Office 2013

Объект TableDef представляет сохраненные определение базовая таблица или связанной таблицы (только для рабочих областей Microsoft Access).

## <a name="methods"></a>Методы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="tabledef-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="field-object-dao.md">поля</a></strong> (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-createindex-method-dao.md">CreateIndex</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="index-object-dao.md">индекса</a></strong> (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-refreshlink-method-dao.md">RefreshLink</a></strong></p></td>
<td><p>Обновляет сведения о подключении для связанной таблицы (только для рабочих областей Microsoft Access).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="tabledef-attributes-property-dao.md">Атрибуты</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, один или несколько характеристик объекта <strong>TableDef</strong> . Чтение и запись <strong>времени</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-conflicttable-property-dao.md">ConflictTable</a></strong></p></td>
<td><p>Возвращает имя таблицы конфликта, содержащий записи базы данных, которые конфликт во время синхронизации двух реплик (только для рабочих областей Microsoft Access). Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-connect-property-dao.md">Подключение</a></strong></p></td>
<td><p>Задает или возвращает значение, которое предоставляет сведения о связанной таблицы. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access). Только для чтения <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-fields-property-dao.md">Поля</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-indexes-property-dao.md">Индексы</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>индексов</strong> , который содержит все хранимые объекты <strong>индекса</strong> для указанной таблицы. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Возвращает дату и время последнего изменения, внесенные в объект. Только для чтения <strong>Variant</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Возвращает общее число записей в объекте <strong><a href="tabledef-object-dao.md">TableDef</a></strong> . Только для чтения <strong>времени</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-replicafilter-property-dao.md">Этого</a></strong></p></td>
<td><p>Задает или возвращает значение на объекте <strong><a href="tabledef-object-dao.md">TableDef</a></strong> в реплику, которое указывает, какие подмножество записей реплицированы на таблицу с полной реплики. (Microsoft Access рабочие области только).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее имя связанной таблицы или имя таблицы (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-updatable-property-dao.md">Обновляемые</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-validationrule-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Чтение и запись <strong>строки</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-validationtext-property-dao.md">Сообщение об ошибке</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение <strong>поля</strong> объекта не удовлетворяют правило проверки, указанного идентификатором <strong>условие на значение</strong> свойства поля (только для рабочих областей Microsoft Access) . Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
</tbody>
</table>

