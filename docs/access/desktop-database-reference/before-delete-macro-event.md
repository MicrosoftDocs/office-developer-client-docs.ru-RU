---
title: Before Delete Macro Event
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7863f8500a81014f3c70b5547fb363c46803f4f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482019"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="509d7-102">Before Delete Macro Event</span><span class="sxs-lookup"><span data-stu-id="509d7-102">Before Delete Macro Event</span></span>

<span data-ttu-id="509d7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="509d7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="509d7-104">**Прежде чем удалить** событие происходит при удалении записи, но перед сохранением изменений.</span><span class="sxs-lookup"><span data-stu-id="509d7-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="509d7-105">**Прежде чем удалить** событие доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="509d7-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="509d7-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="509d7-106">Remarks</span></span>

<span data-ttu-id="509d7-107">С помощью события **До удаления** для выполнения действий, которые следует выполнить перед записью удаляется.</span><span class="sxs-lookup"><span data-stu-id="509d7-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="509d7-108">**До изменения** обычно используется для выполнения проверки и повысить пользовательские сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="509d7-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="509d7-109">Можно получить доступ к значение записи, чтобы удалить с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="509d7-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="509d7-110">Например для доступа к значение поля QuantityInStock в записи для удаления, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="509d7-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="509d7-111">Значения, содержащиеся в записи к удалению удаляется без возможности восстановления при окончания события **До удаления** .</span><span class="sxs-lookup"><span data-stu-id="509d7-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="509d7-112">**Прежде чем удалить** событие можно отменить с помощью действия **RaiseError** .</span><span class="sxs-lookup"><span data-stu-id="509d7-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="509d7-113">Когда возникает ошибка, изменения, содержащиеся в событии **Прежде чем удалять** будут удалены.</span><span class="sxs-lookup"><span data-stu-id="509d7-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="509d7-114">В следующей таблице перечислены команды макросов, которые можно использовать в событии **До удаления** .</span><span class="sxs-lookup"><span data-stu-id="509d7-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="509d7-115">Тип команды</span><span class="sxs-lookup"><span data-stu-id="509d7-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="509d7-116">Команда</span><span class="sxs-lookup"><span data-stu-id="509d7-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="509d7-117">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="509d7-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="509d7-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="509d7-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="509d7-119">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="509d7-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="509d7-120"><a href="group-macro-statement.md">Group Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="509d7-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="509d7-121">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="509d7-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="509d7-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span><span class="sxs-lookup"><span data-stu-id="509d7-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="509d7-123">Блок данных</span><span class="sxs-lookup"><span data-stu-id="509d7-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="509d7-124"><a href="lookuprecord-data-block.md">Действия макрокомандой НайтиЗапись, после макроса</a></span><span class="sxs-lookup"><span data-stu-id="509d7-124"><a href="lookuprecord-data-block.md">LookupRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="509d7-125">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="509d7-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="509d7-126"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="509d7-126"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="509d7-127">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="509d7-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="509d7-128"><a href="onerror-macro-action.md">OnError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="509d7-128"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="509d7-129">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="509d7-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="509d7-130"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="509d7-130"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="509d7-131">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="509d7-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="509d7-132"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="509d7-132"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="509d7-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="509d7-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="509d7-134"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="509d7-134"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="509d7-135">Чтобы создать макрос данных, который захватывает событие **Прежде чем удалять** , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="509d7-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="509d7-136">Откройте таблицу для записи события **До удаления** .</span><span class="sxs-lookup"><span data-stu-id="509d7-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="509d7-137">На вкладке **таблицы** в группе **События перед** выберите **До удаления**.</span><span class="sxs-lookup"><span data-stu-id="509d7-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

