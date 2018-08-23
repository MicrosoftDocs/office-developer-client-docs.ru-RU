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
ms.openlocfilehash: 03465df65498643ce02598fdc26ab78b44e1135a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588680"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="85126-103">Каноническое свойство PidTagIconIndex</span><span class="sxs-lookup"><span data-stu-id="85126-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="85126-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85126-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85126-105">Содержит номер, который указывает, какие значок, используемый при отображении группу объектов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="85126-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85126-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="85126-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85126-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="85126-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="85126-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="85126-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85126-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="85126-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="85126-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="85126-110">Data type:</span></span>  <br/> |<span data-ttu-id="85126-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="85126-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="85126-112">Область:</span><span class="sxs-lookup"><span data-stu-id="85126-112">Area:</span></span>  <br/> |<span data-ttu-id="85126-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="85126-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85126-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="85126-114">Remarks</span></span>

<span data-ttu-id="85126-115">Это свойство, если он существует, соответствует подсказку для клиента.</span><span class="sxs-lookup"><span data-stu-id="85126-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="85126-116">Клиент может игнорировать значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="85126-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="85126-117">**Элемент состояния почты**</span><span class="sxs-lookup"><span data-stu-id="85126-117">**Mail item state**</span></span>|<span data-ttu-id="85126-118">**Значок индексирования**</span><span class="sxs-lookup"><span data-stu-id="85126-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85126-119">Новые сообщения</span><span class="sxs-lookup"><span data-stu-id="85126-119">New mail</span></span>  <br/> |<span data-ttu-id="85126-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="85126-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="85126-121">Запись</span><span class="sxs-lookup"><span data-stu-id="85126-121">Post</span></span>  <br/> |<span data-ttu-id="85126-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="85126-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="85126-123">Other (другие)</span><span class="sxs-lookup"><span data-stu-id="85126-123">Other</span></span>  <br/> |<span data-ttu-id="85126-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="85126-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="85126-125">Чтение почты</span><span class="sxs-lookup"><span data-stu-id="85126-125">Read mail</span></span>  <br/> |<span data-ttu-id="85126-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="85126-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="85126-127">Непрочитанных сообщений</span><span class="sxs-lookup"><span data-stu-id="85126-127">Unread mail</span></span>  <br/> |<span data-ttu-id="85126-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="85126-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="85126-129">Отправленные почты</span><span class="sxs-lookup"><span data-stu-id="85126-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="85126-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="85126-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="85126-131">Неотправленные почты</span><span class="sxs-lookup"><span data-stu-id="85126-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="85126-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="85126-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="85126-133">Получения почты</span><span class="sxs-lookup"><span data-stu-id="85126-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="85126-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="85126-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="85126-135">Пересылаемых почты</span><span class="sxs-lookup"><span data-stu-id="85126-135">Replied mail</span></span>  <br/> |<span data-ttu-id="85126-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="85126-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="85126-137">При пересылке сообщения</span><span class="sxs-lookup"><span data-stu-id="85126-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="85126-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="85126-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="85126-139">Удаленный доступ</span><span class="sxs-lookup"><span data-stu-id="85126-139">Remote mail</span></span>  <br/> |<span data-ttu-id="85126-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="85126-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="85126-141">Доставка почты</span><span class="sxs-lookup"><span data-stu-id="85126-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="85126-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="85126-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="85126-143">Чтение почты</span><span class="sxs-lookup"><span data-stu-id="85126-143">Read mail</span></span>  <br/> |<span data-ttu-id="85126-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="85126-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="85126-145">Недоставке почты</span><span class="sxs-lookup"><span data-stu-id="85126-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="85126-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="85126-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="85126-147">Nonread почты</span><span class="sxs-lookup"><span data-stu-id="85126-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="85126-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="85126-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="85126-149">Recall_S почты</span><span class="sxs-lookup"><span data-stu-id="85126-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="85126-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="85126-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="85126-151">Recall_F почты</span><span class="sxs-lookup"><span data-stu-id="85126-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="85126-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="85126-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="85126-153">Отслеживание почты</span><span class="sxs-lookup"><span data-stu-id="85126-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="85126-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="85126-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="85126-155">Из него почты office</span><span class="sxs-lookup"><span data-stu-id="85126-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="85126-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="85126-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="85126-157">Отзыв почты</span><span class="sxs-lookup"><span data-stu-id="85126-157">Recall mail</span></span>  <br/> |<span data-ttu-id="85126-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="85126-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="85126-159">Записанные почты</span><span class="sxs-lookup"><span data-stu-id="85126-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="85126-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="85126-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="85126-161">Contact</span><span class="sxs-lookup"><span data-stu-id="85126-161">Contact</span></span>  <br/> |<span data-ttu-id="85126-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="85126-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="85126-163">Список рассылки</span><span class="sxs-lookup"><span data-stu-id="85126-163">Distribution list</span></span>  <br/> |<span data-ttu-id="85126-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="85126-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="85126-165">Записки синий</span><span class="sxs-lookup"><span data-stu-id="85126-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="85126-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="85126-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="85126-167">Зеленый записок</span><span class="sxs-lookup"><span data-stu-id="85126-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="85126-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="85126-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="85126-169">Записки розовым</span><span class="sxs-lookup"><span data-stu-id="85126-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="85126-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="85126-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="85126-171">Желтая заметка</span><span class="sxs-lookup"><span data-stu-id="85126-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="85126-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="85126-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="85126-173">Технический записок</span><span class="sxs-lookup"><span data-stu-id="85126-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="85126-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="85126-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="85126-175">Один экземпляр встречи</span><span class="sxs-lookup"><span data-stu-id="85126-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="85126-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="85126-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="85126-177">Повторяющиеся встречи</span><span class="sxs-lookup"><span data-stu-id="85126-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="85126-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="85126-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="85126-179">Один экземпляр собрания</span><span class="sxs-lookup"><span data-stu-id="85126-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="85126-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="85126-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="85126-181">Повторяющееся собрание</span><span class="sxs-lookup"><span data-stu-id="85126-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="85126-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="85126-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="85126-183">Приглашения на собрание</span><span class="sxs-lookup"><span data-stu-id="85126-183">Meeting request</span></span>  <br/> |<span data-ttu-id="85126-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="85126-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="85126-185">Accept</span><span class="sxs-lookup"><span data-stu-id="85126-185">Accept</span></span>  <br/> |<span data-ttu-id="85126-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="85126-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="85126-187">Отклонить</span><span class="sxs-lookup"><span data-stu-id="85126-187">Decline</span></span>  <br/> |<span data-ttu-id="85126-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="85126-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="85126-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="85126-189">Tentativly</span></span>  <br/> |<span data-ttu-id="85126-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="85126-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="85126-191">Отмена</span><span class="sxs-lookup"><span data-stu-id="85126-191">Cancellation</span></span>  <br/> |<span data-ttu-id="85126-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="85126-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="85126-193">Информационные обновления</span><span class="sxs-lookup"><span data-stu-id="85126-193">Informational update</span></span>  <br/> |<span data-ttu-id="85126-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="85126-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="85126-195">Задача/задач</span><span class="sxs-lookup"><span data-stu-id="85126-195">Task/task</span></span>  <br/> |<span data-ttu-id="85126-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="85126-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="85126-197">Неназначенный повторяющейся задачи</span><span class="sxs-lookup"><span data-stu-id="85126-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="85126-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="85126-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="85126-199">Для уполномоченного задач</span><span class="sxs-lookup"><span data-stu-id="85126-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="85126-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="85126-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="85126-201">Назначено по задаче</span><span class="sxs-lookup"><span data-stu-id="85126-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="85126-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="85126-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="85126-203">Запрос задачи</span><span class="sxs-lookup"><span data-stu-id="85126-203">Task request</span></span>  <br/> |<span data-ttu-id="85126-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="85126-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="85126-205">Принятие задачи</span><span class="sxs-lookup"><span data-stu-id="85126-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="85126-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="85126-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="85126-207">Отклонение задачи</span><span class="sxs-lookup"><span data-stu-id="85126-207">Task rejection</span></span>  <br/> |<span data-ttu-id="85126-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="85126-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="85126-209">Журнал бесед</span><span class="sxs-lookup"><span data-stu-id="85126-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="85126-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="85126-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="85126-211">Сообщение электронной почты журнала</span><span class="sxs-lookup"><span data-stu-id="85126-211">Journal email message</span></span>  <br/> |<span data-ttu-id="85126-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="85126-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="85126-213">Журнал приглашения на собрание</span><span class="sxs-lookup"><span data-stu-id="85126-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="85126-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="85126-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="85126-215">Журнал приглашения на собрание</span><span class="sxs-lookup"><span data-stu-id="85126-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="85126-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="85126-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="85126-217">Журнал запроса на задачу</span><span class="sxs-lookup"><span data-stu-id="85126-217">Journal task request</span></span>  <br/> |<span data-ttu-id="85126-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="85126-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="85126-219">Журнал задачи ответа</span><span class="sxs-lookup"><span data-stu-id="85126-219">Journal task response</span></span>  <br/> |<span data-ttu-id="85126-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="85126-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="85126-221">Заметки журнала</span><span class="sxs-lookup"><span data-stu-id="85126-221">Journal note</span></span>  <br/> |<span data-ttu-id="85126-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="85126-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="85126-223">Журнал факсов</span><span class="sxs-lookup"><span data-stu-id="85126-223">Journal fax</span></span>  <br/> |<span data-ttu-id="85126-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="85126-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="85126-225">Журнал телефонного звонка</span><span class="sxs-lookup"><span data-stu-id="85126-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="85126-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="85126-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="85126-227">Буква журнала</span><span class="sxs-lookup"><span data-stu-id="85126-227">Journal letter</span></span>  <br/> |<span data-ttu-id="85126-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="85126-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="85126-229">Журнал Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="85126-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="85126-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="85126-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="85126-231">Журнал Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="85126-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="85126-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="85126-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="85126-233">Журнал Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="85126-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="85126-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="85126-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="85126-235">Microsoft Office Access журнала</span><span class="sxs-lookup"><span data-stu-id="85126-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="85126-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="85126-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="85126-237">Документ журнала</span><span class="sxs-lookup"><span data-stu-id="85126-237">Journal document</span></span>  <br/> |<span data-ttu-id="85126-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="85126-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="85126-239">Журнал собрания</span><span class="sxs-lookup"><span data-stu-id="85126-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="85126-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="85126-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="85126-241">Отмена собрания журнала</span><span class="sxs-lookup"><span data-stu-id="85126-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="85126-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="85126-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="85126-243">Сеанс удаленного журнала</span><span class="sxs-lookup"><span data-stu-id="85126-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="85126-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="85126-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="85126-245">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="85126-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85126-246">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="85126-246">Protocol specifications</span></span>

<span data-ttu-id="85126-247">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85126-247">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85126-248">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="85126-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="85126-249">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85126-249">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85126-250">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="85126-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="85126-251">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85126-251">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85126-252">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="85126-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="85126-253">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85126-253">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85126-254">Задает свойства и операции, допустимые на контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="85126-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85126-255">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="85126-255">Header files</span></span>

<span data-ttu-id="85126-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85126-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="85126-257">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="85126-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="85126-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="85126-258">Mapitags.h</span></span>
  
> <span data-ttu-id="85126-259">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="85126-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85126-260">См. также</span><span class="sxs-lookup"><span data-stu-id="85126-260">See also</span></span>



[<span data-ttu-id="85126-261">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="85126-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85126-262">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="85126-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85126-263">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="85126-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85126-264">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="85126-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

