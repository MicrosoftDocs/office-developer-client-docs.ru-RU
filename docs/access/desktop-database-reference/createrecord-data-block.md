---
title: Блок данных СоздатьЗапись
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719821"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="20a6c-102">Блок данных СоздатьЗапись</span><span class="sxs-lookup"><span data-stu-id="20a6c-102">CreateRecord data block</span></span>


<span data-ttu-id="20a6c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20a6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20a6c-104">Блок данных **СоздатьЗапись** можно использовать для создания новой записи в указанную таблицу.</span><span class="sxs-lookup"><span data-stu-id="20a6c-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="20a6c-105">Блок данных **СоздатьЗапись** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="20a6c-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="20a6c-106">Setting</span><span class="sxs-lookup"><span data-stu-id="20a6c-106">Setting</span></span>

<span data-ttu-id="20a6c-107">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="20a6c-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20a6c-108">Argument</span><span class="sxs-lookup"><span data-stu-id="20a6c-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="20a6c-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="20a6c-109">Required</span></span></p></th>
<th><p><span data-ttu-id="20a6c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="20a6c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20a6c-111"><strong>Создание записи в</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-112">Да</span><span class="sxs-lookup"><span data-stu-id="20a6c-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="20a6c-113">Имя таблицы для создания новой записи в.</span><span class="sxs-lookup"><span data-stu-id="20a6c-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20a6c-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-115">Нет</span><span class="sxs-lookup"><span data-stu-id="20a6c-115">No</span></span></p></td>
<td><p><span data-ttu-id="20a6c-116">Строка, идентифицирующая эту запись.</span><span class="sxs-lookup"><span data-stu-id="20a6c-116">An string that identifies the record.</span></span> <span data-ttu-id="20a6c-117">Можно использовать эту запись псевдонима для идентификации</span><span class="sxs-lookup"><span data-stu-id="20a6c-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="20a6c-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="20a6c-118">Remarks</span></span>

<span data-ttu-id="20a6c-119">Записи, созданной **СоздатьЗапись** автоматически становится текущей.</span><span class="sxs-lookup"><span data-stu-id="20a6c-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="20a6c-120">После оператора **СоздатьЗапись** можно вставить блок команды, которые будут выполняться перед сохранением новую запись.</span><span class="sxs-lookup"><span data-stu-id="20a6c-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="20a6c-121">В блоке данных **СоздатьЗапись** доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="20a6c-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20a6c-122"><a href="cancelrecordchange-macro-action.md">Макрокоманда CancelRecordChange</a></span><span class="sxs-lookup"><span data-stu-id="20a6c-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20a6c-123"><a href="comment-macro-statement.md">Оператор макроса Comment</a></span><span class="sxs-lookup"><span data-stu-id="20a6c-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20a6c-124"><a href="group-macro-statement.md">Оператор макроса Group</a></span><span class="sxs-lookup"><span data-stu-id="20a6c-124"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20a6c-125"><a href="if-then-else-macro-block.md">If... Затем... Оператор Else макросов</a></span><span class="sxs-lookup"><span data-stu-id="20a6c-125"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20a6c-126"><a href="setfield-macro-action.md">Макрокоманда SetField</a></span><span class="sxs-lookup"><span data-stu-id="20a6c-126"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20a6c-127"><a href="setlocalvar-macro-action.md">Макрокоманда SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="20a6c-127"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="20a6c-128">После **СоздатьЗапись** действие создает запись, используйте действие **SetField** для указания значения поля в новую запись.</span><span class="sxs-lookup"><span data-stu-id="20a6c-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="20a6c-129">**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="20a6c-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="20a6c-130">Чтобы отменить создание записи, используйте действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="20a6c-130">To cancel the creation of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="20a6c-131">Это предотвращает фиксации изменений и выполняет выход из блока **СоздатьЗапись** данных.</span><span class="sxs-lookup"><span data-stu-id="20a6c-131">This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="20a6c-132">После фиксации новую запись локальной переменной **LastCreateRecordIdentity** можно использовать для работы с записью.</span><span class="sxs-lookup"><span data-stu-id="20a6c-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="20a6c-133">Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи.</span><span class="sxs-lookup"><span data-stu-id="20a6c-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="20a6c-134">Блок данных **СоздатьЗапись** можно использовать только **[После вставки](after-insert-macro-event.md)**, **[После обновления](after-update-macro-event.md)** и событий макрос данных **[После обновления](after-update-macro-event.md)** .</span><span class="sxs-lookup"><span data-stu-id="20a6c-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

