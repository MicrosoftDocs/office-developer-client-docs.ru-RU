---
title: Index Members (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 18f885dadb5ef86f78ed0a19ca9b2a5feb424b34
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483175"
---
# <a name="index-members-dao"></a>Index Members (DAO)


**Применимо к**: Access 2013 | Office 2013

Объекты индекса указать порядок записей, доступного из таблицы базы данных и принимаются ли повторяющихся записей, предоставляя эффективного доступа к данным. Для внешних баз данных объекты индекса описывают индексов, установленных для внешних таблиц (только для рабочих областей Microsoft Access).

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
<td><p><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="field-object-dao.md">поля</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</p></td>
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
<td><p><strong><a href="index-clustered-property-dao.md">Кластерные</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, представляет ли объект <strong>индекса</strong> кластеризованных индекса для таблицы (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">Число различных значений</a></strong></p></td>
<td><p>Возвращает значение, указывающее количество уникальных значений для объекта <strong><a href="index-object-dao.md">индекса</a></strong> , содержащихся в связанной таблице (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Поля</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта. Для чтения и записи.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Внешний</a></strong></p></td>
<td><p>Возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> внешний ключ в таблице (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, имеют ли записи, для которых значения Null в полях индекса записи индекса (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию. Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Основной</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> индекс первичного ключа для таблицы (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Обязательный</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли объект <strong><a href="field-object-dao.md">поля</a></strong> ненулевое значение.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Уникальный</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> уникальный индекс (основные) для таблицы (только для рабочих областей Microsoft Access).</p></td>
</tr>
</tbody>
</table>

