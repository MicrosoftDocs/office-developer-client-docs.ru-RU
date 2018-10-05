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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401701"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="11f0e-103">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="11f0e-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="11f0e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11f0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11f0e-105">Содержит уникальный идентификатор, сравнимые двоичный для определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="11f0e-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11f0e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="11f0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11f0e-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="11f0e-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="11f0e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="11f0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11f0e-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="11f0e-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="11f0e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="11f0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="11f0e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="11f0e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="11f0e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="11f0e-112">Area:</span></span>  <br/> |<span data-ttu-id="11f0e-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="11f0e-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11f0e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="11f0e-114">Remarks</span></span>

<span data-ttu-id="11f0e-115">Это свойство облегчает опорную ссылки на объект, например поиск его строку в таблице содержимое.</span><span class="sxs-lookup"><span data-stu-id="11f0e-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="11f0e-116">Это свойство не может использоваться для открытия объекта; для этого используется идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="11f0e-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="11f0e-117">Вложенные объекты вложения необходимо однозначно определить в сообщении этим свойством.</span><span class="sxs-lookup"><span data-stu-id="11f0e-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="11f0e-118">Этот идентификатор является единственным характеристика вложения, обязательно не изменяются после закрытия и повторно открыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="11f0e-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="11f0e-119">Поставщик хранения должны сохранить это свойство между сеансами, чтобы убедиться в этом гарантии.</span><span class="sxs-lookup"><span data-stu-id="11f0e-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="11f0e-120">Для папок это свойство содержит ключ, используемый в таблице иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="11f0e-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="11f0e-121">Обычно это совпадает со значением, которое указано в свойстве **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11f0e-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="11f0e-122">Для хранилищ сообщений это свойство идентичен свойство **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11f0e-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="11f0e-123">В объекте хранилища сообщений это свойство должен быть уникальным среди всех поставщиков хранилища.</span><span class="sxs-lookup"><span data-stu-id="11f0e-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="11f0e-124">Одним из способов сделать это является объединение значение свойства **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) для хранилища (уникальный для данного типа поставщика) с [GUID](guid.md) структура или другое значение, уникальным для хранилища определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="11f0e-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="11f0e-125">Это свойство всегда доступен через метод [IMAPIProp::GetProps](imapiprop-getprops.md) после первого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="11f0e-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="11f0e-126">Некоторые поставщики можно сделать его доступным сразу же после создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11f0e-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="11f0e-127">Клиент или служба поставщика позволяет сравнивать значения этого свойства с помощью memcmp.</span><span class="sxs-lookup"><span data-stu-id="11f0e-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="11f0e-128">Это невозможно для значений идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="11f0e-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="11f0e-129">Тем не менее это свойство обязательно должен быть уникальным в пределах одного хранилища сообщений или адресной книги контейнера; два объекта из разных контейнеров может иметь такое же значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="11f0e-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="11f0e-130">Один различие между ключи поиска и записи, что ключ записи специально для объекта, тогда как ключ поиска могут быть скопированы в другие объекты.</span><span class="sxs-lookup"><span data-stu-id="11f0e-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="11f0e-131">К примеру двух копий объекта может иметь такое же значение **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), но должны иметь разные значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="11f0e-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="11f0e-132">В следующей таблице представлены важные различия между **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) и это свойство.</span><span class="sxs-lookup"><span data-stu-id="11f0e-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="11f0e-133">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="11f0e-133">**Characteristic**</span></span>|<span data-ttu-id="11f0e-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="11f0e-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="11f0e-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="11f0e-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="11f0e-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="11f0e-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="11f0e-137">Требуется на объекты вложения</span><span class="sxs-lookup"><span data-stu-id="11f0e-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="11f0e-138">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-138">No</span></span>  <br/> |<span data-ttu-id="11f0e-139">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-139">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-140">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-140">No</span></span>  <br/> |
|<span data-ttu-id="11f0e-141">Требуется на объектов папок</span><span class="sxs-lookup"><span data-stu-id="11f0e-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="11f0e-142">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-142">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-143">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-143">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-144">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-144">No</span></span>  <br/> |
|<span data-ttu-id="11f0e-145">Требуется на объектов хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="11f0e-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="11f0e-146">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-146">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-147">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-147">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-148">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-148">No</span></span>  <br/> |
|<span data-ttu-id="11f0e-149">Требуется на состояние объектов</span><span class="sxs-lookup"><span data-stu-id="11f0e-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="11f0e-150">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-150">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-151">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-151">No</span></span>  <br/> |<span data-ttu-id="11f0e-152">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-152">No</span></span>  <br/> |
|<span data-ttu-id="11f0e-153">Возможно создание клиентом</span><span class="sxs-lookup"><span data-stu-id="11f0e-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="11f0e-154">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-154">No</span></span>  <br/> |<span data-ttu-id="11f0e-155">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-155">No</span></span>  <br/> |<span data-ttu-id="11f0e-156">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-156">Yes</span></span>  <br/> |
|<span data-ttu-id="11f0e-157">Доступные до вызова **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="11f0e-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="11f0e-158">Может быть</span><span class="sxs-lookup"><span data-stu-id="11f0e-158">Maybe</span></span>  <br/> |<span data-ttu-id="11f0e-159">Может быть</span><span class="sxs-lookup"><span data-stu-id="11f0e-159">Maybe</span></span>  <br/> |<span data-ttu-id="11f0e-160">Другим пользователям может быть Yes сообщений</span><span class="sxs-lookup"><span data-stu-id="11f0e-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="11f0e-161">Изменения в операцию копирования</span><span class="sxs-lookup"><span data-stu-id="11f0e-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="11f0e-162">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-162">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-163">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-163">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-164">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-164">No</span></span>  <br/> |
|<span data-ttu-id="11f0e-165">Механизм клиента после копирования</span><span class="sxs-lookup"><span data-stu-id="11f0e-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="11f0e-166">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-166">No</span></span>  <br/> |<span data-ttu-id="11f0e-167">Нет</span><span class="sxs-lookup"><span data-stu-id="11f0e-167">No</span></span>  <br/> |<span data-ttu-id="11f0e-168">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-168">Yes</span></span>  <br/> |
|<span data-ttu-id="11f0e-169">Уникальный в пределах...</span><span class="sxs-lookup"><span data-stu-id="11f0e-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="11f0e-170">Весь мир</span><span class="sxs-lookup"><span data-stu-id="11f0e-170">Entire world</span></span>  <br/> |<span data-ttu-id="11f0e-171">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="11f0e-171">Provider instance</span></span>  <br/> |<span data-ttu-id="11f0e-172">Весь мир</span><span class="sxs-lookup"><span data-stu-id="11f0e-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="11f0e-173">Двоичный сравнимые (как с memcmp)</span><span class="sxs-lookup"><span data-stu-id="11f0e-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="11f0e-174">Нет — используйте **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="11f0e-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="11f0e-175">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-175">Yes</span></span>  <br/> |<span data-ttu-id="11f0e-176">Да</span><span class="sxs-lookup"><span data-stu-id="11f0e-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="11f0e-177">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="11f0e-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11f0e-178">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="11f0e-178">Protocol specifications</span></span>

<span data-ttu-id="11f0e-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11f0e-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11f0e-180">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="11f0e-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11f0e-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11f0e-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11f0e-182">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="11f0e-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="11f0e-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11f0e-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11f0e-184">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11f0e-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11f0e-185">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="11f0e-185">Header files</span></span>

<span data-ttu-id="11f0e-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11f0e-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="11f0e-187">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="11f0e-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="11f0e-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11f0e-188">Mapitags.h</span></span>
  
> <span data-ttu-id="11f0e-189">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="11f0e-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11f0e-190">См. также</span><span class="sxs-lookup"><span data-stu-id="11f0e-190">See also</span></span>



[<span data-ttu-id="11f0e-191">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="11f0e-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11f0e-192">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="11f0e-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11f0e-193">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="11f0e-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11f0e-194">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="11f0e-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

