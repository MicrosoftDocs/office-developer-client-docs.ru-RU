---
title: Метод Recordset2. Update (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4259da0eb48e7ff13e246b326cc6e96d7a916ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307170"
---
# <a name="recordset2update-method-dao"></a>Метод Recordset2. Update (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*expression* .Update(***UpdateType***, ***Force***)

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Необязательна</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Константа <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>, обозначающая тип обновления, заданный в параметрах (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><em>Сила</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Логический</strong></p></td>
<td><p><strong>Логическое</strong> значение, указывающее, следует ли принудительно вносить изменения в базу данных независимо от того, были ли базовые данные изменены другим пользователем с момента вызова метода <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> или <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>. Если задано значение <strong>True</strong>, то ваши изменения принудительно применяются, а изменения, внесенные другими пользователями, просто перезаписываются. Если задано значение <strong>False</strong> (по умолчанию), то изменения, внесенные другими пользователями, пока обновление ожидает обработки, приведут к сбоям обновления в конфликтных участках. Ошибка не возникает, но в свойствах <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> и <strong>BatchCollisions</strong> указывается количество конфликтов и затронутых ими строк, соответственно (только для рабочих областей ODBCDirect).</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Используйте метод **Update**, чтобы сохранить текущую запись и все внесенные в нее изменения.

> [!IMPORTANT]
> Изменения текущей записи теряются, если:
> - вызвать метод **Edit** или **AddNew**, а затем перейти к другой записи, не используя перед этим метод **Update**;
> - вызвать метод **Edit** или **AddNew**, а затем снова применить метод **Edit** или **AddNew**, не используя перед этим метод **Update**;
> - указать в свойстве **[Bookmark](recordset2-bookmark-property-dao.md)** другую запись;
> - закрыть объект **Recordset**, не используя перед этим метод **Update**;
> - отменить операцию **Edit** с помощью метода **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Чтобы изменить запись, используйте метод **Edit** для копирования содержимого текущей записи в буфер обмена. Если сначала не вызвать метод **Edit**, то при использовании метода **Update** или попытке изменить значение поля возникнет ошибка.

В рабочей области ODBCDirect можно выполнять пакетное обновление, при условии что библиотека курсоров поддерживает его, а объект **Recordset** был открыт с использованием оптимистичной блокировки пакетных операций.

Если в рабочей области Microsoft Access для свойства **LockEdits** объекта **Recordset** задано значение **True** (пессимистичная блокировка) в многопользовательской среде, то запись останется заблокированной с момента вызова метода **Edit** до завершения выполнения метода **Update** или отмены изменения. Если для свойства **LockEdits** задано значение **False** (оптимистичная блокировка), то запись блокируется и сравнивается с ее вариантом непосредственно перед обновлением в базе данных. Если запись изменилась с момента использования метода **Edit**, происходит сбой операции **Update**. В базах данных ODBC, подключенных к ядру СУБД Microsoft Access, и устанавливаемых базах данных ISAM всегда используется оптимистичная блокировка. Чтобы продолжить выполнение операции **Update** с вашими изменениями, снова вызовите метод **Update**. Чтобы вернуть запись в состояние, оставленное другим пользователем, обновите текущую запись с помощью команды Move 0.

> [!NOTE]
> Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс. В противном случае возникнет ошибка "Отказано в разрешении" (при вызове метода **AddNew**, **Delete** или **Edit** в рабочей области Microsoft Access) или ошибка "Недопустимый аргумент" (при вызове метода **Update** в рабочей области ODBCDirect).


