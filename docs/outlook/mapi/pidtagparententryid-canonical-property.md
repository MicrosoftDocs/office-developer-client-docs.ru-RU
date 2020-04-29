---
title: Каноническое свойство PidTagParentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 65f5e6c5da88267ec2e63d0acf3ef6f8e10c893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348232"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="9ae4c-103">Каноническое свойство PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="9ae4c-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9ae4c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ae4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ae4c-105">Содержит идентификатор папки, содержащей папку или сообщение.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ae4c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9ae4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ae4c-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9ae4c-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9ae4c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9ae4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ae4c-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="9ae4c-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="9ae4c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9ae4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ae4c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ae4c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ae4c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9ae4c-112">Area:</span></span>  <br/> |<span data-ttu-id="9ae4c-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="9ae4c-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ae4c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9ae4c-114">Remarks</span></span>

<span data-ttu-id="9ae4c-115">Это свойство вычисляется хранилищами сообщений для всех папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="9ae4c-116">Для корневой папки хранилища сообщений это свойство содержит собственный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="9ae4c-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)), и это свойство не связано друг с другом.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="9ae4c-118">Они относятся исключительно к разным контекстам.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ae4c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9ae4c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ae4c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9ae4c-120">Protocol specifications</span></span>

<span data-ttu-id="9ae4c-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ae4c-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ae4c-123">[[MS — ОКСКДАТА]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ae4c-124">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="9ae4c-125">[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ae4c-126">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-126">Handles folder operations.</span></span>
    
<span data-ttu-id="9ae4c-127">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ae4c-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9ae4c-129">[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ae4c-130">Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="9ae4c-131">[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ae4c-132">Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="9ae4c-133">[[MS — ОКСПФОАБ]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ae4c-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ae4c-134">Указывает метод доставки данных автономной адресной книги от сервера клиенту.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ae4c-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9ae4c-135">Header files</span></span>

<span data-ttu-id="9ae4c-136">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9ae4c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ae4c-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ae4c-138">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9ae4c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="9ae4c-139">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="9ae4c-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ae4c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="9ae4c-140">See also</span></span>



[<span data-ttu-id="9ae4c-141">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="9ae4c-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="9ae4c-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae4c-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ae4c-143">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae4c-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ae4c-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae4c-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ae4c-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9ae4c-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

