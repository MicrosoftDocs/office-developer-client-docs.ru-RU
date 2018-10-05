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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401218"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="ef0fb-103">Каноническое свойство PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="ef0fb-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ef0fb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef0fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef0fb-105">Содержит идентификатор записи папка, содержащая папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef0fb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ef0fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef0fb-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ef0fb-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ef0fb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ef0fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef0fb-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="ef0fb-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="ef0fb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ef0fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef0fb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ef0fb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ef0fb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ef0fb-112">Area:</span></span>  <br/> |<span data-ttu-id="ef0fb-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="ef0fb-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef0fb-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef0fb-114">Remarks</span></span>

<span data-ttu-id="ef0fb-115">Это свойство вычисляется путем хранилищ сообщений для всех папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="ef0fb-116">Для корневой папки хранилища сообщений это свойство содержит идентификатор записи папки собственные.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="ef0fb-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) и это свойство не связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="ef0fb-118">Они принадлежат совершенно различных контекстах.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ef0fb-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ef0fb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef0fb-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ef0fb-120">Protocol specifications</span></span>

<span data-ttu-id="ef0fb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0fb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0fb-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef0fb-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0fb-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0fb-124">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="ef0fb-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0fb-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0fb-126">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-126">Handles folder operations.</span></span>
    
<span data-ttu-id="ef0fb-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0fb-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0fb-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ef0fb-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0fb-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0fb-130">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="ef0fb-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0fb-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0fb-132">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="ef0fb-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0fb-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0fb-134">Задает метод доставки автономной адресной книги (OAB) данных от сервера к клиенту.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef0fb-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ef0fb-135">Header files</span></span>

<span data-ttu-id="ef0fb-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef0fb-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef0fb-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef0fb-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ef0fb-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ef0fb-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ef0fb-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef0fb-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ef0fb-140">See also</span></span>



[<span data-ttu-id="ef0fb-141">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="ef0fb-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="ef0fb-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef0fb-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef0fb-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef0fb-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef0fb-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ef0fb-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef0fb-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ef0fb-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

