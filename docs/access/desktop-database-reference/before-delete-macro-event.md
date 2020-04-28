---
title: Событие макроса Before Delete
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296915"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="db07f-102">Событие макроса Before Delete</span><span class="sxs-lookup"><span data-stu-id="db07f-102">Before Delete macro event</span></span>

<span data-ttu-id="db07f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db07f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db07f-104">Событие **перед удалением** возникает при удалении записи, но до фиксации изменения.</span><span class="sxs-lookup"><span data-stu-id="db07f-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="db07f-105">Событие " **перед удалением** " доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="db07f-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="db07f-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="db07f-106">Remarks</span></span>

<span data-ttu-id="db07f-107">Используйте событие **перед удалением** для выполнения действий, которые должны выполняться перед удалением записи.</span><span class="sxs-lookup"><span data-stu-id="db07f-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="db07f-108">Для выполнения проверки и порождения настраиваемых сообщений об ошибках обычно используется значение **Before Change** .</span><span class="sxs-lookup"><span data-stu-id="db07f-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="db07f-109">Можно получить доступ к значению в записи, которую необходимо удалить, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="db07f-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="db07f-110">Например, чтобы получить доступ к значению поля Куантитинстокк в удаляемой записи, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="db07f-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="db07f-111">Значения, которые хранятся в удаляемой записи, удаляются навсегда при завершении события **перед удалением** .</span><span class="sxs-lookup"><span data-stu-id="db07f-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="db07f-112">Вы можете отменить событие " **перед удалением** " с помощью действия **раисиррор** .</span><span class="sxs-lookup"><span data-stu-id="db07f-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="db07f-113">При возникновении ошибки изменения, которые включены в событие **before delete** , отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="db07f-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="db07f-114">В следующей таблице перечислены команды макросов, которые можно использовать в событии **перед удалением** .</span><span class="sxs-lookup"><span data-stu-id="db07f-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db07f-115">Тип команды</span><span class="sxs-lookup"><span data-stu-id="db07f-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="db07f-116">Команда</span><span class="sxs-lookup"><span data-stu-id="db07f-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db07f-117">Управление</span><span class="sxs-lookup"><span data-stu-id="db07f-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="db07f-118"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="db07f-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db07f-119">Управление</span><span class="sxs-lookup"><span data-stu-id="db07f-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="db07f-120"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="db07f-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db07f-121">Управление</span><span class="sxs-lookup"><span data-stu-id="db07f-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="db07f-122"><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></span><span class="sxs-lookup"><span data-stu-id="db07f-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db07f-123">Блок данных</span><span class="sxs-lookup"><span data-stu-id="db07f-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="db07f-124"><a href="lookuprecord-data-block.md">Макрокоманда LookupRecord</a></span><span class="sxs-lookup"><span data-stu-id="db07f-124"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db07f-125">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="db07f-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="db07f-126"><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></span><span class="sxs-lookup"><span data-stu-id="db07f-126"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db07f-127">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="db07f-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="db07f-128"><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></span><span class="sxs-lookup"><span data-stu-id="db07f-128"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db07f-129">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="db07f-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="db07f-130"><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></span><span class="sxs-lookup"><span data-stu-id="db07f-130"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db07f-131">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="db07f-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="db07f-132"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="db07f-132"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db07f-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="db07f-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="db07f-134"><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></span><span class="sxs-lookup"><span data-stu-id="db07f-134"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db07f-135">Чтобы создать макрос данных, захватывающий событие **перед удалением** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="db07f-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="db07f-136">Откройте таблицу, для которой необходимо записать событие **перед удалением** .</span><span class="sxs-lookup"><span data-stu-id="db07f-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="db07f-137">На вкладке **Таблица** в группе **события перед** **удалением выберите перед удалением**.</span><span class="sxs-lookup"><span data-stu-id="db07f-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

