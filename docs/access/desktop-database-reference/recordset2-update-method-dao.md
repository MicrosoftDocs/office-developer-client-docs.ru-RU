---
title: Recordset2.Update Method (DAO)
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
ms.openlocfilehash: 47c97e7f38f05e14bcae457a66c92b87d50844fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483129"
---
# <a name="recordset2update-method-dao"></a><span data-ttu-id="b739d-102">Recordset2.Update Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="b739d-102">Recordset2.Update Method (DAO)</span></span>


<span data-ttu-id="b739d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b739d-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="b739d-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b739d-104">Syntax</span></span>

<span data-ttu-id="b739d-105">*выражение* . Обновление (***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="b739d-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="b739d-106">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b739d-106">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b739d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b739d-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b739d-108">Имя</span><span class="sxs-lookup"><span data-stu-id="b739d-108">Name</span></span></p></th>
<th><p><span data-ttu-id="b739d-109">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="b739d-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b739d-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b739d-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b739d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b739d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b739d-112">UpdateType</span><span class="sxs-lookup"><span data-stu-id="b739d-112">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="b739d-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b739d-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="b739d-114"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="b739d-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b739d-115"><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> константу, указывающую тип обновления, как указано в настройки (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="b739d-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b739d-116">Force</span><span class="sxs-lookup"><span data-stu-id="b739d-116">Force</span></span></p></td>
<td><p><span data-ttu-id="b739d-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b739d-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="b739d-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="b739d-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="b739d-119"><strong>Логическое</strong> значение, указывающее ли принудительно изменения в базу данных, вне зависимости от ли данным был изменен другим пользователем <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Удалить</a></strong>, или <strong><a href="recordset2-edit-method-dao.md">Изменение</a></strong> звонок.</span><span class="sxs-lookup"><span data-stu-id="b739d-119">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call.</span></span> <span data-ttu-id="b739d-120">Если <strong>значение True</strong>, принудительно изменений и изменения, внесенные другими пользователями, просто будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="b739d-120">If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten.</span></span> <span data-ttu-id="b739d-121">Если <strong>значение False</strong> (по умолчанию), изменения, внесенные другим пользователем до обновления будет отображено сбоя для эти изменения, которые находятся в конфликта обновления.</span><span class="sxs-lookup"><span data-stu-id="b739d-121">If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict.</span></span> <span data-ttu-id="b739d-122">Ошибка не происходит, но свойства <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> и <strong>BatchCollisions</strong> будут указывать числа конфликтов и строк, затронутых конфликтов, соответственно (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="b739d-122">No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b739d-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="b739d-123">Remarks</span></span>

<span data-ttu-id="b739d-124">Для сохранения текущей записи и все изменения, внесенные в нее выполните **обновление** .</span><span class="sxs-lookup"><span data-stu-id="b739d-124">Use **Update** to save the current record and any changes you've made to it.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="b739d-125">Изменения в текущей записи не сохраняются, если:</span><span class="sxs-lookup"><span data-stu-id="b739d-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="b739d-126">Используйте метод **AddNew** или **Изменить** и затем перетащить в другой записи без предварительного **обновления**.</span><span class="sxs-lookup"><span data-stu-id="b739d-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="b739d-127">С помощью **AddNew**или **Изменить** и затем с помощью **изменения** или использованием **AddNew** еще раз без предварительного **обновления**.</span><span class="sxs-lookup"><span data-stu-id="b739d-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="b739d-128">Присвойте свойству **[закладку](recordset2-bookmark-property-dao.md)** к другой записи.</span><span class="sxs-lookup"><span data-stu-id="b739d-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="b739d-129">Закройте **записей** без предварительного **обновления**.</span><span class="sxs-lookup"><span data-stu-id="b739d-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="b739d-130">Отменить операцию **редактирования** с помощью **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b739d-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="b739d-131">Чтобы изменить запись, используйте метод **Изменить** чтобы скопировать содержимое текущей записи в буфер копирования.</span><span class="sxs-lookup"><span data-stu-id="b739d-131">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer.</span></span> <span data-ttu-id="b739d-132">Если вы не используете **Изменение** сначала, возникает ошибка при использовании **обновления** или предпринята попытка изменить значение поля.</span><span class="sxs-lookup"><span data-stu-id="b739d-132">If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="b739d-133">В рабочей области технология ODBCDirect, можно сделать пакета обновления, предоставляемые библиотека курсора поддерживает пакетные обновления и **записей** было открыто с помощью пакета оптимистичный блокировки параметр.</span><span class="sxs-lookup"><span data-stu-id="b739d-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="b739d-134">В рабочей области Microsoft Access когда объекта **набора записей** **LockEdits** задается **значение True** (pessimistically заблокирован) в многопользовательской среде запись остается заблокированным с момента **Изменение** используется до \*\* Обновление\*\* метода или изменение отменяется.</span><span class="sxs-lookup"><span data-stu-id="b739d-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="b739d-135">Если значение свойства **LockEdits** равно **False** (оптимистичном случае заблокирован), запись блокируется и по сравнению с предварительно измененной записи непосредственно перед обновляется в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b739d-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="b739d-136">Если запись была изменена используется метод **изменения** , происходит сбой операции **обновления** .</span><span class="sxs-lookup"><span data-stu-id="b739d-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="b739d-137">Базы данных Microsoft Access модуль подключения ODBC и устанавливаемый драйвер ISAM баз данных всегда использовать оптимистичный блокировки.</span><span class="sxs-lookup"><span data-stu-id="b739d-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="b739d-138">Чтобы продолжить операцию **обновления** внесенными изменениями, используйте метод **обновления** еще раз.</span><span class="sxs-lookup"><span data-stu-id="b739d-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="b739d-139">Вернуться к записи другого пользователя изменен, необходимо обновить текущей записи с помощью перемещения 0.</span><span class="sxs-lookup"><span data-stu-id="b739d-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>


> [!NOTE]
> <span data-ttu-id="b739d-140">Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="b739d-140">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="b739d-141">Если нет, произойдет ошибка «Отказано в разрешении» на **AddNew**, **Удаление**или **Изменение** вызова метода в рабочей области Microsoft Access или приведет к возникновению ошибки «Недопустимый аргумент» при вызове **Update** в рабочей области технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="b739d-141">If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


