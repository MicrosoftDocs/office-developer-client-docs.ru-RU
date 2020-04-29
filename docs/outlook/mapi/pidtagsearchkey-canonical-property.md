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
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="073aa-103">Каноническое свойство PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="073aa-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="073aa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="073aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="073aa-105">Содержит ключ, сравнимый с двоичным кодом, который определяет коррелированные объекты для поиска.</span><span class="sxs-lookup"><span data-stu-id="073aa-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="073aa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="073aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="073aa-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="073aa-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="073aa-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="073aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="073aa-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="073aa-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="073aa-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="073aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="073aa-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="073aa-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="073aa-112">Область:</span><span class="sxs-lookup"><span data-stu-id="073aa-112">Area:</span></span>  <br/> |<span data-ttu-id="073aa-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="073aa-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="073aa-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="073aa-114">Remarks</span></span>

<span data-ttu-id="073aa-115">Это свойство предоставляет трассировку для связанных объектов, таких как копии сообщений, и облегчает поиск нежелательных экземпляров, таких как повторяющиеся получатели.</span><span class="sxs-lookup"><span data-stu-id="073aa-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="073aa-116">MAPI использует определенные правила для создания ключей поиска для получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="073aa-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="073aa-117">Ключ поиска формируется путем сцепления типа адреса (в верхнем регистре), знака двоеточия ":", адреса электронной почты в канонической форме и завершающего знака null.</span><span class="sxs-lookup"><span data-stu-id="073aa-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="073aa-118">Каноническую форму это означает, что адреса с учетом регистра отображаются в правильном регистре, а адреса без учета регистра преобразуются в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="073aa-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="073aa-119">Это важно для сохранения корреляции между сообщениями.</span><span class="sxs-lookup"><span data-stu-id="073aa-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="073aa-120">Для объектов Message это свойство доступно через метод [IMAPIProp::-PROPS](imapiprop-getprops.md) сразу после создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="073aa-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="073aa-121">Для других объектов он доступен после первого вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="073aa-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="073aa-122">Так как это свойство является изменяемым, его можно получить с помощью метода- **PROPS** до тех пор, пока вызов **SaveChanges** не зафиксирует какие-либо значения, установленные или измененные методом [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="073aa-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="073aa-123">В случае профилей MAPI также послужит жестко закодированным разделом профиля с именем **MUID_PROFILE_INSTANCE**, в котором это свойство является одним свойством.</span><span class="sxs-lookup"><span data-stu-id="073aa-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="073aa-124">Этот ключ гарантированно уникален среди всех созданных профилей и может быть более надежным, чем свойство **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), которое может быть, например, удалено и создано повторно с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="073aa-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="073aa-125">В следующей таблице приведены важные различия между **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и этим свойством.</span><span class="sxs-lookup"><span data-stu-id="073aa-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="073aa-126">**Характеристика**</span><span class="sxs-lookup"><span data-stu-id="073aa-126">**Characteristic**</span></span>|<span data-ttu-id="073aa-127">PR_ENTRYID \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="073aa-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="073aa-128">PR_RECORD_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="073aa-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="073aa-129">PR_SEARCH_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="073aa-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="073aa-130">Обязательный атрибут для объектов вложений</span><span class="sxs-lookup"><span data-stu-id="073aa-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="073aa-131">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-131">No</span></span>  <br/> |<span data-ttu-id="073aa-132">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-132">Yes</span></span>  <br/> |<span data-ttu-id="073aa-133">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-133">No</span></span>  <br/> |
|<span data-ttu-id="073aa-134">Обязательный атрибут для объектов Folder</span><span class="sxs-lookup"><span data-stu-id="073aa-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="073aa-135">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-135">Yes</span></span>  <br/> |<span data-ttu-id="073aa-136">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-136">Yes</span></span>  <br/> |<span data-ttu-id="073aa-137">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-137">No</span></span>  <br/> |
|<span data-ttu-id="073aa-138">Обязательный для объектов хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="073aa-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="073aa-139">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-139">Yes</span></span>  <br/> |<span data-ttu-id="073aa-140">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-140">Yes</span></span>  <br/> |<span data-ttu-id="073aa-141">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-141">No</span></span>  <br/> |
|<span data-ttu-id="073aa-142">Обязательные для объектов Status</span><span class="sxs-lookup"><span data-stu-id="073aa-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="073aa-143">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-143">Yes</span></span>  <br/> |<span data-ttu-id="073aa-144">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-144">No</span></span>  <br/> |<span data-ttu-id="073aa-145">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-145">No</span></span>  <br/> |
|<span data-ttu-id="073aa-146">Создаваемое клиентом</span><span class="sxs-lookup"><span data-stu-id="073aa-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="073aa-147">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-147">No</span></span>  <br/> |<span data-ttu-id="073aa-148">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-148">No</span></span>  <br/> |<span data-ttu-id="073aa-149">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-149">Yes</span></span>  <br/> |
|<span data-ttu-id="073aa-150">Доступно перед **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="073aa-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="073aa-151">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="073aa-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="073aa-152">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="073aa-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="073aa-153">Для сообщений — да.</span><span class="sxs-lookup"><span data-stu-id="073aa-153">For messages, Yes.</span></span> <span data-ttu-id="073aa-154">Для других пользователей это зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="073aa-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="073aa-155">Изменено в операции копирования</span><span class="sxs-lookup"><span data-stu-id="073aa-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="073aa-156">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-156">Yes</span></span>  <br/> |<span data-ttu-id="073aa-157">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-157">Yes</span></span>  <br/> |<span data-ttu-id="073aa-158">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-158">No</span></span>  <br/> |
|<span data-ttu-id="073aa-159">Изменение клиентом после копирования</span><span class="sxs-lookup"><span data-stu-id="073aa-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="073aa-160">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-160">No</span></span>  <br/> |<span data-ttu-id="073aa-161">Нет</span><span class="sxs-lookup"><span data-stu-id="073aa-161">No</span></span>  <br/> |<span data-ttu-id="073aa-162">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-162">Yes</span></span>  <br/> |
|<span data-ttu-id="073aa-163">Уникальный в пределах...</span><span class="sxs-lookup"><span data-stu-id="073aa-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="073aa-164">Весь мир</span><span class="sxs-lookup"><span data-stu-id="073aa-164">Entire world</span></span>  <br/> |<span data-ttu-id="073aa-165">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="073aa-165">Provider instance</span></span>  <br/> |<span data-ttu-id="073aa-166">Весь мир</span><span class="sxs-lookup"><span data-stu-id="073aa-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="073aa-167">Сравнение двоичных файлов (как и в случае с мемкмп)</span><span class="sxs-lookup"><span data-stu-id="073aa-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="073aa-168">Нет — используйте [имаписуппорт:: метод compareentryids](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="073aa-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="073aa-169">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-169">Yes</span></span>  <br/> |<span data-ttu-id="073aa-170">Да</span><span class="sxs-lookup"><span data-stu-id="073aa-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="073aa-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="073aa-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="073aa-172">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="073aa-172">Protocol specifications</span></span>

<span data-ttu-id="073aa-173">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073aa-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073aa-174">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="073aa-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="073aa-175">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073aa-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073aa-176">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="073aa-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="073aa-177">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073aa-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073aa-178">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="073aa-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="073aa-179">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="073aa-179">Header files</span></span>

<span data-ttu-id="073aa-180">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="073aa-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="073aa-181">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="073aa-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="073aa-182">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="073aa-182">Mapitags.h</span></span>
  
> <span data-ttu-id="073aa-183">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="073aa-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="073aa-184">См. также</span><span class="sxs-lookup"><span data-stu-id="073aa-184">See also</span></span>



[<span data-ttu-id="073aa-185">Каноническое свойство PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="073aa-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="073aa-186">Каноническое свойство PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="073aa-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="073aa-187">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="073aa-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="073aa-188">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="073aa-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="073aa-189">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="073aa-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="073aa-190">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="073aa-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

