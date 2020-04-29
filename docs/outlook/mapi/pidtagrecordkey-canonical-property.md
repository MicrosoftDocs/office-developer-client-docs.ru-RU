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
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="c5d72-103">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="c5d72-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="c5d72-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5d72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5d72-105">Содержит уникальный двоичный код, сравнимый с двоичным кодом для определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="c5d72-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5d72-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c5d72-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5d72-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="c5d72-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="c5d72-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c5d72-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5d72-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="c5d72-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="c5d72-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c5d72-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5d72-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c5d72-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c5d72-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c5d72-112">Area:</span></span>  <br/> |<span data-ttu-id="c5d72-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="c5d72-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5d72-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5d72-114">Remarks</span></span>

<span data-ttu-id="c5d72-115">Это свойство облегчает поиск ссылок на объект, например поиск строки в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="c5d72-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="c5d72-116">Это свойство невозможно использовать для открытия объекта; Используйте идентификатор записи для этой цели.</span><span class="sxs-lookup"><span data-stu-id="c5d72-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="c5d72-117">Это свойство должно однозначно определять вложенный в сообщение вложенный вложенный объект.</span><span class="sxs-lookup"><span data-stu-id="c5d72-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="c5d72-118">Этот идентификатор является единственной гарантией вложения, которая гарантированно остается неизменной после закрытия и повторного открытия сообщения.</span><span class="sxs-lookup"><span data-stu-id="c5d72-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="c5d72-119">Чтобы гарантировать эту гарантию, поставщик хранилища должен сохранить это свойство в сеансах.</span><span class="sxs-lookup"><span data-stu-id="c5d72-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="c5d72-120">Для папок это свойство содержит ключ, используемый в таблице иерархия папок.</span><span class="sxs-lookup"><span data-stu-id="c5d72-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="c5d72-121">Как правило, это то же значение, которое предоставляется свойством **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c5d72-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c5d72-122">Для хранилищ сообщений это свойство идентично свойству **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c5d72-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c5d72-123">В объекте хранилища сообщений это свойство должно быть уникальным для всех поставщиков хранилищ.</span><span class="sxs-lookup"><span data-stu-id="c5d72-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="c5d72-124">Один из способов сделать это — объединить значение свойства **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) для хранилища (от уникального к этому типу поставщика) с использованием структуры [GUID](guid.md) или другого значения, уникального для конкретного хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5d72-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="c5d72-125">Это свойство всегда доступно с помощью метода [IMAPIProp::-PROPS](imapiprop-getprops.md) , следующего за первым вызовом метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d72-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="c5d72-126">Некоторые поставщики могут сделать его доступным сразу же после создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c5d72-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="c5d72-127">Клиент или поставщик услуг может сравнить значения этого свойства с помощью мемкмп.</span><span class="sxs-lookup"><span data-stu-id="c5d72-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="c5d72-128">Это невозможно сделать для значений идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="c5d72-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="c5d72-129">Тем не менее, это свойство обязательно должно быть уникальным в том же хранилище сообщений или в контейнере адресной книги; два объекта из разных контейнеров могут иметь одно и то же значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c5d72-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="c5d72-130">Одно из различий между ключами записи и поиска состоит в том, что ключ записи относится только к объекту, а ключ поиска может быть скопирован в другие объекты.</span><span class="sxs-lookup"><span data-stu-id="c5d72-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="c5d72-131">Например, две копии объекта могут иметь одно и то же значение **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), но для этого свойства должны быть заданы разные значения.</span><span class="sxs-lookup"><span data-stu-id="c5d72-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="c5d72-132">В следующей таблице приведены важные различия между **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) и этим свойством.</span><span class="sxs-lookup"><span data-stu-id="c5d72-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="c5d72-133">**Характеристика**</span><span class="sxs-lookup"><span data-stu-id="c5d72-133">**Characteristic**</span></span>|<span data-ttu-id="c5d72-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="c5d72-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="c5d72-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="c5d72-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="c5d72-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="c5d72-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5d72-137">Обязательный атрибут для объектов вложений</span><span class="sxs-lookup"><span data-stu-id="c5d72-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="c5d72-138">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-138">No</span></span>  <br/> |<span data-ttu-id="c5d72-139">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-139">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-140">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-140">No</span></span>  <br/> |
|<span data-ttu-id="c5d72-141">Обязательный атрибут для объектов Folder</span><span class="sxs-lookup"><span data-stu-id="c5d72-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="c5d72-142">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-142">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-143">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-143">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-144">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-144">No</span></span>  <br/> |
|<span data-ttu-id="c5d72-145">Обязательный для объектов хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="c5d72-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="c5d72-146">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-146">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-147">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-147">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-148">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-148">No</span></span>  <br/> |
|<span data-ttu-id="c5d72-149">Обязательные для объектов Status</span><span class="sxs-lookup"><span data-stu-id="c5d72-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="c5d72-150">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-150">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-151">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-151">No</span></span>  <br/> |<span data-ttu-id="c5d72-152">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-152">No</span></span>  <br/> |
|<span data-ttu-id="c5d72-153">Создаваемое клиентом</span><span class="sxs-lookup"><span data-stu-id="c5d72-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="c5d72-154">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-154">No</span></span>  <br/> |<span data-ttu-id="c5d72-155">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-155">No</span></span>  <br/> |<span data-ttu-id="c5d72-156">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-156">Yes</span></span>  <br/> |
|<span data-ttu-id="c5d72-157">Доступно до вызова **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="c5d72-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="c5d72-158">Возможно</span><span class="sxs-lookup"><span data-stu-id="c5d72-158">Maybe</span></span>  <br/> |<span data-ttu-id="c5d72-159">Возможно</span><span class="sxs-lookup"><span data-stu-id="c5d72-159">Maybe</span></span>  <br/> |<span data-ttu-id="c5d72-160">Сообщения Да, другие могут быть</span><span class="sxs-lookup"><span data-stu-id="c5d72-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="c5d72-161">Изменено в операции копирования</span><span class="sxs-lookup"><span data-stu-id="c5d72-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="c5d72-162">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-162">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-163">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-163">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-164">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-164">No</span></span>  <br/> |
|<span data-ttu-id="c5d72-165">Изменение клиентом после копирования</span><span class="sxs-lookup"><span data-stu-id="c5d72-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="c5d72-166">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-166">No</span></span>  <br/> |<span data-ttu-id="c5d72-167">Нет</span><span class="sxs-lookup"><span data-stu-id="c5d72-167">No</span></span>  <br/> |<span data-ttu-id="c5d72-168">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-168">Yes</span></span>  <br/> |
|<span data-ttu-id="c5d72-169">Уникальный в пределах...</span><span class="sxs-lookup"><span data-stu-id="c5d72-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="c5d72-170">Весь мир</span><span class="sxs-lookup"><span data-stu-id="c5d72-170">Entire world</span></span>  <br/> |<span data-ttu-id="c5d72-171">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="c5d72-171">Provider instance</span></span>  <br/> |<span data-ttu-id="c5d72-172">Весь мир</span><span class="sxs-lookup"><span data-stu-id="c5d72-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="c5d72-173">Сравнение двоичных файлов (как и в случае с мемкмп)</span><span class="sxs-lookup"><span data-stu-id="c5d72-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="c5d72-174">Нет — используйте **имаписуппорт:: метод compareentryids**</span><span class="sxs-lookup"><span data-stu-id="c5d72-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="c5d72-175">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-175">Yes</span></span>  <br/> |<span data-ttu-id="c5d72-176">Да</span><span class="sxs-lookup"><span data-stu-id="c5d72-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c5d72-177">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5d72-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5d72-178">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c5d72-178">Protocol specifications</span></span>

<span data-ttu-id="c5d72-179">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5d72-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5d72-180">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c5d72-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5d72-181">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5d72-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5d72-182">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="c5d72-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c5d72-183">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5d72-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5d72-184">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5d72-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5d72-185">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c5d72-185">Header files</span></span>

<span data-ttu-id="c5d72-186">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c5d72-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5d72-187">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c5d72-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5d72-188">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c5d72-188">Mapitags.h</span></span>
  
> <span data-ttu-id="c5d72-189">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c5d72-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5d72-190">См. также</span><span class="sxs-lookup"><span data-stu-id="c5d72-190">See also</span></span>



[<span data-ttu-id="c5d72-191">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5d72-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5d72-192">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c5d72-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5d72-193">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c5d72-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5d72-194">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c5d72-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

