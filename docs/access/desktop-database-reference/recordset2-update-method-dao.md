---
title: Метод Recordset2.Update (DAO)
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
# <a name="recordset2update-method-dao"></a><span data-ttu-id="f3378-102">Метод Recordset2.Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3378-102">Recordset2.Update method (DAO)</span></span>

<span data-ttu-id="f3378-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3378-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f3378-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3378-104">Syntax</span></span>

<span data-ttu-id="f3378-105">*expression* .Update(***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="f3378-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="f3378-106">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="f3378-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3378-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3378-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3378-108">Имя</span><span class="sxs-lookup"><span data-stu-id="f3378-108">Name</span></span></p></th>
<th><p><span data-ttu-id="f3378-109">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="f3378-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f3378-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f3378-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="f3378-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f3378-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3378-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="f3378-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="f3378-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f3378-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="f3378-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="f3378-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="f3378-115">Константа <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>, обозначающая тип обновления, заданный в параметрах (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="f3378-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3378-116"><em>Сила</em></span><span class="sxs-lookup"><span data-stu-id="f3378-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="f3378-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f3378-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="f3378-118"><strong>Логический</strong></span><span class="sxs-lookup"><span data-stu-id="f3378-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f3378-119"><strong>Логическое</strong> значение, указывающее, следует ли принудительно вносить изменения в базу данных независимо от того, были ли базовые данные изменены другим пользователем с момента вызова метода <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> или <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="f3378-119">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call.</span></span> <span data-ttu-id="f3378-120">Если задано значение <strong>True</strong>, то ваши изменения принудительно применяются, а изменения, внесенные другими пользователями, просто перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="f3378-120">If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten.</span></span> <span data-ttu-id="f3378-121">Если задано значение <strong>False</strong> (по умолчанию), то изменения, внесенные другими пользователями, пока обновление ожидает обработки, приведут к сбоям обновления в конфликтных участках.</span><span class="sxs-lookup"><span data-stu-id="f3378-121">If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict.</span></span> <span data-ttu-id="f3378-122">Ошибка не возникает, но в свойствах <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> и <strong>BatchCollisions</strong> указывается количество конфликтов и затронутых ими строк, соответственно (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="f3378-122">No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f3378-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3378-123">Remarks</span></span>

<span data-ttu-id="f3378-124">Используйте метод **Update**, чтобы сохранить текущую запись и все внесенные в нее изменения.</span><span class="sxs-lookup"><span data-stu-id="f3378-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3378-125">Изменения текущей записи теряются, если:</span><span class="sxs-lookup"><span data-stu-id="f3378-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="f3378-126">вызвать метод **Edit** или **AddNew**, а затем перейти к другой записи, не используя перед этим метод **Update**;</span><span class="sxs-lookup"><span data-stu-id="f3378-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="f3378-127">вызвать метод **Edit** или **AddNew**, а затем снова применить метод **Edit** или **AddNew**, не используя перед этим метод **Update**;</span><span class="sxs-lookup"><span data-stu-id="f3378-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="f3378-128">указать в свойстве **[Bookmark](recordset2-bookmark-property-dao.md)** другую запись;</span><span class="sxs-lookup"><span data-stu-id="f3378-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="f3378-129">закрыть объект **Recordset**, не используя перед этим метод **Update**;</span><span class="sxs-lookup"><span data-stu-id="f3378-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="f3378-130">отменить операцию **Edit** с помощью метода **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f3378-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="f3378-131">Чтобы изменить запись, используйте метод **Edit** для копирования содержимого текущей записи в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="f3378-131">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer.</span></span> <span data-ttu-id="f3378-132">Если сначала не вызвать метод **Edit**, то при использовании метода **Update** или попытке изменить значение поля возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="f3378-132">If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="f3378-133">В рабочей области ODBCDirect можно выполнять пакетное обновление, при условии что библиотека курсоров поддерживает его, а объект **Recordset** был открыт с использованием оптимистичной блокировки пакетных операций.</span><span class="sxs-lookup"><span data-stu-id="f3378-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="f3378-134">Если в рабочей области Microsoft Access для свойства **LockEdits** объекта **Recordset** задано значение **True** (пессимистичная блокировка) в многопользовательской среде, то запись останется заблокированной с момента вызова метода **Edit** до завершения выполнения метода **Update** или отмены изменения.</span><span class="sxs-lookup"><span data-stu-id="f3378-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="f3378-135">Если для свойства **LockEdits** задано значение **False** (оптимистичная блокировка), то запись блокируется и сравнивается с ее вариантом непосредственно перед обновлением в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f3378-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="f3378-136">Если запись изменилась с момента использования метода **Edit**, происходит сбой операции **Update**.</span><span class="sxs-lookup"><span data-stu-id="f3378-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="f3378-137">В базах данных ODBC, подключенных к ядру СУБД Microsoft Access, и устанавливаемых базах данных ISAM всегда используется оптимистичная блокировка.</span><span class="sxs-lookup"><span data-stu-id="f3378-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="f3378-138">Чтобы продолжить выполнение операции **Update** с вашими изменениями, снова вызовите метод **Update**.</span><span class="sxs-lookup"><span data-stu-id="f3378-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="f3378-139">Чтобы вернуть запись в состояние, оставленное другим пользователем, обновите текущую запись с помощью команды Move 0.</span><span class="sxs-lookup"><span data-stu-id="f3378-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="f3378-140">Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="f3378-140">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="f3378-141">В противном случае возникнет ошибка "Отказано в разрешении" (при вызове метода **AddNew**, **Delete** или **Edit** в рабочей области Microsoft Access) или ошибка "Недопустимый аргумент" (при вызове метода **Update** в рабочей области ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="f3378-141">If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


