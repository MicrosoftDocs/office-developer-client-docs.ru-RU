---
title: Каноническое свойство PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8b2d435e132bf453cf41ec141d5a946bf54f9c66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591053"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="91517-103">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="91517-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="91517-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91517-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91517-105">Содержит тип объекта.</span><span class="sxs-lookup"><span data-stu-id="91517-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91517-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="91517-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91517-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="91517-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="91517-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="91517-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91517-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="91517-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="91517-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="91517-110">Data type:</span></span>  <br/> |<span data-ttu-id="91517-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="91517-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="91517-112">Область:</span><span class="sxs-lookup"><span data-stu-id="91517-112">Area:</span></span>  <br/> |<span data-ttu-id="91517-113">Common</span><span class="sxs-lookup"><span data-stu-id="91517-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91517-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="91517-114">Remarks</span></span>

<span data-ttu-id="91517-115">Тип объекта, содержащихся в это свойство соответствует основной интерфейс, доступные для объекта через интерфейс **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="91517-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="91517-116">Его можно получить, consulting параметр _lpulObjType_ , возвращенный методом соответствующие **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="91517-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="91517-117">Интерфейс получения другими способами, вызовите [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="91517-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="91517-118">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="91517-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="91517-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="91517-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="91517-120">Объект-контейнер адресной книги</span><span class="sxs-lookup"><span data-stu-id="91517-120">Address book container object</span></span> 
    
<span data-ttu-id="91517-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="91517-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="91517-122">Объект адресной книги</span><span class="sxs-lookup"><span data-stu-id="91517-122">Address book object</span></span> 
    
<span data-ttu-id="91517-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="91517-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="91517-124">Объект вложения сообщения</span><span class="sxs-lookup"><span data-stu-id="91517-124">Message attachment object</span></span> 
    
<span data-ttu-id="91517-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="91517-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="91517-126">Объект списка рассылки</span><span class="sxs-lookup"><span data-stu-id="91517-126">Distribution list object</span></span> 
    
<span data-ttu-id="91517-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="91517-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="91517-128">Объект папки</span><span class="sxs-lookup"><span data-stu-id="91517-128">Folder object</span></span> 
    
<span data-ttu-id="91517-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="91517-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="91517-130">Объект формы</span><span class="sxs-lookup"><span data-stu-id="91517-130">Form object</span></span> 
    
<span data-ttu-id="91517-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="91517-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="91517-132">Обмена сообщениями объекта пользователя</span><span class="sxs-lookup"><span data-stu-id="91517-132">Messaging user object</span></span> 
    
<span data-ttu-id="91517-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="91517-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="91517-134">Объект Message</span><span class="sxs-lookup"><span data-stu-id="91517-134">Message object</span></span> 
    
<span data-ttu-id="91517-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="91517-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="91517-136">Объект раздела профиля</span><span class="sxs-lookup"><span data-stu-id="91517-136">Profile section object</span></span> 
    
<span data-ttu-id="91517-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="91517-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="91517-138">Объект сеанса</span><span class="sxs-lookup"><span data-stu-id="91517-138">Session object</span></span> 
    
<span data-ttu-id="91517-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="91517-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="91517-140">Состояние объекта</span><span class="sxs-lookup"><span data-stu-id="91517-140">Status object</span></span> 
    
<span data-ttu-id="91517-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="91517-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="91517-142">Объект хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="91517-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="91517-143">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91517-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91517-144">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="91517-144">Protocol specifications</span></span>

<span data-ttu-id="91517-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-146">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="91517-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91517-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-148">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91517-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="91517-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-150">Обрабатывает клиентами с сервером интерфейса поставщика имя службы (NSPI).</span><span class="sxs-lookup"><span data-stu-id="91517-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="91517-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-152">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="91517-152">Handles folder operations.</span></span>
    
<span data-ttu-id="91517-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-154">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="91517-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="91517-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-156">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="91517-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="91517-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-158">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="91517-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="91517-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-160">Указывает форматы файлов автономной адресной книги (OAB) для кэша объектов локальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="91517-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="91517-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-162">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="91517-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="91517-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91517-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91517-164">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="91517-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91517-165">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="91517-165">Header files</span></span>

<span data-ttu-id="91517-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91517-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="91517-167">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="91517-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="91517-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91517-168">Mapitags.h</span></span>
  
> <span data-ttu-id="91517-169">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="91517-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91517-170">См. также</span><span class="sxs-lookup"><span data-stu-id="91517-170">See also</span></span>



[<span data-ttu-id="91517-171">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91517-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91517-172">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91517-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91517-173">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="91517-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91517-174">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="91517-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

