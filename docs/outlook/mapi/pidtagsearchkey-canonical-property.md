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
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345467"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="e28a5-103">Каноническое свойство PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="e28a5-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="e28a5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e28a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e28a5-105">Содержит двухсопоставимый ключ, который определяет связанные объекты для поиска.</span><span class="sxs-lookup"><span data-stu-id="e28a5-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e28a5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e28a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e28a5-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e28a5-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="e28a5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e28a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e28a5-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="e28a5-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="e28a5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e28a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="e28a5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e28a5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e28a5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e28a5-112">Area:</span></span>  <br/> |<span data-ttu-id="e28a5-113">Свойства ID</span><span class="sxs-lookup"><span data-stu-id="e28a5-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e28a5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e28a5-114">Remarks</span></span>

<span data-ttu-id="e28a5-115">Это свойство предоставляет след для связанных объектов, таких как копии сообщений, и облегчает поиск нежелательных случаев, таких как дублирующиеся получатели.</span><span class="sxs-lookup"><span data-stu-id="e28a5-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="e28a5-116">MAPI использует определенные правила для создания ключей поиска для получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="e28a5-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="e28a5-117">Ключ поиска формируется путем укоренения типа адреса (в символах верхнего шкафа), символа двоеточия ":", адреса электронной почты в канонической форме и завершающего null.</span><span class="sxs-lookup"><span data-stu-id="e28a5-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="e28a5-118">Каноническая форма здесь означает, что в правильном случае отображаются чувствительные к делу адреса, а адреса, не чувствительные к делу, преобразуются в верхний шкаф.</span><span class="sxs-lookup"><span data-stu-id="e28a5-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="e28a5-119">Это важно для сохранения корреляций между сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e28a5-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="e28a5-120">Для объектов сообщений это свойство доступно с помощью [метода IMAPIProp::GetProps](imapiprop-getprops.md) сразу после создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="e28a5-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="e28a5-121">Для других объектов он доступен после первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="e28a5-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="e28a5-122">Поскольку это свойство является переменным, его невозможно получить через **GetProps** до тех пор, пока вызов **SaveChanges** не совершит какие-либо значения, заданной или измененной методом [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="e28a5-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="e28a5-123">Для профилей MAPI также обставлен жестко закодированным профилем с именем **MUID_PROFILE_INSTANCE**, с этим свойством как с одним свойством.</span><span class="sxs-lookup"><span data-stu-id="e28a5-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="e28a5-124">Этот ключ гарантируется уникальным для всех когда-либо созданных профилей и может быть более надежным, чем **свойство PR_PROFILE_NAME** [(PidTagProfileName),](pidtagprofilename-canonical-property.md)которое может быть, например, удалено и воссоздано с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="e28a5-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="e28a5-125">В следующей таблице суммируются  важные различия между PR_ENTRYID [(PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_RECORD_KEY** [(PidTagRecordKey)](pidtagrecordkey-canonical-property.md)и этим свойством.</span><span class="sxs-lookup"><span data-stu-id="e28a5-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="e28a5-126">**Характеристика**</span><span class="sxs-lookup"><span data-stu-id="e28a5-126">**Characteristic**</span></span>|<span data-ttu-id="e28a5-127">PR_ENTRYID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e28a5-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="e28a5-128">PR_RECORD_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e28a5-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="e28a5-129">PR_SEARCH_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e28a5-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e28a5-130">Необходимые для объектов вложений</span><span class="sxs-lookup"><span data-stu-id="e28a5-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="e28a5-131">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-131">No</span></span>  <br/> |<span data-ttu-id="e28a5-132">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-132">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-133">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-133">No</span></span>  <br/> |
|<span data-ttu-id="e28a5-134">Необходимые для объектов папок</span><span class="sxs-lookup"><span data-stu-id="e28a5-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="e28a5-135">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-135">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-136">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-136">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-137">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-137">No</span></span>  <br/> |
|<span data-ttu-id="e28a5-138">Необходимые для объектов хранения сообщений</span><span class="sxs-lookup"><span data-stu-id="e28a5-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="e28a5-139">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-139">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-140">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-140">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-141">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-141">No</span></span>  <br/> |
|<span data-ttu-id="e28a5-142">Необходимые для объектов состояния</span><span class="sxs-lookup"><span data-stu-id="e28a5-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="e28a5-143">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-143">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-144">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-144">No</span></span>  <br/> |<span data-ttu-id="e28a5-145">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-145">No</span></span>  <br/> |
|<span data-ttu-id="e28a5-146">Creatable клиентом</span><span class="sxs-lookup"><span data-stu-id="e28a5-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="e28a5-147">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-147">No</span></span>  <br/> |<span data-ttu-id="e28a5-148">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-148">No</span></span>  <br/> |<span data-ttu-id="e28a5-149">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-149">Yes</span></span>  <br/> |
|<span data-ttu-id="e28a5-150">Доступно перед **saveChanges**</span><span class="sxs-lookup"><span data-stu-id="e28a5-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="e28a5-151">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="e28a5-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="e28a5-152">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="e28a5-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="e28a5-153">Для сообщений да.</span><span class="sxs-lookup"><span data-stu-id="e28a5-153">For messages, Yes.</span></span> <span data-ttu-id="e28a5-154">Для других это зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="e28a5-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="e28a5-155">Изменено в операции копирования</span><span class="sxs-lookup"><span data-stu-id="e28a5-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="e28a5-156">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-156">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-157">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-157">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-158">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-158">No</span></span>  <br/> |
|<span data-ttu-id="e28a5-159">Изменение клиента после копирования</span><span class="sxs-lookup"><span data-stu-id="e28a5-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="e28a5-160">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-160">No</span></span>  <br/> |<span data-ttu-id="e28a5-161">Нет</span><span class="sxs-lookup"><span data-stu-id="e28a5-161">No</span></span>  <br/> |<span data-ttu-id="e28a5-162">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-162">Yes</span></span>  <br/> |
|<span data-ttu-id="e28a5-163">Уникальный в ...</span><span class="sxs-lookup"><span data-stu-id="e28a5-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="e28a5-164">Весь мир</span><span class="sxs-lookup"><span data-stu-id="e28a5-164">Entire world</span></span>  <br/> |<span data-ttu-id="e28a5-165">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="e28a5-165">Provider instance</span></span>  <br/> |<span data-ttu-id="e28a5-166">Весь мир</span><span class="sxs-lookup"><span data-stu-id="e28a5-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="e28a5-167">Двоичная сопоставимая (как с memcmp)</span><span class="sxs-lookup"><span data-stu-id="e28a5-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="e28a5-168">Нет - используйте [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="e28a5-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="e28a5-169">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-169">Yes</span></span>  <br/> |<span data-ttu-id="e28a5-170">Да</span><span class="sxs-lookup"><span data-stu-id="e28a5-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e28a5-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e28a5-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e28a5-172">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e28a5-172">Protocol specifications</span></span>

<span data-ttu-id="e28a5-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e28a5-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e28a5-174">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="e28a5-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e28a5-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e28a5-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e28a5-176">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="e28a5-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e28a5-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e28a5-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e28a5-178">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e28a5-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e28a5-179">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e28a5-179">Header files</span></span>

<span data-ttu-id="e28a5-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e28a5-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="e28a5-181">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e28a5-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="e28a5-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e28a5-182">Mapitags.h</span></span>
  
> <span data-ttu-id="e28a5-183">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e28a5-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e28a5-184">См. также</span><span class="sxs-lookup"><span data-stu-id="e28a5-184">See also</span></span>



[<span data-ttu-id="e28a5-185">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="e28a5-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="e28a5-186">Каноническое свойство PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="e28a5-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="e28a5-187">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e28a5-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e28a5-188">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e28a5-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e28a5-189">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e28a5-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e28a5-190">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e28a5-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

