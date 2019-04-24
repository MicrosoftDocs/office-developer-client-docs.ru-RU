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
# <a name="recordset2update-method-dao"></a><span data-ttu-id="c8c6c-102">Метод Recordset2. Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="c8c6c-102">Recordset2.Update method (DAO)</span></span>

<span data-ttu-id="c8c6c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8c6c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c6c-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8c6c-104">Syntax</span></span>

<span data-ttu-id="c8c6c-105">*Expression* . Обновление (***упдатетипе***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="c8c6c-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="c8c6c-106">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="c8c6c-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8c6c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8c6c-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8c6c-108">Имя</span><span class="sxs-lookup"><span data-stu-id="c8c6c-108">Name</span></span></p></th>
<th><p><span data-ttu-id="c8c6c-109">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="c8c6c-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c8c6c-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c8c6c-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="c8c6c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c8c6c-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8c6c-112"><em>Упдатетипе</em></span><span class="sxs-lookup"><span data-stu-id="c8c6c-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="c8c6c-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c8c6c-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="c8c6c-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="c8c6c-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="c8c6c-115">Константа <strong><a href="updatetypeenum-enumeration-dao.md">упдатетипинум</a></strong> , указывающая тип обновления, как указано в разделе Параметры (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="c8c6c-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8c6c-116"><em>Force</em></span><span class="sxs-lookup"><span data-stu-id="c8c6c-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="c8c6c-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c8c6c-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="c8c6c-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="c8c6c-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="c8c6c-119"><strong>Логическое</strong> значение, указывающее, следует ли принудительно вносить изменения в базу данных независимо от того, были ли базовые данные изменены другим пользователем с момента вызова <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>или <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="c8c6c-119">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call.</span></span> <span data-ttu-id="c8c6c-120">Если этот параметр <strong>имеет значение true</strong>, изменения принудительны, а изменения, внесенные другими пользователями, просто перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-120">If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten.</span></span> <span data-ttu-id="c8c6c-121">Если задано <strong>значение false</strong> (по умолчанию), изменения, внесенные другим пользователем во время выполнения обновления, приведут к сбою обновления для тех изменений, которые конфликтуют.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-121">If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict.</span></span> <span data-ttu-id="c8c6c-122">Ошибка не возникает, но свойства <strong><a href="recordset-batchcollisioncount-property-dao.md">батчколлисионкаунт</a></strong> и <strong>батчколлисионс</strong> будут указывать количество конфликтов и строк, затрагиваемых конфликтами соответственно (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="c8c6c-122">No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c8c6c-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="c8c6c-123">Remarks</span></span>

<span data-ttu-id="c8c6c-124">Используйте **Update** , чтобы сохранить текущую запись и все изменения, внесенные в нее.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8c6c-125">Изменения в текущей записи теряются, если:</span><span class="sxs-lookup"><span data-stu-id="c8c6c-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="c8c6c-126">Используйте метод **Edit** или **AddNew** , а затем переходите к другой записи, не используя сначала **Обновление**.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="c8c6c-127">Используйте команду **изменить** или \*\*\*\* выполнить, а затем снова выполните команду **Edit** или **AddNew** , не используя **Обновление**.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="c8c6c-128">Свойство **[Bookmark](recordset2-bookmark-property-dao.md)** задается для другой записи.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="c8c6c-129">Закрывается **набор записей** без предварительного **обновления**.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="c8c6c-130">Вы отменили операцию **редактирования** с помощью **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="c8c6c-131">Чтобы изменить запись, используйте метод **Edit** , чтобы скопировать содержимое текущей записи в буфер копирования.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-131">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer.</span></span> <span data-ttu-id="c8c6c-132">Если вы не используете **Edit** First, то при использовании **обновления** или попытке изменить значение поля возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-132">If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="c8c6c-133">В рабочей области ODBCDirect можно выполнить пакетные обновления, при условии, что библиотека курсоров поддерживает пакетные обновления, а **набор записей** был открыт с помощью параметра "Оптимистическая блокировка пакетов".</span><span class="sxs-lookup"><span data-stu-id="c8c6c-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="c8c6c-134">Если в рабочей области Microsoft Access для свойства **LockEdits** объекта **Recordset** задано **значение true** (пессимистикалли заблокировано) в многопользовательской среде, то запись остается заблокированной при **изменении** времени до \*\* Метод Update\*\* выполняется, или редактирование отменено.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="c8c6c-135">Если для свойства **LockEdits** задано **значение false** (оптимистикалли заблокировано), запись блокируется и сравнивается с предварительно измененной записью непосредственно перед ее обновлением в базе данных.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="c8c6c-136">Если после использования метода **Edit** запись изменилась, операция **обновления** завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="c8c6c-137">ODBC и устанавливаемые базы данных ISAM, подключенные к ядру СУБД Microsoft Access, всегда используют оптимистическую блокировку.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="c8c6c-138">Чтобы продолжить операцию **обновления** с внесенными изменениями, снова используйте метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="c8c6c-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="c8c6c-139">Чтобы вернуться к записи, когда она была изменена другим пользователем, обновите текущую запись с помощью перемещения 0.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c6c-140">Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="c8c6c-140">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="c8c6c-141">В противном случае при вызове метода **AddNew**, **Delete**или **Edit** в рабочей области Microsoft Access возникнет ошибка "отказано в разрешении", или при вызове **обновления** в рабочей области ODBCDirect произойдет ошибка "Недопустимый аргумент".</span><span class="sxs-lookup"><span data-stu-id="c8c6c-141">If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


