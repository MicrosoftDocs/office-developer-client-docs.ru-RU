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
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328590"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="b79e9-103">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="b79e9-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b79e9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b79e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b79e9-105">Содержит идентификатор записи MAPI, используемый для открытия и редактирования свойств определенного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="b79e9-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b79e9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b79e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b79e9-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b79e9-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b79e9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b79e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b79e9-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="b79e9-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="b79e9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b79e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="b79e9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b79e9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b79e9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b79e9-112">Area:</span></span>  <br/> |<span data-ttu-id="b79e9-113">Свойства ID</span><span class="sxs-lookup"><span data-stu-id="b79e9-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b79e9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b79e9-114">Remarks</span></span>

<span data-ttu-id="b79e9-115">Это свойство идентифицирует объект **Для OpenEntry** для мгновенного обмена данными и предоставляет доступ ко всем его свойствам с помощью соответствующего интерфейса **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="b79e9-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="b79e9-116">Это свойство является одним из базовых свойств адресов для всех пользователей обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b79e9-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="b79e9-117">Это свойство может содержать долгосрочный или краткосрочный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="b79e9-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="b79e9-118">Краткосрочные идентификаторы легче и быстрее создавать, но ограничены в их области и продолжительности, как правило, для текущего сеанса и рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="b79e9-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="b79e9-119">Они обычно используются для объектов временного характера, таких как строки таблицы или записи диалоговых полей, а затем заброшены.</span><span class="sxs-lookup"><span data-stu-id="b79e9-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="b79e9-120">Долгосрочные идентификаторы используются для объектов более широкого и длительного характера.</span><span class="sxs-lookup"><span data-stu-id="b79e9-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="b79e9-121">Это свойство всегда доступно с помощью [метода IMAPIProp::GetProps](imapiprop-getprops.md) после первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="b79e9-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="b79e9-122">Некоторые поставщики услуг могут сделать ее доступной сразу после мгновенной работы.</span><span class="sxs-lookup"><span data-stu-id="b79e9-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="b79e9-123">Поставщик должен всегда возвращать долгосрочный идентификатор записи из **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="b79e9-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="b79e9-124">Поэтому, чтобы преобразовать краткосрочный идентификатор в долгосрочный, просто откройте объект и получите его это свойство через **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="b79e9-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="b79e9-125">В следующей таблице обобщены важные различия между этим **свойством: PR_RECORD_KEY** [(PidTagRecordKey)](pidtagrecordkey-canonical-property.md)и **PR_SEARCH_KEY** [(PidTagSearchKey).](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b79e9-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="b79e9-126">**Характеристика**</span><span class="sxs-lookup"><span data-stu-id="b79e9-126">**Characteristic**</span></span>|<span data-ttu-id="b79e9-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="b79e9-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="b79e9-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="b79e9-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="b79e9-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="b79e9-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b79e9-130">Необходимые для объектов вложений</span><span class="sxs-lookup"><span data-stu-id="b79e9-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="b79e9-131">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-131">No</span></span>  <br/> |<span data-ttu-id="b79e9-132">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-132">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-133">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-133">No</span></span>  <br/> |
|<span data-ttu-id="b79e9-134">Необходимые для объектов папок</span><span class="sxs-lookup"><span data-stu-id="b79e9-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="b79e9-135">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-135">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-136">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-136">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-137">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-137">No</span></span>  <br/> |
|<span data-ttu-id="b79e9-138">Необходимые для объектов хранения сообщений</span><span class="sxs-lookup"><span data-stu-id="b79e9-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="b79e9-139">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-139">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-140">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-140">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-141">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-141">No</span></span>  <br/> |
|<span data-ttu-id="b79e9-142">Необходимые для объектов состояния</span><span class="sxs-lookup"><span data-stu-id="b79e9-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="b79e9-143">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-143">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-144">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-144">No</span></span>  <br/> |<span data-ttu-id="b79e9-145">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-145">No</span></span>  <br/> |
|<span data-ttu-id="b79e9-146">Созданный клиентом</span><span class="sxs-lookup"><span data-stu-id="b79e9-146">Created by client</span></span>  <br/> |<span data-ttu-id="b79e9-147">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-147">No</span></span>  <br/> |<span data-ttu-id="b79e9-148">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-148">No</span></span>  <br/> |<span data-ttu-id="b79e9-149">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-149">Yes</span></span>  <br/> |
|<span data-ttu-id="b79e9-150">Доступно перед вызовом **в SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="b79e9-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="b79e9-151">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="b79e9-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="b79e9-152">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="b79e9-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="b79e9-153">Для сообщений да.</span><span class="sxs-lookup"><span data-stu-id="b79e9-153">For messages, Yes.</span></span> <span data-ttu-id="b79e9-154">Для других это зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="b79e9-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="b79e9-155">Изменено в операции копирования</span><span class="sxs-lookup"><span data-stu-id="b79e9-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="b79e9-156">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-156">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-157">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-157">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-158">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-158">No</span></span>  <br/> |
|<span data-ttu-id="b79e9-159">Изменение клиента после копирования</span><span class="sxs-lookup"><span data-stu-id="b79e9-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="b79e9-160">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-160">No</span></span>  <br/> |<span data-ttu-id="b79e9-161">Нет</span><span class="sxs-lookup"><span data-stu-id="b79e9-161">No</span></span>  <br/> |<span data-ttu-id="b79e9-162">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-162">Yes</span></span>  <br/> |
|<span data-ttu-id="b79e9-163">Уникальный в пределах</span><span class="sxs-lookup"><span data-stu-id="b79e9-163">Unique within</span></span>  <br/> |<span data-ttu-id="b79e9-164">Весь мир</span><span class="sxs-lookup"><span data-stu-id="b79e9-164">Entire world</span></span>  <br/> |<span data-ttu-id="b79e9-165">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="b79e9-165">Provider instance</span></span>  <br/> |<span data-ttu-id="b79e9-166">Весь мир</span><span class="sxs-lookup"><span data-stu-id="b79e9-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="b79e9-167">Двоичная сопоставимая (как с memcmp)</span><span class="sxs-lookup"><span data-stu-id="b79e9-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="b79e9-168">Отсутствие использования [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="b79e9-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="b79e9-169">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-169">Yes</span></span>  <br/> |<span data-ttu-id="b79e9-170">Да</span><span class="sxs-lookup"><span data-stu-id="b79e9-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b79e9-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b79e9-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b79e9-172">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b79e9-172">Protocol specifications</span></span>

<span data-ttu-id="b79e9-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-174">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b79e9-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b79e9-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-176">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="b79e9-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b79e9-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-178">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b79e9-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="b79e9-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-180">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="b79e9-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="b79e9-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-182">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="b79e9-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b79e9-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-184">Обрабатывает ирисовку списков разрешений папок, хранимых на сервере.</span><span class="sxs-lookup"><span data-stu-id="b79e9-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="b79e9-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-186">Указывает методы подключения к почтовым ящикам и настройки их в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b79e9-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="b79e9-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79e9-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79e9-188">Указывает схему и методы, используемые для запроса сведений о доступности для пользователей и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b79e9-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b79e9-189">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b79e9-189">Header files</span></span>

<span data-ttu-id="b79e9-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b79e9-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="b79e9-191">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b79e9-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="b79e9-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b79e9-192">Mapitags.h</span></span>
  
> <span data-ttu-id="b79e9-193">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b79e9-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b79e9-194">См. также</span><span class="sxs-lookup"><span data-stu-id="b79e9-194">See also</span></span>



[<span data-ttu-id="b79e9-195">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="b79e9-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="b79e9-196">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b79e9-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b79e9-197">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b79e9-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b79e9-198">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b79e9-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b79e9-199">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b79e9-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

