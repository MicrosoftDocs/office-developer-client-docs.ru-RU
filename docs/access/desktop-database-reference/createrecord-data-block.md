---
title: Блок данных CreateRecord
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295354"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="0b970-102">Блок данных CreateRecord</span><span class="sxs-lookup"><span data-stu-id="0b970-102">CreateRecord data block</span></span>


<span data-ttu-id="0b970-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b970-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b970-104">Блок данных **CreateRecord можно использовать** для создания новой записи в указанной таблице.</span><span class="sxs-lookup"><span data-stu-id="0b970-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="0b970-105">Блок **данных CreateRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="0b970-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="0b970-106">Setting</span><span class="sxs-lookup"><span data-stu-id="0b970-106">Setting</span></span>

<span data-ttu-id="0b970-107">Блок **данных CreateRecord** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="0b970-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b970-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="0b970-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0b970-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0b970-109">Required</span></span></p></th>
<th><p><span data-ttu-id="0b970-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0b970-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b970-111"><strong>Создание записи</strong></span><span class="sxs-lookup"><span data-stu-id="0b970-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="0b970-112">Да</span><span class="sxs-lookup"><span data-stu-id="0b970-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="0b970-113">Имя таблицы для создания новой записи.</span><span class="sxs-lookup"><span data-stu-id="0b970-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b970-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="0b970-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="0b970-115">Нет</span><span class="sxs-lookup"><span data-stu-id="0b970-115">No</span></span></p></td>
<td><p><span data-ttu-id="0b970-116">Строка, идентифицирует запись.</span><span class="sxs-lookup"><span data-stu-id="0b970-116">An string that identifies the record.</span></span> <span data-ttu-id="0b970-117">Псевдоним записи можно использовать для идентификации</span><span class="sxs-lookup"><span data-stu-id="0b970-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0b970-118">Заметки</span><span class="sxs-lookup"><span data-stu-id="0b970-118">Remarks</span></span>

<span data-ttu-id="0b970-119">Запись, созданная **с помощью CreateRecord,** автоматически становится текущей записью.</span><span class="sxs-lookup"><span data-stu-id="0b970-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="0b970-120">После **записи CreateRecord** можно вставить блок команд, которые будут выполняться до того, как будет зафиксирована новая запись.</span><span class="sxs-lookup"><span data-stu-id="0b970-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="0b970-121">В блоке данных **CreateRecord** доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b970-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b970-122"><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="0b970-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b970-123"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="0b970-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b970-124"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="0b970-124"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b970-125"><a href="if-then-else-macro-block.md">If... Затем... Макрос Else</a></span><span class="sxs-lookup"><span data-stu-id="0b970-125"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b970-126"><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></span><span class="sxs-lookup"><span data-stu-id="0b970-126"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b970-127"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="0b970-127"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b970-128">После создания записи с помощью действия **CreateRecord** используйте действие **SetField,** чтобы указать значение поля в новой записи.</span><span class="sxs-lookup"><span data-stu-id="0b970-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="0b970-129">Вы можете использовать **if... Затем... Заявление Else** для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="0b970-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="0b970-130">Чтобы отменить создание записи, используйте действие **CancelRecordChange.**</span><span class="sxs-lookup"><span data-stu-id="0b970-130">To cancel the creation of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="0b970-131">Это предотвращает внесение изменений и выход из блока **данных CreateRecord.**</span><span class="sxs-lookup"><span data-stu-id="0b970-131">This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="0b970-132">После записи можно использовать локализованную переменную **LastCreateRecordIdentity** для работы с записью.</span><span class="sxs-lookup"><span data-stu-id="0b970-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="0b970-133">Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи.</span><span class="sxs-lookup"><span data-stu-id="0b970-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="0b970-134">Блок **данных CreateRecord** можно использовать только в макросах "После вставки", **[](after-insert-macro-event.md)** **["После](after-update-macro-event.md)** обновления" и **["После](after-update-macro-event.md)** обновления".</span><span class="sxs-lookup"><span data-stu-id="0b970-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

