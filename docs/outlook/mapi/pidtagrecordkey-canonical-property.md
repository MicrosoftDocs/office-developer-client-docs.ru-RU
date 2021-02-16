---
title: Каноническое свойство PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355267"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="e095e-103">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="e095e-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="e095e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e095e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e095e-105">Содержит уникальный схожий двоичный идентификатор для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="e095e-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e095e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e095e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e095e-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="e095e-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="e095e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e095e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e095e-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="e095e-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="e095e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e095e-110">Data type:</span></span>  <br/> |<span data-ttu-id="e095e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e095e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e095e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e095e-112">Area:</span></span>  <br/> |<span data-ttu-id="e095e-113">Свойства ID</span><span class="sxs-lookup"><span data-stu-id="e095e-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e095e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e095e-114">Remarks</span></span>

<span data-ttu-id="e095e-115">Это свойство упрощает поиск ссылок на объект, например поиск его строки в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="e095e-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="e095e-116">Это свойство нельзя использовать для открытия объекта; используйте идентификатор записи для этой цели.</span><span class="sxs-lookup"><span data-stu-id="e095e-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="e095e-117">Это свойство должно уникальным образом идентифицировать подпроект вложения в сообщении.</span><span class="sxs-lookup"><span data-stu-id="e095e-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="e095e-118">Этот идентификатор является единственной характеристикой вложения, которая гарантированно остается такой же после закрытия и повторного открытия сообщения.</span><span class="sxs-lookup"><span data-stu-id="e095e-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="e095e-119">Поставщик магазина должен сохранить это свойство во время сеансов, чтобы обеспечить эту гарантию.</span><span class="sxs-lookup"><span data-stu-id="e095e-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="e095e-120">Для папок это свойство содержит ключ, используемый в таблице иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="e095e-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="e095e-121">Обычно это то же значение, что и в свойстве **PR_ENTRYID** ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e095e-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e095e-122">Для хранилищ сообщений это свойство идентично свойству **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey).](pidtagstorerecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e095e-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e095e-123">В объекте хранения сообщений это свойство должно быть уникальным для всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="e095e-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="e095e-124">Один из способов сделать это — объединить значение свойства **PR_MDB_PROVIDER** ([PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)для магазина (уникально для этого типа поставщика) со структурой [GUID](guid.md) или другим значением, уникальным для конкретного хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e095e-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="e095e-125">Это свойство всегда доступно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) после первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="e095e-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="e095e-126">Некоторые поставщики могут сделать его доступным сразу же после его искомой службы.</span><span class="sxs-lookup"><span data-stu-id="e095e-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="e095e-127">Клиент или поставщик услуг может сравнить значения из этого свойства с помощью memcmp.</span><span class="sxs-lookup"><span data-stu-id="e095e-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="e095e-128">Это невозможно для значений идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="e095e-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="e095e-129">Однако это свойство гарантированно будет уникальным в том же хранилище сообщений или контейнере адресной книги; два объекта из разных контейнеров могут иметь одинаковое значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e095e-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="e095e-130">Одним различием между записью и ключами поиска является то, что ключ записи является специфическим для объекта, тогда как ключ поиска можно скопировать в другие объекты.</span><span class="sxs-lookup"><span data-stu-id="e095e-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="e095e-131">Например, две копии объекта могут иметь одно и то же значение **PR_SEARCH_KEY** ([PidTagSearchKey),](pidtagsearchkey-canonical-property.md)но должны иметь разные значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e095e-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="e095e-132">В следующей таблице скомплены важные различия между **PR_ENTRYID,** **PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)и этим свойством.</span><span class="sxs-lookup"><span data-stu-id="e095e-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="e095e-133">**Характеристика**</span><span class="sxs-lookup"><span data-stu-id="e095e-133">**Characteristic**</span></span>|<span data-ttu-id="e095e-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e095e-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="e095e-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="e095e-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="e095e-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="e095e-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e095e-137">Требуется для объектов вложений</span><span class="sxs-lookup"><span data-stu-id="e095e-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="e095e-138">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-138">No</span></span>  <br/> |<span data-ttu-id="e095e-139">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-139">Yes</span></span>  <br/> |<span data-ttu-id="e095e-140">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-140">No</span></span>  <br/> |
|<span data-ttu-id="e095e-141">Требуется для объектов папок</span><span class="sxs-lookup"><span data-stu-id="e095e-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="e095e-142">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-142">Yes</span></span>  <br/> |<span data-ttu-id="e095e-143">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-143">Yes</span></span>  <br/> |<span data-ttu-id="e095e-144">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-144">No</span></span>  <br/> |
|<span data-ttu-id="e095e-145">Требуется для объектов, хранимых в сообщениях</span><span class="sxs-lookup"><span data-stu-id="e095e-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="e095e-146">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-146">Yes</span></span>  <br/> |<span data-ttu-id="e095e-147">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-147">Yes</span></span>  <br/> |<span data-ttu-id="e095e-148">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-148">No</span></span>  <br/> |
|<span data-ttu-id="e095e-149">Требуется для объектов состояния</span><span class="sxs-lookup"><span data-stu-id="e095e-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="e095e-150">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-150">Yes</span></span>  <br/> |<span data-ttu-id="e095e-151">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-151">No</span></span>  <br/> |<span data-ttu-id="e095e-152">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-152">No</span></span>  <br/> |
|<span data-ttu-id="e095e-153">Можно с помощью клиента</span><span class="sxs-lookup"><span data-stu-id="e095e-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="e095e-154">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-154">No</span></span>  <br/> |<span data-ttu-id="e095e-155">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-155">No</span></span>  <br/> |<span data-ttu-id="e095e-156">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-156">Yes</span></span>  <br/> |
|<span data-ttu-id="e095e-157">Доступно перед вызовом **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="e095e-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="e095e-158">Возможно,</span><span class="sxs-lookup"><span data-stu-id="e095e-158">Maybe</span></span>  <br/> |<span data-ttu-id="e095e-159">Возможно,</span><span class="sxs-lookup"><span data-stu-id="e095e-159">Maybe</span></span>  <br/> |<span data-ttu-id="e095e-160">Messages Yes Others Maybe</span><span class="sxs-lookup"><span data-stu-id="e095e-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="e095e-161">Изменено в операции копирования</span><span class="sxs-lookup"><span data-stu-id="e095e-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="e095e-162">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-162">Yes</span></span>  <br/> |<span data-ttu-id="e095e-163">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-163">Yes</span></span>  <br/> |<span data-ttu-id="e095e-164">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-164">No</span></span>  <br/> |
|<span data-ttu-id="e095e-165">Изменение клиентом после копирования</span><span class="sxs-lookup"><span data-stu-id="e095e-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="e095e-166">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-166">No</span></span>  <br/> |<span data-ttu-id="e095e-167">Нет</span><span class="sxs-lookup"><span data-stu-id="e095e-167">No</span></span>  <br/> |<span data-ttu-id="e095e-168">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-168">Yes</span></span>  <br/> |
|<span data-ttu-id="e095e-169">Уникальный в ...</span><span class="sxs-lookup"><span data-stu-id="e095e-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="e095e-170">Весь мир</span><span class="sxs-lookup"><span data-stu-id="e095e-170">Entire world</span></span>  <br/> |<span data-ttu-id="e095e-171">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="e095e-171">Provider instance</span></span>  <br/> |<span data-ttu-id="e095e-172">Весь мир</span><span class="sxs-lookup"><span data-stu-id="e095e-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="e095e-173">Двоичное сравнимое (как с memcmp)</span><span class="sxs-lookup"><span data-stu-id="e095e-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="e095e-174">Нет — используйте **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="e095e-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="e095e-175">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-175">Yes</span></span>  <br/> |<span data-ttu-id="e095e-176">Да</span><span class="sxs-lookup"><span data-stu-id="e095e-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e095e-177">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e095e-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e095e-178">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e095e-178">Protocol specifications</span></span>

<span data-ttu-id="e095e-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e095e-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e095e-180">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="e095e-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e095e-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e095e-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e095e-182">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="e095e-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e095e-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e095e-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e095e-184">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e095e-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e095e-185">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="e095e-185">Header files</span></span>

<span data-ttu-id="e095e-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e095e-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="e095e-187">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e095e-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="e095e-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e095e-188">Mapitags.h</span></span>
  
> <span data-ttu-id="e095e-189">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e095e-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e095e-190">См. также</span><span class="sxs-lookup"><span data-stu-id="e095e-190">See also</span></span>



[<span data-ttu-id="e095e-191">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e095e-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e095e-192">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e095e-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e095e-193">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e095e-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e095e-194">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e095e-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

