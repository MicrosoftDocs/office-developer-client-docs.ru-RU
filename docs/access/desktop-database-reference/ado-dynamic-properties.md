---
title: Динамические свойства ADO
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fae0df2a4cc5c9de585d2b101e9fa31cb6a0a545
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281717"
---
# <a name="ado-dynamic-properties"></a>Динамические свойства ADO

**Область применения**: Access 2013, Office 2013

Динамические свойства можно добавить в коллекции [свойств](properties-collection-ado.md) объектов [Connection,](connection-object-ado.md) [Command](command-object-ado.md)или [Recordset.](recordset-object-ado.md) Источником этих свойств является либо поставщик данных, например поставщик [OLE DB](microsoft-ole-db-provider-for-sql-server.md)для SQL Server, либо поставщик услуг, например служба курсора Майкрософт для [OLE DB.](microsoft-cursor-service-for-ole-db-ado-service-component.md) Дополнительные сведения об определенном динамическом свойстве можно найти в соответствующей документации поставщика данных или поставщика услуг.

Индекс [динамического свойства ADO](ado-dynamic-property-index.md) предоставляет перекрестную ссылку между именами ADO и OLE DB для каждого стандартного динамического свойства поставщика OLE DB.

Следующие динамические свойства имеют особый интерес и также описаны в источниках, упомянутых выше. Специальные функции ADO описаны в справке ADO, перечисленных ниже.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Динамическое свойство</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">Оптимизация</a></p></td>
<td><p>Указывает, следует ли создавать индекс для этого поля.</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Prompt</a></p></td>
<td><p>Указывает, должен ли поставщик OLE DB затметь пользователю информацию об инициализации.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Указывает имя объекта <strong>Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Указывает предоставленную пользователем строку команды, которую метод <strong>Resync</strong> выдает для обновления данных в таблице с именем в динамическом свойстве <strong>Unique Table.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица, уникальная схема, уникальный каталог</a></p></td>
<td><p><strong>Уникальная</strong> таблица — указывает имя базовой таблицы, в которой разрешены обновления, вставки и удаления.<br/><br/><strong>Уникальная схема</strong> — указывает схему или имя владельца таблицы.<br/><br/><strong>Уникальный каталог</strong> — указывает каталог или имя базы данных, содержащей таблицу.</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Обновление resync</a></p></td>
<td><p>Указывает, следует ли за <strong>методом UpdateBatch</strong> неявную операцию метода <strong>Resync</strong> и, если да, область этой операции.</p></td>
</tr>
</tbody>
</table>

<br/>

