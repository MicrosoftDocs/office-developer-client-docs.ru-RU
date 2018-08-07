---
title: Каноническое свойство PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 169afc3b8cf982c4767802542b900ae80822cd01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811878"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="b00a3-103">Каноническое свойство PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="b00a3-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="b00a3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b00a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b00a3-105">Содержит двоичный сравнимые ключ, который определяет соответствующих объектов для поиска.</span><span class="sxs-lookup"><span data-stu-id="b00a3-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b00a3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b00a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b00a3-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="b00a3-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="b00a3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b00a3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b00a3-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="b00a3-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="b00a3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b00a3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b00a3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b00a3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b00a3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b00a3-112">Area:</span></span>  <br/> |<span data-ttu-id="b00a3-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="b00a3-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b00a3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b00a3-114">Remarks</span></span>

<span data-ttu-id="b00a3-115">Это свойство содержит трассировку для связанные объекты, такие как копии сообщения и упрощает поиск нежелательных вхождения, такие как повторяющиеся получателей.</span><span class="sxs-lookup"><span data-stu-id="b00a3-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="b00a3-116">MAPI использует определенные правила для создания ключей поиска для получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="b00a3-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="b00a3-117">Ключ поиска образуется путем объединения тип адреса (в верхнем регистре), двоеточие ":", адреса электронной почты в каноническое формы и конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="b00a3-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="b00a3-118">Каноническое формы здесь означает, что к регистру адреса отображаются в случае правильный и адреса, которые не учитывают регистр преобразуются в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="b00a3-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="b00a3-119">Это важно сохранения взаимосвязи между сообщения.</span><span class="sxs-lookup"><span data-stu-id="b00a3-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="b00a3-120">Для объектов-сообщение этому свойству можно получить через метод [IMAPIProp::GetProps](imapiprop-getprops.md) сразу после создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="b00a3-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="b00a3-121">Для других объектов доступных после первого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="b00a3-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="b00a3-122">Поскольку это свойство является изменяемым, нестабильна его можно получить через **GetProps** до вызова **SaveChanges** завершена значения установить или изменить с помощью метода [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="b00a3-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="b00a3-123">Для профилей MAPI также предоставляет раздел жестко заданного профиля с именем **MUID_PROFILE_INSTANCE**, с помощью этого свойства, как его отдельное свойство.</span><span class="sxs-lookup"><span data-stu-id="b00a3-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="b00a3-124">Этот ключ гарантированно уникальным во всех профилей, когда-либо созданных и может быть более надежным, чем свойство **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), который может быть например, удалены и заново с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="b00a3-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="b00a3-125">В следующей таблице представлены важные различия между **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и это свойство.</span><span class="sxs-lookup"><span data-stu-id="b00a3-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="b00a3-126">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="b00a3-126">**Characteristic**</span></span>|<span data-ttu-id="b00a3-127">PR_ENTRYID \*\*\*</span><span class="sxs-lookup"><span data-stu-id="b00a3-127">****PR_ENTRYID****</span></span>|<span data-ttu-id="b00a3-128">PR_RECORD_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="b00a3-128">****PR_RECORD_KEY****</span></span>|<span data-ttu-id="b00a3-129">PR_SEARCH_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="b00a3-129">****PR_SEARCH_KEY****</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b00a3-130">Требуется на объекты вложения</span><span class="sxs-lookup"><span data-stu-id="b00a3-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="b00a3-131">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-131">No</span></span>  <br/> |<span data-ttu-id="b00a3-132">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-132">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-133">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-133">No</span></span>  <br/> |
|<span data-ttu-id="b00a3-134">Требуется на объектов папок</span><span class="sxs-lookup"><span data-stu-id="b00a3-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="b00a3-135">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-135">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-136">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-136">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-137">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-137">No</span></span>  <br/> |
|<span data-ttu-id="b00a3-138">Требуется на объектов хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="b00a3-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="b00a3-139">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-139">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-140">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-140">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-141">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-141">No</span></span>  <br/> |
|<span data-ttu-id="b00a3-142">Требуется на состояние объектов</span><span class="sxs-lookup"><span data-stu-id="b00a3-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="b00a3-143">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-143">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-144">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-144">No</span></span>  <br/> |<span data-ttu-id="b00a3-145">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-145">No</span></span>  <br/> |
|<span data-ttu-id="b00a3-146">Возможно создание клиентом</span><span class="sxs-lookup"><span data-stu-id="b00a3-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="b00a3-147">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-147">No</span></span>  <br/> |<span data-ttu-id="b00a3-148">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-148">No</span></span>  <br/> |<span data-ttu-id="b00a3-149">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-149">Yes</span></span>  <br/> |
|<span data-ttu-id="b00a3-150">Доступные до **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="b00a3-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="b00a3-151">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="b00a3-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="b00a3-152">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="b00a3-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="b00a3-153">Для сообщений, Да.</span><span class="sxs-lookup"><span data-stu-id="b00a3-153">For messages, Yes.</span></span> <span data-ttu-id="b00a3-154">Для других пользователей он зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="b00a3-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="b00a3-155">Изменения в операцию копирования</span><span class="sxs-lookup"><span data-stu-id="b00a3-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="b00a3-156">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-156">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-157">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-157">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-158">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-158">No</span></span>  <br/> |
|<span data-ttu-id="b00a3-159">Механизм клиента после копирования</span><span class="sxs-lookup"><span data-stu-id="b00a3-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="b00a3-160">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-160">No</span></span>  <br/> |<span data-ttu-id="b00a3-161">Нет</span><span class="sxs-lookup"><span data-stu-id="b00a3-161">No</span></span>  <br/> |<span data-ttu-id="b00a3-162">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-162">Yes</span></span>  <br/> |
|<span data-ttu-id="b00a3-163">Уникальный в пределах...</span><span class="sxs-lookup"><span data-stu-id="b00a3-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="b00a3-164">Весь мир</span><span class="sxs-lookup"><span data-stu-id="b00a3-164">Entire world</span></span>  <br/> |<span data-ttu-id="b00a3-165">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="b00a3-165">Provider instance</span></span>  <br/> |<span data-ttu-id="b00a3-166">Весь мир</span><span class="sxs-lookup"><span data-stu-id="b00a3-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="b00a3-167">Двоичный сравнимые (как с memcmp)</span><span class="sxs-lookup"><span data-stu-id="b00a3-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="b00a3-168">Нет — используйте [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="b00a3-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="b00a3-169">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-169">Yes</span></span>  <br/> |<span data-ttu-id="b00a3-170">Да</span><span class="sxs-lookup"><span data-stu-id="b00a3-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b00a3-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b00a3-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b00a3-172">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b00a3-172">Protocol specifications</span></span>

<span data-ttu-id="b00a3-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b00a3-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b00a3-174">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b00a3-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b00a3-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b00a3-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b00a3-176">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="b00a3-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b00a3-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b00a3-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b00a3-178">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b00a3-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b00a3-179">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b00a3-179">Header files</span></span>

<span data-ttu-id="b00a3-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b00a3-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="b00a3-181">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b00a3-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="b00a3-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b00a3-182">Mapitags.h</span></span>
  
> <span data-ttu-id="b00a3-183">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b00a3-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b00a3-184">См. также</span><span class="sxs-lookup"><span data-stu-id="b00a3-184">See also</span></span>



[<span data-ttu-id="b00a3-185">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="b00a3-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="b00a3-186">Каноническое свойство PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="b00a3-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="b00a3-187">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b00a3-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b00a3-188">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b00a3-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b00a3-189">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b00a3-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b00a3-190">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b00a3-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

