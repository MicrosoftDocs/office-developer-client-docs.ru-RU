---
title: EditRecord Data Block
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07763e32e0f8687816dc39298f91733ca814d275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479802"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="aa7ce-102">EditRecord Data Block</span><span class="sxs-lookup"><span data-stu-id="aa7ce-102">EditRecord Data Block</span></span>

<span data-ttu-id="aa7ce-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa7ce-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aa7ce-104">Чтобы изменить значения, содержащиеся в существующей записи можно использовать блок данных **ИзменитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="aa7ce-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="aa7ce-105">Блок данных **ИзменитьЗапись** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="aa7ce-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="aa7ce-106">Setting</span></span>

<span data-ttu-id="aa7ce-107">Блок данных **ИзменитьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa7ce-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="aa7ce-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="aa7ce-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aa7ce-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa7ce-110"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="aa7ce-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="aa7ce-111">Строка, идентифицирующая записи для редактирования.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-111">A string that identifies the record to edit.</span></span> <span data-ttu-id="aa7ce-112">Если аргумент <em>псевдоним</em> не задан, изменяется текущей записи.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-112">If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="aa7ce-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="aa7ce-113">Remarks</span></span>

<span data-ttu-id="aa7ce-114">После оператора **ИзменитьЗапись** можно вставить блок команды, которые будут выполняться перед comitted изменений в запись.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-114">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted.</span></span> <span data-ttu-id="aa7ce-115">В блоке данных **ИзменитьЗапись** доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-115">The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa7ce-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="aa7ce-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa7ce-117"><a href="comment-macro-statement.md">Comment Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="aa7ce-117"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa7ce-118"><a href="group-macro-statement.md">Group Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="aa7ce-118"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa7ce-119"><a href="if-then-else-macro-block.md">If... Затем... Оператор Else макросов</a></span><span class="sxs-lookup"><span data-stu-id="aa7ce-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa7ce-120"><a href="setfield-macro-action.md">SetField Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="aa7ce-120"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa7ce-121"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="aa7ce-121"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aa7ce-122">Действие **SetField** используется для указания нового значения поля в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="aa7ce-123">**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="aa7ce-124">Чтобы отменить редактирование записи, используйте действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="aa7ce-124">To cancel the editing of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="aa7ce-125">Это предотвращает фиксации изменений и выполняет выход из блока данных **ИзменитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="aa7ce-125">This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="aa7ce-126">Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="aa7ce-126">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="aa7ce-127">Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи:</span><span class="sxs-lookup"><span data-stu-id="aa7ce-127">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="aa7ce-128">Блок данных СоздатьЗапись можно использовать только **[После вставки](after-insert-macro-event.md)**, **[После обновления](after-update-macro-event.md)** и событий макрос данных **[После обновления](after-update-macro-event.md)** .</span><span class="sxs-lookup"><span data-stu-id="aa7ce-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

