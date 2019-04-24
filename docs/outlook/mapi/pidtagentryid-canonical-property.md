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
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="97370-103">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="97370-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="97370-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97370-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97370-105">Содержит идентификатор записи MAPI, используемый для открытия и изменения свойств определенного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="97370-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97370-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="97370-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97370-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="97370-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="97370-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="97370-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97370-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="97370-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="97370-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="97370-110">Data type:</span></span>  <br/> |<span data-ttu-id="97370-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="97370-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="97370-112">Область:</span><span class="sxs-lookup"><span data-stu-id="97370-112">Area:</span></span>  <br/> |<span data-ttu-id="97370-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="97370-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97370-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97370-114">Remarks</span></span>

<span data-ttu-id="97370-115">Это свойство идентифицирует объект для **OpenEntry** , который создает экземпляр, и предоставляет доступ ко всем его свойствам с помощью соответствующего производного интерфейса **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="97370-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="97370-116">Это свойство является одним из свойств базового адреса для всех пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="97370-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="97370-117">Это свойство может содержать либо долгосрочный, либо краткосрочный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="97370-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="97370-118">Краткосрочные идентификаторы проще и быстрее строятся, но ограничены их областью и длительностью, обычно к текущему сеансу и рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="97370-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="97370-119">Они обычно используются для объектов временной природы, таких как строки таблицы или элементы диалоговых окон, а затем отброшены.</span><span class="sxs-lookup"><span data-stu-id="97370-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="97370-120">Долгосрочные идентификаторы используются для объектов более широкого и долгосрочного характера.</span><span class="sxs-lookup"><span data-stu-id="97370-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="97370-121">Это свойство всегда доступно с помощью метода [IMAPIProp::](imapiprop-getprops.md) -Props, следующего за первым вызовом метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="97370-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="97370-122">Некоторые поставщики услуг могут сделать их доступными сразу же после создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="97370-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="97370-123">Поставщик должен всегда возвращать долгосрочный идентификатор записи из PROPS \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="97370-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="97370-124">Таким образом, чтобы преобразовать краткосрочный идентификатор в долгосрочный, просто откройте объект и получите его свойство через **PROPS**.</span><span class="sxs-lookup"><span data-stu-id="97370-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="97370-125">В следующей таблице приведены важные различия между этим свойством, **пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и **пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="97370-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="97370-126">**Характеристика**</span><span class="sxs-lookup"><span data-stu-id="97370-126">**Characteristic**</span></span>|<span data-ttu-id="97370-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="97370-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="97370-128">**ПР_РЕКОРД_КЭЙ**</span><span class="sxs-lookup"><span data-stu-id="97370-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="97370-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="97370-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="97370-130">Обязательный атрибут для объектов вложений</span><span class="sxs-lookup"><span data-stu-id="97370-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="97370-131">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-131">No</span></span>  <br/> |<span data-ttu-id="97370-132">Да</span><span class="sxs-lookup"><span data-stu-id="97370-132">Yes</span></span>  <br/> |<span data-ttu-id="97370-133">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-133">No</span></span>  <br/> |
|<span data-ttu-id="97370-134">Обязательный атрибут для объектов Folder</span><span class="sxs-lookup"><span data-stu-id="97370-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="97370-135">Да</span><span class="sxs-lookup"><span data-stu-id="97370-135">Yes</span></span>  <br/> |<span data-ttu-id="97370-136">Да</span><span class="sxs-lookup"><span data-stu-id="97370-136">Yes</span></span>  <br/> |<span data-ttu-id="97370-137">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-137">No</span></span>  <br/> |
|<span data-ttu-id="97370-138">Обязательный для объектов хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="97370-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="97370-139">Да</span><span class="sxs-lookup"><span data-stu-id="97370-139">Yes</span></span>  <br/> |<span data-ttu-id="97370-140">Да</span><span class="sxs-lookup"><span data-stu-id="97370-140">Yes</span></span>  <br/> |<span data-ttu-id="97370-141">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-141">No</span></span>  <br/> |
|<span data-ttu-id="97370-142">Обязательные для объектов Status</span><span class="sxs-lookup"><span data-stu-id="97370-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="97370-143">Да</span><span class="sxs-lookup"><span data-stu-id="97370-143">Yes</span></span>  <br/> |<span data-ttu-id="97370-144">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-144">No</span></span>  <br/> |<span data-ttu-id="97370-145">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-145">No</span></span>  <br/> |
|<span data-ttu-id="97370-146">Создано клиентом</span><span class="sxs-lookup"><span data-stu-id="97370-146">Created by client</span></span>  <br/> |<span data-ttu-id="97370-147">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-147">No</span></span>  <br/> |<span data-ttu-id="97370-148">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-148">No</span></span>  <br/> |<span data-ttu-id="97370-149">Да</span><span class="sxs-lookup"><span data-stu-id="97370-149">Yes</span></span>  <br/> |
|<span data-ttu-id="97370-150">Доступно до вызова **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="97370-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="97370-151">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="97370-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="97370-152">Зависит от реализации поставщика</span><span class="sxs-lookup"><span data-stu-id="97370-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="97370-153">Для сообщений — да.</span><span class="sxs-lookup"><span data-stu-id="97370-153">For messages, Yes.</span></span> <span data-ttu-id="97370-154">Для других пользователей зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="97370-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="97370-155">Изменено в операции копирования</span><span class="sxs-lookup"><span data-stu-id="97370-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="97370-156">Да</span><span class="sxs-lookup"><span data-stu-id="97370-156">Yes</span></span>  <br/> |<span data-ttu-id="97370-157">Да</span><span class="sxs-lookup"><span data-stu-id="97370-157">Yes</span></span>  <br/> |<span data-ttu-id="97370-158">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-158">No</span></span>  <br/> |
|<span data-ttu-id="97370-159">Изменение клиентом после копирования</span><span class="sxs-lookup"><span data-stu-id="97370-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="97370-160">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-160">No</span></span>  <br/> |<span data-ttu-id="97370-161">Нет</span><span class="sxs-lookup"><span data-stu-id="97370-161">No</span></span>  <br/> |<span data-ttu-id="97370-162">Да</span><span class="sxs-lookup"><span data-stu-id="97370-162">Yes</span></span>  <br/> |
|<span data-ttu-id="97370-163">Уникальный в пределах</span><span class="sxs-lookup"><span data-stu-id="97370-163">Unique within</span></span>  <br/> |<span data-ttu-id="97370-164">Весь мир</span><span class="sxs-lookup"><span data-stu-id="97370-164">Entire world</span></span>  <br/> |<span data-ttu-id="97370-165">Экземпляр поставщика</span><span class="sxs-lookup"><span data-stu-id="97370-165">Provider instance</span></span>  <br/> |<span data-ttu-id="97370-166">Весь мир</span><span class="sxs-lookup"><span data-stu-id="97370-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="97370-167">Сравнение двоичных файлов (как и в случае с мемкмп)</span><span class="sxs-lookup"><span data-stu-id="97370-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="97370-168">Без использования [имаписуппорт:: метод compareentryids](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="97370-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="97370-169">Да</span><span class="sxs-lookup"><span data-stu-id="97370-169">Yes</span></span>  <br/> |<span data-ttu-id="97370-170">Да</span><span class="sxs-lookup"><span data-stu-id="97370-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="97370-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="97370-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97370-172">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="97370-172">Protocol specifications</span></span>

<span data-ttu-id="97370-173">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-174">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="97370-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97370-175">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-176">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="97370-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="97370-177">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-178">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97370-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="97370-179">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-180">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="97370-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="97370-181">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-182">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="97370-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="97370-183">[[MS — ОКСКПЕРМ]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-184">Обрабатывает получение списков разрешений на доступ к папкам, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="97370-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="97370-185">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-186">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="97370-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="97370-187">[[MS — ОКСВАВЛС]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97370-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97370-188">Указывает схему и методы, которые используются для запроса сведений о доступности для пользователей и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97370-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97370-189">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="97370-189">Header files</span></span>

<span data-ttu-id="97370-190">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="97370-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="97370-191">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="97370-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="97370-192">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="97370-192">Mapitags.h</span></span>
  
> <span data-ttu-id="97370-193">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="97370-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97370-194">См. также</span><span class="sxs-lookup"><span data-stu-id="97370-194">See also</span></span>



[<span data-ttu-id="97370-195">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="97370-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="97370-196">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97370-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97370-197">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="97370-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97370-198">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="97370-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97370-199">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="97370-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

