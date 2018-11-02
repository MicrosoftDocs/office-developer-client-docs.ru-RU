---
title: Динамические свойства ADO
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab0d84931389aecb5bd495c884baa9163c52d4a6
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910924"
---
# <a name="ado-dynamic-properties"></a>Динамические свойства ADO

**Применимо к**: Access 2013, Office 2013

Динамические свойства можно добавить в коллекции [свойств](properties-collection-ado.md) объектов [подключения](connection-object-ado.md), [команда](command-object-ado.md)или [набора записей](recordset-object-ado.md) . Источник данных свойств — это либо поставщик данных, таких как [Поставщик OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md)или поставщика услуг, таких как [Служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Обратитесь к требуемые данные поставщика или документации поставщика службы Дополнительные сведения о конкретных динамического свойства.

[Динамические свойства индекса ADO](ado-dynamic-property-index.md) предоставляет перекрестная ссылка между имена ADO и OLE DB для каждого стандартных OLE DB поставщика динамические свойства.

Следующие свойства динамического представляют интерес и также описаны в источниках, перечисленных выше. Специальные функциональные возможности с помощью ADO описана в перечисленных ниже разделах справки ADO.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Динамические свойства</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">Оптимизация</a></p></td>
<td><p>Указывает, следует ли создавать индекса на это поле.</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Запрос</a></p></td>
<td><p>Указывает, следует ли поставщик OLE DB запрашивать у пользователя сведения инициализации.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Изменить форму имя</a></p></td>
<td><p>Указывает имя для объекта <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Команда синхронизации</a></p></td>
<td><p>Указывает строку пользовательские команды, метод <strong>выполнить повторную синхронизацию</strong> проблемы для обновления данных в таблице с именем в свойстве динамических <strong>Уникальной таблицы</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальной таблицы, уникальные схемы, уникальный каталога</a></p></td>
<td><p><strong>Уникальная таблица</strong> — определяет имя базовая таблица, для которой разрешены обновления, вставки и удаления.<br/><br/><strong>Уникальный схемы</strong> — определяет схему или имя владельца таблицы.<br/><br/><strong>Уникальный каталога</strong> — указывает каталог или имя базы данных, содержащий таблицу.</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Обновление повторной синхронизации</a></p></td>
<td><p>Указывает, будет ли метод <strong>UpdateBatch</strong> следуют неявных <strong>выполнить повторную синхронизацию</strong> метод операцию и если да, области действия этой операции.</p></td>
</tr>
</tbody>
</table>

<br/>

