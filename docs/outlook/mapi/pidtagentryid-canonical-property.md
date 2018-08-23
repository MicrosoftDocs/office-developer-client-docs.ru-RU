---
title: Каноническое свойство PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f3d49faba9d1e9cc8609ee55f7fb3c329e9ae947
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593041"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="53877-103">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="53877-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="53877-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53877-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53877-105">Содержит идентификатор запись MAPI, используемый для открытия и изменения свойств конкретного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="53877-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53877-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="53877-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53877-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="53877-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="53877-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="53877-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53877-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="53877-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="53877-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="53877-110">Data type:</span></span>  <br/> |<span data-ttu-id="53877-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="53877-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="53877-112">Область:</span><span class="sxs-lookup"><span data-stu-id="53877-112">Area:</span></span>  <br/> |<span data-ttu-id="53877-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="53877-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53877-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="53877-114">Remarks</span></span>

<span data-ttu-id="53877-115">Это свойство определяет объект для **OpenEntry** для создания экземпляра и предоставляет доступ ко всем его свойства через соответствующие производного интерфейса **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="53877-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="53877-116">Это свойство является одним из свойств базовый адрес для всех пользователей, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="53877-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="53877-117">Это свойство может содержать долгосрочные или краткосрочной идентификатор.</span><span class="sxs-lookup"><span data-stu-id="53877-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="53877-118">Краткосрочные идентификаторы, проще и быстрее конструкции, но не могут быть длиннее в области действия и длительность, обычно для текущего сеанса и рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="53877-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="53877-119">Они обычно используется для объектов временные характера, например строк таблицы или элементами диалогового окна и затем заброшены пользователями.</span><span class="sxs-lookup"><span data-stu-id="53877-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="53877-120">Долгосрочные идентификаторы используются для объектов более широкие и длительный характер.</span><span class="sxs-lookup"><span data-stu-id="53877-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="53877-121">Это свойство всегда доступен через метод [IMAPIProp::GetProps](imapiprop-getprops.md) после первого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="53877-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="53877-122">Некоторые поставщики услуг можно сделать его доступным сразу же после создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="53877-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="53877-123">Поставщик всегда должен возвращать долгосрочного идентификатор записи из **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="53877-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="53877-124">Таким образом, чтобы преобразовать идентификатор краткосрочных долгосрочного, просто откройте объект и получите его это свойство через **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="53877-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="53877-125">В следующей таблице представлены важные различия между это свойство **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53877-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="53877-126">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="53877-126">**Characteristic**</span></span>|<span data-ttu-id="53877-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="53877-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="53877-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="53877-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="53877-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="53877-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="53877-130">Требуется на объекты вложения</span><span class="sxs-lookup"><span data-stu-id="53877-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="53877-131">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-131">No</span></span>  <br/> |<span data-ttu-id="53877-132">Да</span><span class="sxs-lookup"><span data-stu-id="53877-132">Yes</span></span>  <br/> |<span data-ttu-id="53877-133">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-133">No</span></span>  <br/> |
|<span data-ttu-id="53877-134">Требуется на объектов папок</span><span class="sxs-lookup"><span data-stu-id="53877-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="53877-135">Да</span><span class="sxs-lookup"><span data-stu-id="53877-135">Yes</span></span>  <br/> |<span data-ttu-id="53877-136">Да</span><span class="sxs-lookup"><span data-stu-id="53877-136">Yes</span></span>  <br/> |<span data-ttu-id="53877-137">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-137">No</span></span>  <br/> |
|<span data-ttu-id="53877-138">Требуется на объектов хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="53877-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="53877-139">Да</span><span class="sxs-lookup"><span data-stu-id="53877-139">Yes</span></span>  <br/> |<span data-ttu-id="53877-140">Да</span><span class="sxs-lookup"><span data-stu-id="53877-140">Yes</span></span>  <br/> |<span data-ttu-id="53877-141">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-141">No</span></span>  <br/> |
|<span data-ttu-id="53877-142">Требуется на состояние объектов</span><span class="sxs-lookup"><span data-stu-id="53877-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="53877-143">Да</span><span class="sxs-lookup"><span data-stu-id="53877-143">Yes</span></span>  <br/> |<span data-ttu-id="53877-144">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-144">No</span></span>  <br/> |<span data-ttu-id="53877-145">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-145">No</span></span>  <br/> |
|<span data-ttu-id="53877-146">Созданные клиента</span><span class="sxs-lookup"><span data-stu-id="53877-146">Created by client</span></span>  <br/> |<span data-ttu-id="53877-147">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-147">No</span></span>  <br/> |<span data-ttu-id="53877-148">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-148">No</span></span>  <br/> |<span data-ttu-id="53877-149">Да</span><span class="sxs-lookup"><span data-stu-id="53877-149">Yes</span></span>  <br/> |
|<span data-ttu-id="53877-150">Доступные до вызова **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="53877-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="53877-151">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="53877-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="53877-152">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="53877-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="53877-153">Для сообщений, Да.</span><span class="sxs-lookup"><span data-stu-id="53877-153">For messages, Yes.</span></span> <span data-ttu-id="53877-154">Для других пользователей зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="53877-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="53877-155">Изменения в операцию копирования</span><span class="sxs-lookup"><span data-stu-id="53877-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="53877-156">Да</span><span class="sxs-lookup"><span data-stu-id="53877-156">Yes</span></span>  <br/> |<span data-ttu-id="53877-157">Да</span><span class="sxs-lookup"><span data-stu-id="53877-157">Yes</span></span>  <br/> |<span data-ttu-id="53877-158">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-158">No</span></span>  <br/> |
|<span data-ttu-id="53877-159">Механизм клиента после копирования</span><span class="sxs-lookup"><span data-stu-id="53877-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="53877-160">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-160">No</span></span>  <br/> |<span data-ttu-id="53877-161">Нет</span><span class="sxs-lookup"><span data-stu-id="53877-161">No</span></span>  <br/> |<span data-ttu-id="53877-162">Да</span><span class="sxs-lookup"><span data-stu-id="53877-162">Yes</span></span>  <br/> |
|<span data-ttu-id="53877-163">Уникальным в рамках</span><span class="sxs-lookup"><span data-stu-id="53877-163">Unique within</span></span>  <br/> |<span data-ttu-id="53877-164">Весь мир</span><span class="sxs-lookup"><span data-stu-id="53877-164">Entire world</span></span>  <br/> |<span data-ttu-id="53877-165">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="53877-165">Provider instance</span></span>  <br/> |<span data-ttu-id="53877-166">Весь мир</span><span class="sxs-lookup"><span data-stu-id="53877-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="53877-167">Двоичный сравнимые (как с memcmp)</span><span class="sxs-lookup"><span data-stu-id="53877-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="53877-168">Не используйте [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="53877-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="53877-169">Да</span><span class="sxs-lookup"><span data-stu-id="53877-169">Yes</span></span>  <br/> |<span data-ttu-id="53877-170">Да</span><span class="sxs-lookup"><span data-stu-id="53877-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="53877-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="53877-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53877-172">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="53877-172">Protocol specifications</span></span>

<span data-ttu-id="53877-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-174">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="53877-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53877-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-176">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="53877-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="53877-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-178">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53877-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="53877-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-180">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="53877-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="53877-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-182">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="53877-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="53877-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-184">Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="53877-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="53877-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-186">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="53877-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="53877-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53877-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53877-188">Указывает схему и методы, которые используются для запроса сведений о доступности для пользователей и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53877-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53877-189">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="53877-189">Header files</span></span>

<span data-ttu-id="53877-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53877-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="53877-191">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="53877-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="53877-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53877-192">Mapitags.h</span></span>
  
> <span data-ttu-id="53877-193">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="53877-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53877-194">См. также</span><span class="sxs-lookup"><span data-stu-id="53877-194">See also</span></span>



[<span data-ttu-id="53877-195">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="53877-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="53877-196">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53877-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53877-197">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53877-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53877-198">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="53877-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53877-199">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="53877-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

