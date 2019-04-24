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
ms.openlocfilehash: 6051d3403cede21fa4aebdb6ca561dd3efb46771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360089"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="0c37d-103">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="0c37d-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="0c37d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c37d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c37d-105">Содержит тип электронного адреса пользователя обмена сообщениями, например, SMTP.</span><span class="sxs-lookup"><span data-stu-id="0c37d-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c37d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0c37d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c37d-107">ПР_АДДРТИПЕ, ПР_АДДРТИПЕ_А, ПР_АДДРТИПЕ_В</span><span class="sxs-lookup"><span data-stu-id="0c37d-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="0c37d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0c37d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c37d-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="0c37d-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="0c37d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0c37d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c37d-111">ПТ_УНИКОДЕ, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0c37d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0c37d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0c37d-112">Area:</span></span>  <br/> |<span data-ttu-id="0c37d-113">Address</span><span class="sxs-lookup"><span data-stu-id="0c37d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c37d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c37d-114">Remarks</span></span>

<span data-ttu-id="0c37d-115">Эти свойства являются примерами свойств базового адреса, общих для всех пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0c37d-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="0c37d-116">Он указывает, какая система обмена сообщениями использует MAPI для обработки данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="0c37d-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="0c37d-117">Это свойство также определяет формат строки адреса в **пр_емаил_адресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0c37d-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="0c37d-118">Строка, которую она предоставляет, может содержать только буквы в верхнем регистре от A до Z и цифры от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="0c37d-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="0c37d-119">Допустимыми примерами для строки являются:</span><span class="sxs-lookup"><span data-stu-id="0c37d-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="0c37d-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0c37d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c37d-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0c37d-121">Protocol specifications</span></span>

<span data-ttu-id="0c37d-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0c37d-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c37d-124">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-125">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c37d-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="0c37d-126">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-127">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c37d-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0c37d-128">[[MS — NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-129">Обрабатывает связь клиента с сервером интерфейса поставщика услуг имен (NSPI).</span><span class="sxs-lookup"><span data-stu-id="0c37d-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="0c37d-130">[[MS — ОКСКДАТА]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-131">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="0c37d-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="0c37d-132">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-133">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="0c37d-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0c37d-134">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-135">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="0c37d-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0c37d-136">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-137">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="0c37d-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0c37d-138">[[MS — ОКСКСТОР]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-139">Указывает допустимые операции для основных объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c37d-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="0c37d-140">[[MS — ОКСОАБКТ]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-141">Задает свойства и операции, допустимые для шаблонов адресных книг.</span><span class="sxs-lookup"><span data-stu-id="0c37d-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="0c37d-142">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-143">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0c37d-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0c37d-144">[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-145">Управляет входящими сообщениями электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="0c37d-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="0c37d-146">[[MS — ОКСОСРЧ]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c37d-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c37d-147">Задает свойства и операции для управления конфигурацией списка папок поиска.</span><span class="sxs-lookup"><span data-stu-id="0c37d-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c37d-148">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="0c37d-148">Header files</span></span>

<span data-ttu-id="0c37d-149">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0c37d-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c37d-150">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0c37d-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c37d-151">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="0c37d-151">Mapitags.h</span></span>
  
> <span data-ttu-id="0c37d-152">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="0c37d-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c37d-153">См. также</span><span class="sxs-lookup"><span data-stu-id="0c37d-153">See also</span></span>



[<span data-ttu-id="0c37d-154">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0c37d-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c37d-155">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0c37d-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c37d-156">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0c37d-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c37d-157">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0c37d-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="0c37d-158">Типы адресов MAPI</span><span class="sxs-lookup"><span data-stu-id="0c37d-158">MAPI Address Types</span></span>](mapi-address-types.md)

