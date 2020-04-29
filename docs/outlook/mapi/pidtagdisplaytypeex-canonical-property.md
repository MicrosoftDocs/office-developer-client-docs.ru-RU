---
title: Каноническое свойство PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360776"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="91ac3-103">Каноническое свойство PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="91ac3-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="91ac3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91ac3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91ac3-105">Содержит тип записи, по отношению к способу отображения записи в строке таблицы для глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="91ac3-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91ac3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="91ac3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91ac3-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="91ac3-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="91ac3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="91ac3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91ac3-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="91ac3-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="91ac3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="91ac3-110">Data type:</span></span>  <br/> |<span data-ttu-id="91ac3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="91ac3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="91ac3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="91ac3-112">Area:</span></span>  <br/> |<span data-ttu-id="91ac3-113">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="91ac3-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91ac3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="91ac3-114">Remarks</span></span>

<span data-ttu-id="91ac3-115">Это свойство определяет тип записи по отношению к тому, как она должна отображаться в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="91ac3-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="91ac3-116">Он предоставляет дополнительные сведения, которые не могут быть представлены в **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91ac3-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="91ac3-117">Значения обоих **PR_DISPLAY_TYPE** и этого свойства начинаются с "DT_" и определяются в мапитагс. h.</span><span class="sxs-lookup"><span data-stu-id="91ac3-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="91ac3-118">Все значения, которые не задокументированы, зарезервированы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="91ac3-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="91ac3-119">Клиентские приложения не должны определять новые значения и должны быть готовы к работе с недокументированным значением.</span><span class="sxs-lookup"><span data-stu-id="91ac3-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="91ac3-120">Существует несколько макросов, которые могут помочь определить атрибуты объекта, например, будь это локальная, удаленная или контроль безопасности.</span><span class="sxs-lookup"><span data-stu-id="91ac3-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="91ac3-121">К этим макросам относятся:</span><span class="sxs-lookup"><span data-stu-id="91ac3-121">These macros include:</span></span> 
  
|<span data-ttu-id="91ac3-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="91ac3-122">**Macro**</span></span>|<span data-ttu-id="91ac3-123">**Значение**</span><span class="sxs-lookup"><span data-stu-id="91ac3-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91ac3-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="91ac3-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="91ac3-125">0x80000000</span><span class="sxs-lookup"><span data-stu-id="91ac3-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="91ac3-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="91ac3-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="91ac3-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="91ac3-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="91ac3-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="91ac3-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="91ac3-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="91ac3-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="91ac3-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="91ac3-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="91ac3-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="91ac3-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="91ac3-132">DTE_IS_REMOTE_VALID (v)</span><span class="sxs-lookup"><span data-stu-id="91ac3-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="91ac3-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="91ac3-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="91ac3-134">DTE_IS_ACL_CAPABLE (v)</span><span class="sxs-lookup"><span data-stu-id="91ac3-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="91ac3-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="91ac3-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="91ac3-136">DTE_REMOTE (v)</span><span class="sxs-lookup"><span data-stu-id="91ac3-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="91ac3-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="91ac3-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="91ac3-138">DTE_LOCAL (v)</span><span class="sxs-lookup"><span data-stu-id="91ac3-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="91ac3-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="91ac3-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="91ac3-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="91ac3-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="91ac3-141">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="91ac3-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="91ac3-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="91ac3-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="91ac3-143">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="91ac3-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="91ac3-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="91ac3-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="91ac3-145">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="91ac3-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="91ac3-146">Ниже приведены несколько заметок о том, как использовать эти макросы.</span><span class="sxs-lookup"><span data-stu-id="91ac3-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="91ac3-147">Чтобы проверить, является ли запись удаленной записью в другом лесу, примените макрос DTE_IS_REMOTE_VALID к значению этого свойства, чтобы проверить, установлен ли флаг DTE_FLAG_REMOTE_VALID в записи.</span><span class="sxs-lookup"><span data-stu-id="91ac3-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="91ac3-148">Если это удаленная запись, можно узнать тип удаленной записи с помощью макроса DTE_REMOTE.</span><span class="sxs-lookup"><span data-stu-id="91ac3-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="91ac3-149">В конфигурациях с одним лесом и между лесами, если **PR_DISPLAY_TYPE** имеет значение DT_DISTLIST, а DTE_IS_REMOTE_VALID имеет значение false, то применение DTE_LOCAL макросов к значению этого свойства позволяет определить тип объекта как DT_DISTLIST (списка рассылки) или DT_SEC_DISTLIST (список рассылки безопасности).</span><span class="sxs-lookup"><span data-stu-id="91ac3-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="91ac3-150">Если вы применяете DTE_LOCAL макроса к значению **PR_DISPLAY_TYPE_EX** и возвращает тип DT_REMOTE_MAILUSER, то запись будет удалена.</span><span class="sxs-lookup"><span data-stu-id="91ac3-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="91ac3-151">В отдельном лесу или в конфигурации с несколькими лесами, где управление репликацией осуществляется со списками управления доступом (ACL), можно использовать макрос DTE_IS_ACL_CAPABLE, чтобы определить, является ли запись субъектом безопасности.</span><span class="sxs-lookup"><span data-stu-id="91ac3-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="91ac3-152">В конфигурации с несколькими лесами **PR_DISPLAY_TYPE** имеет значение DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="91ac3-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="91ac3-153">Применение макроса DTE_REMOTE к значению этого свойства позволяет получить тип удаленной записи.</span><span class="sxs-lookup"><span data-stu-id="91ac3-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="91ac3-154">Возможны следующие типы удаленной записи:</span><span class="sxs-lookup"><span data-stu-id="91ac3-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="91ac3-155">**Тип удаленной записи**</span><span class="sxs-lookup"><span data-stu-id="91ac3-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="91ac3-156">**Значение**</span><span class="sxs-lookup"><span data-stu-id="91ac3-156">**Value**</span></span>|<span data-ttu-id="91ac3-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="91ac3-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91ac3-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="91ac3-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="91ac3-159">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="91ac3-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="91ac3-160">Динамический список рассылки.</span><span class="sxs-lookup"><span data-stu-id="91ac3-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="91ac3-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="91ac3-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="91ac3-162">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="91ac3-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="91ac3-163">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="91ac3-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="91ac3-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="91ac3-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="91ac3-165">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="91ac3-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="91ac3-166">Оборудование, например принтер или проектор.</span><span class="sxs-lookup"><span data-stu-id="91ac3-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="91ac3-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="91ac3-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="91ac3-168">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="91ac3-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="91ac3-169">Пользователь с почтовым ящиком.</span><span class="sxs-lookup"><span data-stu-id="91ac3-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="91ac3-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="91ac3-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="91ac3-171">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="91ac3-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="91ac3-172">Запись списка адресов в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="91ac3-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="91ac3-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="91ac3-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="91ac3-174">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="91ac3-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="91ac3-175">Конференц-зал.</span><span class="sxs-lookup"><span data-stu-id="91ac3-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="91ac3-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="91ac3-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="91ac3-177">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="91ac3-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="91ac3-178">Список рассылки по безопасности.</span><span class="sxs-lookup"><span data-stu-id="91ac3-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="91ac3-179">В случае с одним лесом и в конфигурации нескольких лесов, если **PR_DISPLAY_TYPE** имеет значение DT_DISTLIST и DTE_IS_REMOTE_VALID false, то применение макроса DTE_LOCAL к значению этого свойства может позволить получить тип списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="91ac3-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="91ac3-180">Ниже перечислены возможные типы списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="91ac3-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="91ac3-181">**Тип списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="91ac3-181">**Type of Distribution List**</span></span>|<span data-ttu-id="91ac3-182">**Значение**</span><span class="sxs-lookup"><span data-stu-id="91ac3-182">**Value**</span></span>|<span data-ttu-id="91ac3-183">**Описание**</span><span class="sxs-lookup"><span data-stu-id="91ac3-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91ac3-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="91ac3-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="91ac3-185">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="91ac3-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="91ac3-186">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="91ac3-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="91ac3-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="91ac3-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="91ac3-188">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="91ac3-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="91ac3-189">Список рассылки по безопасности.</span><span class="sxs-lookup"><span data-stu-id="91ac3-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="91ac3-190">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91ac3-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91ac3-191">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="91ac3-191">Protocol specifications</span></span>

<span data-ttu-id="91ac3-192">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91ac3-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91ac3-193">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="91ac3-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91ac3-194">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91ac3-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91ac3-195">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91ac3-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91ac3-196">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="91ac3-196">Header files</span></span>

<span data-ttu-id="91ac3-197">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="91ac3-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="91ac3-198">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="91ac3-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="91ac3-199">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="91ac3-199">Mapitags.h</span></span>
  
> <span data-ttu-id="91ac3-200">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="91ac3-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91ac3-201">См. также</span><span class="sxs-lookup"><span data-stu-id="91ac3-201">See also</span></span>



[<span data-ttu-id="91ac3-202">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91ac3-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91ac3-203">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="91ac3-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91ac3-204">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="91ac3-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91ac3-205">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="91ac3-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

