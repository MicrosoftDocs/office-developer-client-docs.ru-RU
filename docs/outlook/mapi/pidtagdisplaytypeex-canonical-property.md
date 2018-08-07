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
ms.openlocfilehash: a21eecfb1bf3bc4f09fc5becb9a4a99a97193330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811092"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="90a4b-103">Каноническое свойство PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="90a4b-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="90a4b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90a4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90a4b-105">Содержит тип записи, в отношении как операция должно отображаться на строку в таблице для глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="90a4b-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90a4b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="90a4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90a4b-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="90a4b-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="90a4b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="90a4b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90a4b-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="90a4b-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="90a4b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="90a4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="90a4b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90a4b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="90a4b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="90a4b-112">Area:</span></span>  <br/> |<span data-ttu-id="90a4b-113">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="90a4b-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90a4b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="90a4b-114">Remarks</span></span>

<span data-ttu-id="90a4b-115">Это свойство определяет тип записи, в отношении как должны отображаться в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="90a4b-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="90a4b-116">Они предоставляют дополнительную информацию, которая не может быть представлена в **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="90a4b-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="90a4b-117">Значения **PR_DISPLAY_TYPE** и это свойство начинаются с «DT_» и определяются в Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="90a4b-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="90a4b-118">Все значения не задокументирован зарезервированы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="90a4b-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="90a4b-119">Клиентские приложения не должны определить все новые значения и должны быть готовы для смягчения последствий недокументированного значения.</span><span class="sxs-lookup"><span data-stu-id="90a4b-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="90a4b-120">Существуют некоторые макросы, которые могут помочь определить атрибуты объекта, например, будет ли это локального, удаленного или контролем безопасности.</span><span class="sxs-lookup"><span data-stu-id="90a4b-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="90a4b-121">Эти макросы включают:</span><span class="sxs-lookup"><span data-stu-id="90a4b-121">These macros include:</span></span> 
  
|<span data-ttu-id="90a4b-122">**Макрос**</span><span class="sxs-lookup"><span data-stu-id="90a4b-122">**Macro**</span></span>|<span data-ttu-id="90a4b-123">**Значение**</span><span class="sxs-lookup"><span data-stu-id="90a4b-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90a4b-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="90a4b-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="90a4b-125">0x80000000)</span><span class="sxs-lookup"><span data-stu-id="90a4b-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="90a4b-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="90a4b-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="90a4b-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="90a4b-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="90a4b-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="90a4b-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="90a4b-129">0x0000FF00</span><span class="sxs-lookup"><span data-stu-id="90a4b-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="90a4b-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="90a4b-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="90a4b-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="90a4b-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="90a4b-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="90a4b-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="90a4b-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="90a4b-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="90a4b-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="90a4b-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="90a4b-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="90a4b-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="90a4b-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="90a4b-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="90a4b-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="90a4b-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="90a4b-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="90a4b-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="90a4b-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="90a4b-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="90a4b-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="90a4b-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="90a4b-141">((ULONG) 0X00000007)</span><span class="sxs-lookup"><span data-stu-id="90a4b-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="90a4b-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="90a4b-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="90a4b-143">((ULONG) 0X00000008)</span><span class="sxs-lookup"><span data-stu-id="90a4b-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="90a4b-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="90a4b-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="90a4b-145">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="90a4b-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="90a4b-146">Ниже приведены некоторые примечания об использовании этих макросов.</span><span class="sxs-lookup"><span data-stu-id="90a4b-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="90a4b-147">Чтобы проверить, является ли запись удаленного запись в другом лесу, относятся к значение этого свойства, чтобы проверить, установлен ли флажок DTE_FLAG_REMOTE_VALID в запись макроса DTE_IS_REMOTE_VALID.</span><span class="sxs-lookup"><span data-stu-id="90a4b-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="90a4b-148">Если удаленный запись, чтобы затем узнать тип удаленные записи с помощью макроса DTE_REMOTE.</span><span class="sxs-lookup"><span data-stu-id="90a4b-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="90a4b-149">В конфигурациях с одним лесом и между лесами когда **PR_DISPLAY_TYPE** имеет значение DT_DISTLIST и DTE_IS_REMOTE_VALID присвоено значение false, применение макрос DTE_LOCAL значение этого свойства может позволяют затем определить тип объекта как DT_DISTLIST (список рассылки) или DT_SEC_DISTLIST (список рассылки безопасности).</span><span class="sxs-lookup"><span data-stu-id="90a4b-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="90a4b-150">Если применить макрос DTE_LOCAL значение **PR_DISPLAY_TYPE_EX** , он возвращает тип DT_REMOTE_MAILUSER запись является записью удаленного.</span><span class="sxs-lookup"><span data-stu-id="90a4b-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="90a4b-151">В одном лесу или в конфигурации между лесами, где репликации, контролируются с списка управления доступом (ACL) макрос DTE_IS_ACL_CAPABLE можно использовать для определения, является ли запись участника безопасности.</span><span class="sxs-lookup"><span data-stu-id="90a4b-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="90a4b-152">В конфигурации между лесами **PR_DISPLAY_TYPE** имеет значение DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="90a4b-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="90a4b-153">Применение макрос DTE_REMOTE значение этого свойства позволяет получить тип удаленные записи.</span><span class="sxs-lookup"><span data-stu-id="90a4b-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="90a4b-154">Ниже представлены возможные типы удаленного элемента.</span><span class="sxs-lookup"><span data-stu-id="90a4b-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="90a4b-155">**Тип записи удаленного**</span><span class="sxs-lookup"><span data-stu-id="90a4b-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="90a4b-156">**Значение**</span><span class="sxs-lookup"><span data-stu-id="90a4b-156">**Value**</span></span>|<span data-ttu-id="90a4b-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90a4b-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90a4b-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="90a4b-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="90a4b-159">((ULONG) 0X00000003)</span><span class="sxs-lookup"><span data-stu-id="90a4b-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="90a4b-160">Список динамических рассылки.</span><span class="sxs-lookup"><span data-stu-id="90a4b-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="90a4b-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="90a4b-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="90a4b-162">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="90a4b-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="90a4b-163">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="90a4b-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="90a4b-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="90a4b-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="90a4b-165">((ULONG) 0X00000008)</span><span class="sxs-lookup"><span data-stu-id="90a4b-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="90a4b-166">Оборудование, например, принтера или проектор.</span><span class="sxs-lookup"><span data-stu-id="90a4b-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="90a4b-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="90a4b-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="90a4b-168">((ULONG) 0X00000000)</span><span class="sxs-lookup"><span data-stu-id="90a4b-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="90a4b-169">Пользователь с почтовым ящиком.</span><span class="sxs-lookup"><span data-stu-id="90a4b-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="90a4b-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="90a4b-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="90a4b-171">((ULONG) 0X00000000)</span><span class="sxs-lookup"><span data-stu-id="90a4b-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="90a4b-172">Запись списка адресов в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="90a4b-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="90a4b-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="90a4b-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="90a4b-174">((ULONG) 0X00000007)</span><span class="sxs-lookup"><span data-stu-id="90a4b-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="90a4b-175">Конференц-зала.</span><span class="sxs-lookup"><span data-stu-id="90a4b-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="90a4b-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="90a4b-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="90a4b-177">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="90a4b-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="90a4b-178">Список рассылки безопасности.</span><span class="sxs-lookup"><span data-stu-id="90a4b-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="90a4b-179">В одном лесу и между лесами конфигурации, когда **PR_DISPLAY_TYPE** имеет значение DT_DISTLIST и DTE_IS_REMOTE_VALID имеет значение false, применение макрос DTE_LOCAL значение этого свойства может позволяют получить тип списка рассылки .</span><span class="sxs-lookup"><span data-stu-id="90a4b-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="90a4b-180">Ниже представлены возможные типы списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="90a4b-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="90a4b-181">**Тип списка рассылки**</span><span class="sxs-lookup"><span data-stu-id="90a4b-181">**Type of Distribution List**</span></span>|<span data-ttu-id="90a4b-182">**Значение**</span><span class="sxs-lookup"><span data-stu-id="90a4b-182">**Value**</span></span>|<span data-ttu-id="90a4b-183">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90a4b-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90a4b-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="90a4b-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="90a4b-185">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="90a4b-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="90a4b-186">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="90a4b-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="90a4b-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="90a4b-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="90a4b-188">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="90a4b-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="90a4b-189">Список рассылки безопасности.</span><span class="sxs-lookup"><span data-stu-id="90a4b-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="90a4b-190">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="90a4b-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90a4b-191">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="90a4b-191">Protocol specifications</span></span>

<span data-ttu-id="90a4b-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90a4b-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90a4b-193">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="90a4b-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90a4b-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90a4b-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90a4b-195">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90a4b-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90a4b-196">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="90a4b-196">Header files</span></span>

<span data-ttu-id="90a4b-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90a4b-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="90a4b-198">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="90a4b-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="90a4b-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90a4b-199">Mapitags.h</span></span>
  
> <span data-ttu-id="90a4b-200">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="90a4b-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90a4b-201">См. также</span><span class="sxs-lookup"><span data-stu-id="90a4b-201">See also</span></span>



[<span data-ttu-id="90a4b-202">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="90a4b-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90a4b-203">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="90a4b-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90a4b-204">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="90a4b-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90a4b-205">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="90a4b-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

