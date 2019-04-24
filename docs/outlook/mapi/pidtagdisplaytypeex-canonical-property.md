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
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="6d12c-103">Каноническое свойство PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="6d12c-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="6d12c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d12c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d12c-105">Содержит тип записи, по отношению к способу отображения записи в строке таблицы для глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="6d12c-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d12c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d12c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d12c-107">ПР_ДИСПЛАЙ_ТИПЕ_ЕКС</span><span class="sxs-lookup"><span data-stu-id="6d12c-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="6d12c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6d12c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d12c-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="6d12c-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="6d12c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d12c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d12c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6d12c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6d12c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6d12c-112">Area:</span></span>  <br/> |<span data-ttu-id="6d12c-113">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="6d12c-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d12c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d12c-114">Remarks</span></span>

<span data-ttu-id="6d12c-115">Это свойство определяет тип записи по отношению к тому, как она должна отображаться в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="6d12c-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="6d12c-116">Он предоставляет дополнительные сведения, которые не могут быть представлены в **пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6d12c-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="6d12c-117">Значения обоих **пр_дисплай_типе** и этого свойства начинаются с "дт_" и определяются в мапитагс. h.</span><span class="sxs-lookup"><span data-stu-id="6d12c-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="6d12c-118">Все значения, которые не задокументированы, зарезервированы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="6d12c-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="6d12c-119">Клиентские приложения не должны определять новые значения и должны быть готовы к работе с недокументированным значением.</span><span class="sxs-lookup"><span data-stu-id="6d12c-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="6d12c-120">Существует несколько макросов, которые могут помочь определить атрибуты объекта, например, будь это локальная, удаленная или контроль безопасности.</span><span class="sxs-lookup"><span data-stu-id="6d12c-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="6d12c-121">К этим макросам относятся:</span><span class="sxs-lookup"><span data-stu-id="6d12c-121">These macros include:</span></span> 
  
|<span data-ttu-id="6d12c-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="6d12c-122">**Macro**</span></span>|<span data-ttu-id="6d12c-123">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6d12c-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d12c-124">ДТЕ_ФЛАГ_РЕМОТЕ_ВАЛИД</span><span class="sxs-lookup"><span data-stu-id="6d12c-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="6d12c-125">0x80000000</span><span class="sxs-lookup"><span data-stu-id="6d12c-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="6d12c-126">ДТЕ_ФЛАГ_АКЛ_КАПАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="6d12c-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="6d12c-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="6d12c-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="6d12c-128">ДТЕ_МАСК_РЕМОТЕ</span><span class="sxs-lookup"><span data-stu-id="6d12c-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="6d12c-129">0x0000FF00</span><span class="sxs-lookup"><span data-stu-id="6d12c-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="6d12c-130">ДТЕ_МАСК_ЛОКАЛ</span><span class="sxs-lookup"><span data-stu-id="6d12c-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="6d12c-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="6d12c-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="6d12c-132">ДТЕ_ИС_РЕМОТЕ_ВАЛИД (v)</span><span class="sxs-lookup"><span data-stu-id="6d12c-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="6d12c-133">(!! ((v) &amp; дте_флаг_ремоте_валид)</span><span class="sxs-lookup"><span data-stu-id="6d12c-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="6d12c-134">ДТЕ_ИС_АКЛ_КАПАБЛЕ (v)</span><span class="sxs-lookup"><span data-stu-id="6d12c-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="6d12c-135">(!! ((v) &amp; дте_флаг_акл_капабле))</span><span class="sxs-lookup"><span data-stu-id="6d12c-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="6d12c-136">ДТЕ_РЕМОТЕ (v)</span><span class="sxs-lookup"><span data-stu-id="6d12c-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="6d12c-137">(((v) &amp; дте_маск_ремоте) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="6d12c-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="6d12c-138">ДТЕ_ЛОКАЛ (v)</span><span class="sxs-lookup"><span data-stu-id="6d12c-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="6d12c-139">((v) &amp; дте_маск_локал)</span><span class="sxs-lookup"><span data-stu-id="6d12c-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="6d12c-140">ДТ_РУМ</span><span class="sxs-lookup"><span data-stu-id="6d12c-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="6d12c-141">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="6d12c-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="6d12c-142">ДТ_ЕКУИПМЕНТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="6d12c-143">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="6d12c-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="6d12c-144">ДТ_СЕК_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="6d12c-145">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="6d12c-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="6d12c-146">Ниже приведены несколько заметок о том, как использовать эти макросы.</span><span class="sxs-lookup"><span data-stu-id="6d12c-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="6d12c-147">Чтобы проверить, является ли запись удаленной записью в другом лесу, примените макрос ДТЕ_ИС_РЕМОТЕ_ВАЛИД к значению этого свойства, чтобы проверить, установлен ли флаг ДТЕ_ФЛАГ_РЕМОТЕ_ВАЛИД в записи.</span><span class="sxs-lookup"><span data-stu-id="6d12c-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="6d12c-148">Если это удаленная запись, можно узнать тип удаленной записи с помощью макроса ДТЕ_РЕМОТЕ.</span><span class="sxs-lookup"><span data-stu-id="6d12c-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="6d12c-149">В конфигурациях с одним лесом и между лесами, когда **пр_дисплай_типе** имеет значение дт_дистлист, а дте_ис_ремоте_валид имеет значение false, применение макроса дте_локал к значению этого свойства позволяет определить тип объекта как ДТ_ДИСТЛИСТ (список рассылки) или ДТ_СЕК_ДИСТЛИСТ (список рассылки по безопасности).</span><span class="sxs-lookup"><span data-stu-id="6d12c-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="6d12c-150">Если вы применяете макрос ДТЕ_ЛОКАЛ к значению \*\*пр_дисплай_типе_екс\*\* и ВОЗВРАЩАЕТ тип дт_ремоте_маилусер, то запись будет удалена.</span><span class="sxs-lookup"><span data-stu-id="6d12c-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="6d12c-151">В отдельном лесу или в конфигурации с несколькими лесами, где управление репликацией осуществляется со списками управления доступом (ACL), можно использовать макрос ДТЕ_ИС_АКЛ_КАПАБЛЕ, чтобы определить, является ли запись субъектом безопасности.</span><span class="sxs-lookup"><span data-stu-id="6d12c-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="6d12c-152">В конфигурации с несколькими лесами **пр_дисплай_типе** имеет значение дт_ремоте_маилусер.</span><span class="sxs-lookup"><span data-stu-id="6d12c-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="6d12c-153">Применение макроса ДТЕ_РЕМОТЕ к значению этого свойства позволяет получить тип удаленной записи.</span><span class="sxs-lookup"><span data-stu-id="6d12c-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="6d12c-154">Возможны следующие типы удаленной записи:</span><span class="sxs-lookup"><span data-stu-id="6d12c-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="6d12c-155">**Тип удаленной записи**</span><span class="sxs-lookup"><span data-stu-id="6d12c-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="6d12c-156">**Value**</span><span class="sxs-lookup"><span data-stu-id="6d12c-156">**Value**</span></span>|<span data-ttu-id="6d12c-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d12c-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d12c-158">ДТ_АЖЕНТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="6d12c-159">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="6d12c-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="6d12c-160">Динамический список рассылки.</span><span class="sxs-lookup"><span data-stu-id="6d12c-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="6d12c-161">ДТ_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="6d12c-162">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="6d12c-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="6d12c-163">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="6d12c-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="6d12c-164">ДТ_ЕКУИПМЕНТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="6d12c-165">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="6d12c-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="6d12c-166">Оборудование, например принтер или проектор.</span><span class="sxs-lookup"><span data-stu-id="6d12c-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="6d12c-167">ДТ_МАИЛУСЕР</span><span class="sxs-lookup"><span data-stu-id="6d12c-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="6d12c-168">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="6d12c-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="6d12c-169">Пользователь с почтовым ящиком.</span><span class="sxs-lookup"><span data-stu-id="6d12c-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="6d12c-170">ДТ_РЕМОТЕ_МАИЛУСЕР</span><span class="sxs-lookup"><span data-stu-id="6d12c-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="6d12c-171">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="6d12c-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="6d12c-172">Запись списка адресов в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="6d12c-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="6d12c-173">ДТ_РУМ</span><span class="sxs-lookup"><span data-stu-id="6d12c-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="6d12c-174">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="6d12c-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="6d12c-175">Конференц-зал.</span><span class="sxs-lookup"><span data-stu-id="6d12c-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="6d12c-176">ДТ_СЕК_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="6d12c-177">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="6d12c-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="6d12c-178">Список рассылки по безопасности.</span><span class="sxs-lookup"><span data-stu-id="6d12c-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="6d12c-179">Как в случае с одним лесом, так и в конфигурации с несколькими лесами, когда **пр_дисплай_типе** имеет значение дт_дистлист, а дте_ис_ремоте_валид — false, применение макроса дте_локал к значению этого свойства позволит получить тип списка рассылки. .</span><span class="sxs-lookup"><span data-stu-id="6d12c-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="6d12c-180">Ниже перечислены возможные типы списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="6d12c-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="6d12c-181">**Тип списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="6d12c-181">**Type of Distribution List**</span></span>|<span data-ttu-id="6d12c-182">**Value**</span><span class="sxs-lookup"><span data-stu-id="6d12c-182">**Value**</span></span>|<span data-ttu-id="6d12c-183">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d12c-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d12c-184">ДТ_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="6d12c-185">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="6d12c-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="6d12c-186">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="6d12c-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="6d12c-187">ДТ_СЕК_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="6d12c-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="6d12c-188">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="6d12c-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="6d12c-189">Список рассылки по безопасности.</span><span class="sxs-lookup"><span data-stu-id="6d12c-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6d12c-190">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d12c-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d12c-191">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6d12c-191">Protocol specifications</span></span>

<span data-ttu-id="6d12c-192">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d12c-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d12c-193">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6d12c-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d12c-194">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d12c-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d12c-195">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d12c-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d12c-196">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="6d12c-196">Header files</span></span>

<span data-ttu-id="6d12c-197">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6d12c-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d12c-198">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d12c-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d12c-199">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6d12c-199">Mapitags.h</span></span>
  
> <span data-ttu-id="6d12c-200">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="6d12c-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d12c-201">См. также</span><span class="sxs-lookup"><span data-stu-id="6d12c-201">See also</span></span>



[<span data-ttu-id="6d12c-202">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d12c-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d12c-203">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6d12c-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d12c-204">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d12c-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d12c-205">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6d12c-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

