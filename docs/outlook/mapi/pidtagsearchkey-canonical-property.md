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
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="7b296-103">Каноническое свойство PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="7b296-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="7b296-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b296-105">Содержит схожий двоичный ключ, который идентифицирует связанные объекты для поиска.</span><span class="sxs-lookup"><span data-stu-id="7b296-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b296-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7b296-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b296-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="7b296-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="7b296-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7b296-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b296-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="7b296-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="7b296-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7b296-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b296-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7b296-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7b296-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7b296-112">Area:</span></span>  <br/> |<span data-ttu-id="7b296-113">Свойства ID</span><span class="sxs-lookup"><span data-stu-id="7b296-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b296-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b296-114">Remarks</span></span>

<span data-ttu-id="7b296-115">Это свойство обеспечивает трассировка связанных объектов, таких как копии сообщений, и упрощает поиск нежелательных вхождений, таких как дублирующиеся получатели.</span><span class="sxs-lookup"><span data-stu-id="7b296-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="7b296-116">MAPI использует определенные правила для создания ключей поиска для получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b296-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="7b296-117">Ключ поиска формируется путем сбиения типа адреса (в верхнем регистре), двоеточия ":", адреса электронной почты в канонической форме и завершающего символа null.</span><span class="sxs-lookup"><span data-stu-id="7b296-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="7b296-118">Каноническая форма здесь означает, что адреса с регистром отображаются в правильном случае, а адреса, не чувствительные к регистру, преобразуются в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="7b296-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="7b296-119">Это важно для сохранения корреляций между сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7b296-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="7b296-120">Для объектов сообщений это свойство доступно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) сразу после создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="7b296-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="7b296-121">Для других объектов он доступен после первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="7b296-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="7b296-122">Так как это свойство является изменяемым, его невозможно получить через **GetProps,** пока вызов **SaveChanges** не заблокировает значения, установленные или измененные методом [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="7b296-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="7b296-123">Для профилей MAPI также передает жестко заданная часть профиля с именем **MUID_PROFILE_INSTANCE**, с этим свойством в качестве одного свойства.</span><span class="sxs-lookup"><span data-stu-id="7b296-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="7b296-124">Этот ключ гарантированно будет уникальным для всех когда-либо созданных профилей и может быть более надежным, чем **свойство PR_PROFILE_NAME** ([PidTagProfileName),](pidtagprofilename-canonical-property.md)которое может быть, например, удалено и повторно создано с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="7b296-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="7b296-125">В следующей таблице водятся  важные различия между PR_ENTRYID [(PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)и этим свойством.</span><span class="sxs-lookup"><span data-stu-id="7b296-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="7b296-126">**Характеристика**</span><span class="sxs-lookup"><span data-stu-id="7b296-126">**Characteristic**</span></span>|<span data-ttu-id="7b296-127">PR_ENTRYID\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7b296-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="7b296-128">PR_RECORD_KEY\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7b296-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="7b296-129">PR_SEARCH_KEY\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7b296-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b296-130">Требуется для объектов вложений</span><span class="sxs-lookup"><span data-stu-id="7b296-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="7b296-131">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-131">No</span></span>  <br/> |<span data-ttu-id="7b296-132">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-132">Yes</span></span>  <br/> |<span data-ttu-id="7b296-133">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-133">No</span></span>  <br/> |
|<span data-ttu-id="7b296-134">Требуется для объектов папок</span><span class="sxs-lookup"><span data-stu-id="7b296-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="7b296-135">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-135">Yes</span></span>  <br/> |<span data-ttu-id="7b296-136">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-136">Yes</span></span>  <br/> |<span data-ttu-id="7b296-137">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-137">No</span></span>  <br/> |
|<span data-ttu-id="7b296-138">Требуется для объектов, хранимых в сообщениях</span><span class="sxs-lookup"><span data-stu-id="7b296-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="7b296-139">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-139">Yes</span></span>  <br/> |<span data-ttu-id="7b296-140">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-140">Yes</span></span>  <br/> |<span data-ttu-id="7b296-141">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-141">No</span></span>  <br/> |
|<span data-ttu-id="7b296-142">Требуется для объектов состояния</span><span class="sxs-lookup"><span data-stu-id="7b296-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="7b296-143">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-143">Yes</span></span>  <br/> |<span data-ttu-id="7b296-144">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-144">No</span></span>  <br/> |<span data-ttu-id="7b296-145">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-145">No</span></span>  <br/> |
|<span data-ttu-id="7b296-146">Можно с помощью клиента</span><span class="sxs-lookup"><span data-stu-id="7b296-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="7b296-147">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-147">No</span></span>  <br/> |<span data-ttu-id="7b296-148">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-148">No</span></span>  <br/> |<span data-ttu-id="7b296-149">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-149">Yes</span></span>  <br/> |
|<span data-ttu-id="7b296-150">Доступно до **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="7b296-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="7b296-151">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="7b296-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="7b296-152">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="7b296-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="7b296-153">Да, для сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b296-153">For messages, Yes.</span></span> <span data-ttu-id="7b296-154">Для других это зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="7b296-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="7b296-155">Изменено в операции копирования</span><span class="sxs-lookup"><span data-stu-id="7b296-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="7b296-156">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-156">Yes</span></span>  <br/> |<span data-ttu-id="7b296-157">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-157">Yes</span></span>  <br/> |<span data-ttu-id="7b296-158">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-158">No</span></span>  <br/> |
|<span data-ttu-id="7b296-159">Может изменяться клиентом после копирования</span><span class="sxs-lookup"><span data-stu-id="7b296-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="7b296-160">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-160">No</span></span>  <br/> |<span data-ttu-id="7b296-161">Нет</span><span class="sxs-lookup"><span data-stu-id="7b296-161">No</span></span>  <br/> |<span data-ttu-id="7b296-162">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-162">Yes</span></span>  <br/> |
|<span data-ttu-id="7b296-163">Уникальный в ...</span><span class="sxs-lookup"><span data-stu-id="7b296-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="7b296-164">Весь мир</span><span class="sxs-lookup"><span data-stu-id="7b296-164">Entire world</span></span>  <br/> |<span data-ttu-id="7b296-165">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="7b296-165">Provider instance</span></span>  <br/> |<span data-ttu-id="7b296-166">Весь мир</span><span class="sxs-lookup"><span data-stu-id="7b296-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="7b296-167">Двоичное сравнимое (как с memcmp)</span><span class="sxs-lookup"><span data-stu-id="7b296-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="7b296-168">Нет — используйте [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="7b296-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="7b296-169">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-169">Yes</span></span>  <br/> |<span data-ttu-id="7b296-170">Да</span><span class="sxs-lookup"><span data-stu-id="7b296-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7b296-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b296-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b296-172">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7b296-172">Protocol specifications</span></span>

<span data-ttu-id="7b296-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b296-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b296-174">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="7b296-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b296-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b296-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b296-176">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="7b296-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7b296-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b296-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b296-178">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b296-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b296-179">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="7b296-179">Header files</span></span>

<span data-ttu-id="7b296-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b296-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b296-181">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b296-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b296-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b296-182">Mapitags.h</span></span>
  
> <span data-ttu-id="7b296-183">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7b296-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b296-184">См. также</span><span class="sxs-lookup"><span data-stu-id="7b296-184">See also</span></span>



[<span data-ttu-id="7b296-185">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="7b296-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="7b296-186">Каноническое свойство PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="7b296-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="7b296-187">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b296-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b296-188">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b296-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b296-189">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7b296-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b296-190">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7b296-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

