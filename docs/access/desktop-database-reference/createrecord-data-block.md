---
title: Блок данных CreateRecord
TOCTitle: CreateRecord Data Block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bda30265cbcf2377114734d03b16f889b0d165b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880819"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="fe53d-102">Блок данных CreateRecord</span><span class="sxs-lookup"><span data-stu-id="fe53d-102">CreateRecord Data Block</span></span>


<span data-ttu-id="fe53d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe53d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe53d-104">Блок данных **СоздатьЗапись** можно использовать для создания новой записи в указанную таблицу.</span><span class="sxs-lookup"><span data-stu-id="fe53d-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="fe53d-105">Блок данных **СоздатьЗапись** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="fe53d-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="fe53d-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="fe53d-106">Setting</span></span>

<span data-ttu-id="fe53d-107">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="fe53d-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe53d-108">Argument</span><span class="sxs-lookup"><span data-stu-id="fe53d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="fe53d-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fe53d-109">Required</span></span></p></th>
<th><p><span data-ttu-id="fe53d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fe53d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe53d-111"><strong>Создание записи в</strong></span><span class="sxs-lookup"><span data-stu-id="fe53d-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="fe53d-112">Да</span><span class="sxs-lookup"><span data-stu-id="fe53d-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="fe53d-113">Имя таблицы для создания новой записи в.</span><span class="sxs-lookup"><span data-stu-id="fe53d-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe53d-114"><strong>псевдоним;</strong></span><span class="sxs-lookup"><span data-stu-id="fe53d-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="fe53d-115">Нет</span><span class="sxs-lookup"><span data-stu-id="fe53d-115">No</span></span></p></td>
<td><p><span data-ttu-id="fe53d-116">Строка, идентифицирующая эту запись.</span><span class="sxs-lookup"><span data-stu-id="fe53d-116">An string that identifies the record.</span></span> <span data-ttu-id="fe53d-117">Можно использовать эту запись псевдонима для идентификации</span><span class="sxs-lookup"><span data-stu-id="fe53d-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fe53d-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe53d-118">Remarks</span></span>

<span data-ttu-id="fe53d-119">Записи, созданной **СоздатьЗапись** автоматически становится текущей.</span><span class="sxs-lookup"><span data-stu-id="fe53d-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="fe53d-120">После оператора **СоздатьЗапись** можно вставить блок команды, которые будут выполняться перед сохранением новую запись.</span><span class="sxs-lookup"><span data-stu-id="fe53d-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="fe53d-121">В блоке данных **СоздатьЗапись** доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe53d-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe53d-122"><a href="cancelrecordchange-macro-action.md">Действия макроса CancelRecordChange</a></span><span class="sxs-lookup"><span data-stu-id="fe53d-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe53d-123"><a href="comment-macro-statement.md">Оператор комментария макросов</a></span><span class="sxs-lookup"><span data-stu-id="fe53d-123"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe53d-124"><a href="group-macro-statement.md">Оператор группы макросов</a></span><span class="sxs-lookup"><span data-stu-id="fe53d-124"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe53d-125"><a href="if-then-else-macro-block.md">If... Затем... Оператор Else макросов</a></span><span class="sxs-lookup"><span data-stu-id="fe53d-125"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe53d-126"><a href="setfield-macro-action.md">Действия SetField макроса</a></span><span class="sxs-lookup"><span data-stu-id="fe53d-126"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe53d-127"><a href="setlocalvar-macro-action.md">Действия макроса SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="fe53d-127"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe53d-128">После **СоздатьЗапись** действие создает запись, используйте действие **SetField** для указания значения поля в новую запись.</span><span class="sxs-lookup"><span data-stu-id="fe53d-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="fe53d-129">**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="fe53d-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="fe53d-130">Чтобы отменить создание записи, используйте действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="fe53d-130">To cancel the creation of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="fe53d-131">Это предотвращает фиксации изменений и выполняет выход из блока **СоздатьЗапись** данных.</span><span class="sxs-lookup"><span data-stu-id="fe53d-131">This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="fe53d-132">После фиксации новую запись локальной переменной **LastCreateRecordIdentity** можно использовать для работы с записью.</span><span class="sxs-lookup"><span data-stu-id="fe53d-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="fe53d-133">Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи.</span><span class="sxs-lookup"><span data-stu-id="fe53d-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="fe53d-134">Блок данных **СоздатьЗапись** можно использовать только **[После вставки](after-insert-macro-event.md)**, **[После обновления](after-update-macro-event.md)** и событий макрос данных **[После обновления](after-update-macro-event.md)** .</span><span class="sxs-lookup"><span data-stu-id="fe53d-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

