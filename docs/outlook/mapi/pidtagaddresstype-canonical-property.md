---
title: Каноническое свойство PidTagAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 464121a969beea06294049985052eb150651765f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580091"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="4b28b-103">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="4b28b-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="4b28b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b28b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b28b-105">Содержит тип адреса электронной почты, обмена мгновенными сообщениями пользователя, например SMTP.</span><span class="sxs-lookup"><span data-stu-id="4b28b-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b28b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4b28b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b28b-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="4b28b-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="4b28b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4b28b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b28b-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="4b28b-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="4b28b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4b28b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b28b-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4b28b-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4b28b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4b28b-112">Area:</span></span>  <br/> |<span data-ttu-id="4b28b-113">Address</span><span class="sxs-lookup"><span data-stu-id="4b28b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b28b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b28b-114">Remarks</span></span>

<span data-ttu-id="4b28b-115">Эти свойства являются примерами общие свойства базовый адрес всем пользователям, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4b28b-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="4b28b-116">Указывает, какие системы обмена сообщениями MAPI используется для обработки данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4b28b-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="4b28b-117">Это свойство также определяет формат строки адреса в **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4b28b-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="4b28b-118">Строка, которая предоставляет может содержать только прописные буквы от A до Z и цифры от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="4b28b-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="4b28b-119">Допустимый примеры строки:</span><span class="sxs-lookup"><span data-stu-id="4b28b-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="4b28b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4b28b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b28b-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4b28b-121">Protocol specifications</span></span>

<span data-ttu-id="4b28b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4b28b-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b28b-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-125">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b28b-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="4b28b-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-127">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="4b28b-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="4b28b-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-129">Обрабатывает клиентами с сервером интерфейса поставщика имя службы (NSPI).</span><span class="sxs-lookup"><span data-stu-id="4b28b-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="4b28b-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-131">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="4b28b-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="4b28b-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-133">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="4b28b-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="4b28b-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-135">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="4b28b-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="4b28b-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-137">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="4b28b-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4b28b-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-139">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="4b28b-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="4b28b-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-141">Задает свойства и операции, допустимые для шаблонов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4b28b-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="4b28b-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-143">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4b28b-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4b28b-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-145">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="4b28b-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="4b28b-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b28b-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b28b-147">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="4b28b-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b28b-148">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4b28b-148">Header files</span></span>

<span data-ttu-id="4b28b-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b28b-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b28b-150">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4b28b-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b28b-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4b28b-151">Mapitags.h</span></span>
  
> <span data-ttu-id="4b28b-152">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="4b28b-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b28b-153">См. также</span><span class="sxs-lookup"><span data-stu-id="4b28b-153">See also</span></span>



[<span data-ttu-id="4b28b-154">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4b28b-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b28b-155">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4b28b-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b28b-156">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4b28b-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b28b-157">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4b28b-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="4b28b-158">Типы адресов MAPI</span><span class="sxs-lookup"><span data-stu-id="4b28b-158">MAPI Address Types</span></span>](mapi-address-types.md)

