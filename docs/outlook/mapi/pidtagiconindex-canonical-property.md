---
title: Каноническое свойство PidTagIconIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346622"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="7cdaa-103">Каноническое свойство PidTagIconIndex</span><span class="sxs-lookup"><span data-stu-id="7cdaa-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="7cdaa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cdaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cdaa-105">Содержит номер, который указывает, какой значок следует использовать при отобраив группу объектов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7cdaa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7cdaa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7cdaa-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="7cdaa-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="7cdaa-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7cdaa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7cdaa-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="7cdaa-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="7cdaa-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7cdaa-110">Data type:</span></span>  <br/> |<span data-ttu-id="7cdaa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7cdaa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7cdaa-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7cdaa-112">Area:</span></span>  <br/> |<span data-ttu-id="7cdaa-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="7cdaa-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cdaa-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7cdaa-114">Remarks</span></span>

<span data-ttu-id="7cdaa-115">Это свойство, если оно существует, является подсказкой для клиента.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="7cdaa-116">Клиент может игнорировать значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="7cdaa-117">**Состояние элемента почты**</span><span class="sxs-lookup"><span data-stu-id="7cdaa-117">**Mail item state**</span></span>|<span data-ttu-id="7cdaa-118">**Индекс icon**</span><span class="sxs-lookup"><span data-stu-id="7cdaa-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7cdaa-119">Новая почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-119">New mail</span></span>  <br/> |<span data-ttu-id="7cdaa-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="7cdaa-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="7cdaa-121">Запись</span><span class="sxs-lookup"><span data-stu-id="7cdaa-121">Post</span></span>  <br/> |<span data-ttu-id="7cdaa-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7cdaa-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="7cdaa-123">Другое</span><span class="sxs-lookup"><span data-stu-id="7cdaa-123">Other</span></span>  <br/> |<span data-ttu-id="7cdaa-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7cdaa-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="7cdaa-125">Чтение почты</span><span class="sxs-lookup"><span data-stu-id="7cdaa-125">Read mail</span></span>  <br/> |<span data-ttu-id="7cdaa-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="7cdaa-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="7cdaa-127">Нечитаемая почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-127">Unread mail</span></span>  <br/> |<span data-ttu-id="7cdaa-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="7cdaa-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="7cdaa-129">Отправленная почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="7cdaa-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="7cdaa-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="7cdaa-131">Неавентная почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="7cdaa-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="7cdaa-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="7cdaa-133">Почта получения</span><span class="sxs-lookup"><span data-stu-id="7cdaa-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="7cdaa-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="7cdaa-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="7cdaa-135">Ответная почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-135">Replied mail</span></span>  <br/> |<span data-ttu-id="7cdaa-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="7cdaa-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="7cdaa-137">Пересылаемая почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="7cdaa-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="7cdaa-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="7cdaa-139">Удаленная почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-139">Remote mail</span></span>  <br/> |<span data-ttu-id="7cdaa-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="7cdaa-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="7cdaa-141">Почта доставки</span><span class="sxs-lookup"><span data-stu-id="7cdaa-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="7cdaa-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="7cdaa-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="7cdaa-143">Чтение почты</span><span class="sxs-lookup"><span data-stu-id="7cdaa-143">Read mail</span></span>  <br/> |<span data-ttu-id="7cdaa-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="7cdaa-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="7cdaa-145">Почта nondelivery</span><span class="sxs-lookup"><span data-stu-id="7cdaa-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="7cdaa-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="7cdaa-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="7cdaa-147">Нечитаемая почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="7cdaa-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="7cdaa-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="7cdaa-149">Recall_S почты</span><span class="sxs-lookup"><span data-stu-id="7cdaa-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="7cdaa-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="7cdaa-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="7cdaa-151">Recall_F почты</span><span class="sxs-lookup"><span data-stu-id="7cdaa-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="7cdaa-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="7cdaa-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="7cdaa-153">Отслеживание почты</span><span class="sxs-lookup"><span data-stu-id="7cdaa-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="7cdaa-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="7cdaa-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="7cdaa-155">Вне почтовой почты</span><span class="sxs-lookup"><span data-stu-id="7cdaa-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="7cdaa-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="7cdaa-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="7cdaa-157">Отзыв почты</span><span class="sxs-lookup"><span data-stu-id="7cdaa-157">Recall mail</span></span>  <br/> |<span data-ttu-id="7cdaa-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="7cdaa-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="7cdaa-159">Отслеживаемая почта</span><span class="sxs-lookup"><span data-stu-id="7cdaa-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="7cdaa-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="7cdaa-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="7cdaa-161">Contact</span><span class="sxs-lookup"><span data-stu-id="7cdaa-161">Contact</span></span>  <br/> |<span data-ttu-id="7cdaa-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="7cdaa-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="7cdaa-163">Список рассылки</span><span class="sxs-lookup"><span data-stu-id="7cdaa-163">Distribution list</span></span>  <br/> |<span data-ttu-id="7cdaa-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="7cdaa-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="7cdaa-165">Липкий синий примечание</span><span class="sxs-lookup"><span data-stu-id="7cdaa-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="7cdaa-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="7cdaa-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="7cdaa-167">Липкий зеленый примечание</span><span class="sxs-lookup"><span data-stu-id="7cdaa-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="7cdaa-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="7cdaa-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="7cdaa-169">Липкий примечание розовый</span><span class="sxs-lookup"><span data-stu-id="7cdaa-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="7cdaa-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="7cdaa-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="7cdaa-171">Липкий желтый примечание</span><span class="sxs-lookup"><span data-stu-id="7cdaa-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="7cdaa-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="7cdaa-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="7cdaa-173">Липкий белый примечание</span><span class="sxs-lookup"><span data-stu-id="7cdaa-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="7cdaa-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="7cdaa-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="7cdaa-175">Назначение одного экземпляра</span><span class="sxs-lookup"><span data-stu-id="7cdaa-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="7cdaa-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="7cdaa-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="7cdaa-177">Повторяющиеся встречи</span><span class="sxs-lookup"><span data-stu-id="7cdaa-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="7cdaa-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="7cdaa-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="7cdaa-179">Собрание одного экземпляра</span><span class="sxs-lookup"><span data-stu-id="7cdaa-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="7cdaa-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="7cdaa-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="7cdaa-181">Повторяющееся собрание.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="7cdaa-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="7cdaa-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="7cdaa-183">Запрос на собрание</span><span class="sxs-lookup"><span data-stu-id="7cdaa-183">Meeting request</span></span>  <br/> |<span data-ttu-id="7cdaa-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="7cdaa-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="7cdaa-185">Accept</span><span class="sxs-lookup"><span data-stu-id="7cdaa-185">Accept</span></span>  <br/> |<span data-ttu-id="7cdaa-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="7cdaa-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="7cdaa-187">Отклонение</span><span class="sxs-lookup"><span data-stu-id="7cdaa-187">Decline</span></span>  <br/> |<span data-ttu-id="7cdaa-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="7cdaa-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="7cdaa-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="7cdaa-189">Tentativly</span></span>  <br/> |<span data-ttu-id="7cdaa-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="7cdaa-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="7cdaa-191">Отмена</span><span class="sxs-lookup"><span data-stu-id="7cdaa-191">Cancellation</span></span>  <br/> |<span data-ttu-id="7cdaa-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="7cdaa-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="7cdaa-193">Информационное обновление</span><span class="sxs-lookup"><span data-stu-id="7cdaa-193">Informational update</span></span>  <br/> |<span data-ttu-id="7cdaa-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="7cdaa-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="7cdaa-195">Задача/задача</span><span class="sxs-lookup"><span data-stu-id="7cdaa-195">Task/task</span></span>  <br/> |<span data-ttu-id="7cdaa-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="7cdaa-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="7cdaa-197">Не назначенная повторяемая задача</span><span class="sxs-lookup"><span data-stu-id="7cdaa-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="7cdaa-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="7cdaa-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="7cdaa-199">Задача assignee</span><span class="sxs-lookup"><span data-stu-id="7cdaa-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="7cdaa-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="7cdaa-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="7cdaa-201">Задача назначитель</span><span class="sxs-lookup"><span data-stu-id="7cdaa-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="7cdaa-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="7cdaa-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="7cdaa-203">Поручение</span><span class="sxs-lookup"><span data-stu-id="7cdaa-203">Task request</span></span>  <br/> |<span data-ttu-id="7cdaa-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="7cdaa-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="7cdaa-205">Принятие задач</span><span class="sxs-lookup"><span data-stu-id="7cdaa-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="7cdaa-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="7cdaa-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="7cdaa-207">Отклонение задачи</span><span class="sxs-lookup"><span data-stu-id="7cdaa-207">Task rejection</span></span>  <br/> |<span data-ttu-id="7cdaa-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="7cdaa-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="7cdaa-209">Беседа в журнале</span><span class="sxs-lookup"><span data-stu-id="7cdaa-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="7cdaa-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="7cdaa-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="7cdaa-211">Сообщение электронной почты журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-211">Journal email message</span></span>  <br/> |<span data-ttu-id="7cdaa-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="7cdaa-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="7cdaa-213">Запрос на собрание журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="7cdaa-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="7cdaa-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="7cdaa-215">Ответ на собрание журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="7cdaa-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="7cdaa-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="7cdaa-217">Запрос на задачу журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-217">Journal task request</span></span>  <br/> |<span data-ttu-id="7cdaa-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="7cdaa-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="7cdaa-219">Ответ на задачи журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-219">Journal task response</span></span>  <br/> |<span data-ttu-id="7cdaa-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="7cdaa-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="7cdaa-221">Заметка журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-221">Journal note</span></span>  <br/> |<span data-ttu-id="7cdaa-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="7cdaa-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="7cdaa-223">Факс журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-223">Journal fax</span></span>  <br/> |<span data-ttu-id="7cdaa-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="7cdaa-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="7cdaa-225">Телефонный звонок журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="7cdaa-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="7cdaa-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="7cdaa-227">Письмо журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-227">Journal letter</span></span>  <br/> |<span data-ttu-id="7cdaa-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="7cdaa-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="7cdaa-229">Журнал Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="7cdaa-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="7cdaa-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="7cdaa-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="7cdaa-231">Журнал Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="7cdaa-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="7cdaa-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="7cdaa-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="7cdaa-233">Журнал Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="7cdaa-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="7cdaa-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="7cdaa-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="7cdaa-235">Доступ Microsoft Office журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="7cdaa-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="7cdaa-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="7cdaa-237">Документ журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-237">Journal document</span></span>  <br/> |<span data-ttu-id="7cdaa-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="7cdaa-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="7cdaa-239">Собрание журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="7cdaa-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="7cdaa-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="7cdaa-241">Отмена собрания журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="7cdaa-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="7cdaa-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="7cdaa-243">Удаленный сеанс журнала</span><span class="sxs-lookup"><span data-stu-id="7cdaa-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="7cdaa-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="7cdaa-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7cdaa-245">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7cdaa-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7cdaa-246">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7cdaa-246">Protocol specifications</span></span>

<span data-ttu-id="7cdaa-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cdaa-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cdaa-248">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7cdaa-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cdaa-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cdaa-250">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="7cdaa-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cdaa-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cdaa-252">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="7cdaa-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cdaa-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cdaa-254">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7cdaa-255">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="7cdaa-255">Header files</span></span>

<span data-ttu-id="7cdaa-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7cdaa-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="7cdaa-257">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="7cdaa-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7cdaa-258">Mapitags.h</span></span>
  
> <span data-ttu-id="7cdaa-259">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7cdaa-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cdaa-260">См. также</span><span class="sxs-lookup"><span data-stu-id="7cdaa-260">See also</span></span>



[<span data-ttu-id="7cdaa-261">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cdaa-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7cdaa-262">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cdaa-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7cdaa-263">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7cdaa-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7cdaa-264">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="7cdaa-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

