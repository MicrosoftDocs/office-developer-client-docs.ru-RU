---
title: Блок данных EditRecord
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ddfbbf21e62d5967fa1f2f31bab0222664eb39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293597"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="51fa2-102">Блок данных EditRecord</span><span class="sxs-lookup"><span data-stu-id="51fa2-102">EditRecord data block</span></span>

<span data-ttu-id="51fa2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51fa2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51fa2-104">Блок данных **EditRecord можно** использовать для изменения значений, содержащихся в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="51fa2-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="51fa2-105">Блок **данных EditRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="51fa2-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="51fa2-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="51fa2-106">Setting</span></span>

<span data-ttu-id="51fa2-107">Блок **данных EditRecord** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="51fa2-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51fa2-108">Аргументация</span><span class="sxs-lookup"><span data-stu-id="51fa2-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="51fa2-109">Description</span><span class="sxs-lookup"><span data-stu-id="51fa2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51fa2-110"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="51fa2-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="51fa2-111">Строка, идентифицируемая для редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="51fa2-111">A string that identifies the record to edit.</span></span> <span data-ttu-id="51fa2-112">Если аргумент <em>Alias</em> не указан, то текущая запись редактирована.</span><span class="sxs-lookup"><span data-stu-id="51fa2-112">If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="51fa2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="51fa2-113">Remarks</span></span>

<span data-ttu-id="51fa2-114">После **заявления EditRecord** можно вставить блок команд, которые будут выполняться до того, как изменения в записи будут запятнаными.</span><span class="sxs-lookup"><span data-stu-id="51fa2-114">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted.</span></span> <span data-ttu-id="51fa2-115">Следующие действия доступны в блоке **данных EditRecord.**</span><span class="sxs-lookup"><span data-stu-id="51fa2-115">The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51fa2-116"><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="51fa2-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fa2-117"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="51fa2-117"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fa2-118"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="51fa2-118"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fa2-119"><a href="if-then-else-macro-block.md">Если... Затем... Else macro statement</a></span><span class="sxs-lookup"><span data-stu-id="51fa2-119"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fa2-120"><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></span><span class="sxs-lookup"><span data-stu-id="51fa2-120"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fa2-121"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="51fa2-121"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="51fa2-122">Используйте действие **SetField,** чтобы указать новые значения поля в отредактируемой записи.</span><span class="sxs-lookup"><span data-stu-id="51fa2-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="51fa2-123">Вы можете использовать **if... Затем... Другое** заявление для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="51fa2-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="51fa2-124">Чтобы отменить редактирование записи, используйте **действие CancelRecordChange.**</span><span class="sxs-lookup"><span data-stu-id="51fa2-124">To cancel the editing of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="51fa2-125">Это предотвращает совершение изменений и выход из блока **данных EditRecord.**</span><span class="sxs-lookup"><span data-stu-id="51fa2-125">This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="51fa2-126">Для работы с последней записью, созданной в блоке данных CreateRecord, можно использовать локализованную переменную **LastCreateRecordIdentity.** </span><span class="sxs-lookup"><span data-stu-id="51fa2-126">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="51fa2-127">Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи:</span><span class="sxs-lookup"><span data-stu-id="51fa2-127">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="51fa2-128">Блок данных CreateRecord можно использовать только в **[](after-update-macro-event.md)** событиях **[](after-update-macro-event.md)** макрос данных После вставки, **[](after-insert-macro-event.md)** после обновления и после обновления макрос данных.</span><span class="sxs-lookup"><span data-stu-id="51fa2-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

