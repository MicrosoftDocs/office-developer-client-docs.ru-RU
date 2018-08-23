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
ms.openlocfilehash: 48627c6d6eb2100e7dfcab832c86c1ec2e4ec8bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582807"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="bfe8f-103">Каноническое свойство PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="bfe8f-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="bfe8f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfe8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfe8f-105">Содержит идентификатор записи папка, содержащая папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe8f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bfe8f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfe8f-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bfe8f-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="bfe8f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bfe8f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bfe8f-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="bfe8f-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="bfe8f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bfe8f-110">Data type:</span></span>  <br/> |<span data-ttu-id="bfe8f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bfe8f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bfe8f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bfe8f-112">Area:</span></span>  <br/> |<span data-ttu-id="bfe8f-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="bfe8f-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfe8f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bfe8f-114">Remarks</span></span>

<span data-ttu-id="bfe8f-115">Это свойство вычисляется путем хранилищ сообщений для всех папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="bfe8f-116">Для корневой папки хранилища сообщений это свойство содержит идентификатор записи папки собственные.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="bfe8f-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) и это свойство не связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="bfe8f-118">Они принадлежат совершенно различных контекстах.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bfe8f-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bfe8f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfe8f-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bfe8f-120">Protocol specifications</span></span>

<span data-ttu-id="bfe8f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8f-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bfe8f-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8f-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8f-124">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="bfe8f-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8f-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8f-126">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-126">Handles folder operations.</span></span>
    
<span data-ttu-id="bfe8f-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8f-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8f-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="bfe8f-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8f-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8f-130">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="bfe8f-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8f-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8f-132">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="bfe8f-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8f-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8f-134">Задает метод доставки автономной адресной книги (OAB) данных от сервера к клиенту.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfe8f-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bfe8f-135">Header files</span></span>

<span data-ttu-id="bfe8f-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfe8f-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfe8f-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="bfe8f-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bfe8f-138">Mapitags.h</span></span>
  
> <span data-ttu-id="bfe8f-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bfe8f-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfe8f-140">См. также</span><span class="sxs-lookup"><span data-stu-id="bfe8f-140">See also</span></span>



[<span data-ttu-id="bfe8f-141">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="bfe8f-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="bfe8f-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe8f-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfe8f-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe8f-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfe8f-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe8f-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfe8f-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bfe8f-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

