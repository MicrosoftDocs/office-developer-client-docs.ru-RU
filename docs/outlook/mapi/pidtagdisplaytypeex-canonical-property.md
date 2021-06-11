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
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="8197a-103">Каноническое свойство PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="8197a-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="8197a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8197a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8197a-105">Содержит тип записи в отношении того, как запись должна отображаться в строке в таблице глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="8197a-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8197a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8197a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8197a-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="8197a-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="8197a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8197a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8197a-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="8197a-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="8197a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8197a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8197a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8197a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8197a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8197a-112">Area:</span></span>  <br/> |<span data-ttu-id="8197a-113">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="8197a-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8197a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8197a-114">Remarks</span></span>

<span data-ttu-id="8197a-115">Это свойство указывает тип записи в отношении того, как она должна отображаться в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="8197a-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="8197a-116">Он предоставляет дополнительные сведения, которые не могут быть представлены **в PR_DISPLAY_TYPE** [(PidTagDisplayType).](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8197a-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8197a-117">Значения как PR_DISPLAY_TYPE, так и этого свойства начинаются с DT_ и определяются в Mapitags.h. </span><span class="sxs-lookup"><span data-stu-id="8197a-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="8197a-118">Все значения, не задокументированные, зарезервированы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="8197a-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="8197a-119">Клиентские приложения не должны определять новые значения и должны быть готовы к обращению с недокументным значением.</span><span class="sxs-lookup"><span data-stu-id="8197a-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="8197a-120">Существуют некоторые макрос, которые могут помочь определить атрибуты объекта, например локальный, удаленный или контролируемый безопасностью.</span><span class="sxs-lookup"><span data-stu-id="8197a-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="8197a-121">Эти макрос включают в себя:</span><span class="sxs-lookup"><span data-stu-id="8197a-121">These macros include:</span></span> 
  
|<span data-ttu-id="8197a-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="8197a-122">**Macro**</span></span>|<span data-ttu-id="8197a-123">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8197a-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8197a-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="8197a-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="8197a-125">0x80000000)</span><span class="sxs-lookup"><span data-stu-id="8197a-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="8197a-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="8197a-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="8197a-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="8197a-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="8197a-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="8197a-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="8197a-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="8197a-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="8197a-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="8197a-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="8197a-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="8197a-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="8197a-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="8197a-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="8197a-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="8197a-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="8197a-134">DTE_IS_ACL_CAPABLE (v)</span><span class="sxs-lookup"><span data-stu-id="8197a-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="8197a-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="8197a-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="8197a-136">DTE_REMOTE (v)</span><span class="sxs-lookup"><span data-stu-id="8197a-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="8197a-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="8197a-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="8197a-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="8197a-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="8197a-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="8197a-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="8197a-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="8197a-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="8197a-141">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="8197a-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="8197a-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="8197a-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="8197a-143">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="8197a-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="8197a-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8197a-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="8197a-145">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="8197a-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="8197a-146">Ниже приводится несколько заметок об использовании этих макрос.</span><span class="sxs-lookup"><span data-stu-id="8197a-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="8197a-147">Чтобы проверить, является ли запись удаленной записью в другом лесу, применяйте макрос DTE_IS_REMOTE_VALID к значению этого свойства, чтобы проверить, установлен ли флаг DTE_FLAG_REMOTE_VALID в записи.</span><span class="sxs-lookup"><span data-stu-id="8197a-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="8197a-148">Если это удаленная запись, вы можете узнать тип удаленной записи с помощью DTE_REMOTE макроса.</span><span class="sxs-lookup"><span data-stu-id="8197a-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="8197a-149">В конфигурациях как лесного, так и межлесного, если **PR_DISPLAY_TYPE** имеет значение DT_DISTLIST, а DTE_IS_REMOTE_VALID — ложное, применение макроса DTE_LOCAL к значению этого свойства может позволить дополнительно определить тип объекта как DT_DISTLIST (список рассылки) или DT_SEC_DISTLIST (список рассылки безопасности).</span><span class="sxs-lookup"><span data-stu-id="8197a-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="8197a-150">Если применить макрос DTE_LOCAL значение PR_DISPLAY_TYPE_EX  и он возвращает тип DT_REMOTE_MAILUSER, то запись является удаленной записью.</span><span class="sxs-lookup"><span data-stu-id="8197a-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="8197a-151">В одном лесу или в межлесной конфигурации, где репликация контролируется списком управления доступом (ACL), вы можете использовать макрос DTE_IS_ACL_CAPABLE, чтобы определить, является ли запись основной службой безопасности.</span><span class="sxs-lookup"><span data-stu-id="8197a-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="8197a-152">В конфигурации между лесами **PR_DISPLAY_TYPE** имеет значение DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="8197a-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="8197a-153">Применение макроса DTE_REMOTE к значению этого свойства может позволить вам получить тип удаленной записи.</span><span class="sxs-lookup"><span data-stu-id="8197a-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="8197a-154">Возможные типы удаленной записи:</span><span class="sxs-lookup"><span data-stu-id="8197a-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="8197a-155">**Тип удаленного входа**</span><span class="sxs-lookup"><span data-stu-id="8197a-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="8197a-156">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8197a-156">**Value**</span></span>|<span data-ttu-id="8197a-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8197a-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8197a-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="8197a-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="8197a-159">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="8197a-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="8197a-160">Динамический список рассылки.</span><span class="sxs-lookup"><span data-stu-id="8197a-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="8197a-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8197a-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="8197a-162">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8197a-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="8197a-163">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="8197a-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="8197a-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="8197a-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="8197a-165">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="8197a-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="8197a-166">Оборудование, например принтер или проектор.</span><span class="sxs-lookup"><span data-stu-id="8197a-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="8197a-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="8197a-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="8197a-168">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="8197a-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="8197a-169">Пользователь с почтовым ящиком.</span><span class="sxs-lookup"><span data-stu-id="8197a-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="8197a-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="8197a-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="8197a-171">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="8197a-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="8197a-172">Запись списка адресов в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="8197a-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="8197a-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="8197a-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="8197a-174">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="8197a-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="8197a-175">Конференц-зал.</span><span class="sxs-lookup"><span data-stu-id="8197a-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="8197a-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8197a-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="8197a-177">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="8197a-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="8197a-178">Список рассылки безопасности.</span><span class="sxs-lookup"><span data-stu-id="8197a-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="8197a-179">Как в одном лесу, так и в межлесной конфигурации, **если** PR_DISPLAY_TYPE значение DT_DISTLIST и DTE_IS_REMOTE_VALID является ложным, применение макроса DTE_LOCAL к значению этого свойства может позволить вам получить тип списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="8197a-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="8197a-180">Возможные типы списка рассылки:</span><span class="sxs-lookup"><span data-stu-id="8197a-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="8197a-181">**Тип списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="8197a-181">**Type of Distribution List**</span></span>|<span data-ttu-id="8197a-182">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8197a-182">**Value**</span></span>|<span data-ttu-id="8197a-183">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8197a-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8197a-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8197a-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="8197a-185">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8197a-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="8197a-186">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="8197a-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="8197a-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8197a-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="8197a-188">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="8197a-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="8197a-189">Список рассылки безопасности.</span><span class="sxs-lookup"><span data-stu-id="8197a-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8197a-190">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8197a-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8197a-191">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8197a-191">Protocol specifications</span></span>

<span data-ttu-id="8197a-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8197a-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8197a-193">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="8197a-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8197a-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8197a-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8197a-195">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8197a-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8197a-196">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8197a-196">Header files</span></span>

<span data-ttu-id="8197a-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8197a-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="8197a-198">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8197a-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="8197a-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8197a-199">Mapitags.h</span></span>
  
> <span data-ttu-id="8197a-200">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8197a-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8197a-201">См. также</span><span class="sxs-lookup"><span data-stu-id="8197a-201">See also</span></span>



[<span data-ttu-id="8197a-202">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8197a-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8197a-203">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8197a-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8197a-204">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8197a-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8197a-205">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8197a-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

