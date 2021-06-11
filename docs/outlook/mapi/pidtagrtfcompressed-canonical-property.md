---
title: Каноническое свойство PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357892"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="d7ef7-103">Каноническое свойство PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="d7ef7-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="d7ef7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7ef7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7ef7-105">Содержит версию текста сообщения с богатым текстовым форматом (RTF), обычно в сжатой форме.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7ef7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d7ef7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7ef7-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="d7ef7-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="d7ef7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d7ef7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7ef7-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="d7ef7-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="d7ef7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d7ef7-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7ef7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7ef7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7ef7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d7ef7-112">Area:</span></span>  <br/> |<span data-ttu-id="d7ef7-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="d7ef7-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7ef7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7ef7-114">Remarks</span></span>

<span data-ttu-id="d7ef7-115">Это свойство содержит тот же текст сообщения, **что и свойство PR_BODY** [(PidTagBody),](pidtagbody-canonical-property.md)но в RTF.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="d7ef7-116">Текст сообщения в RTF обычно хранится в сжатой форме.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="d7ef7-117">Однако некоторые системы не сжимаются форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="d7ef7-118">Для их размещения MAPI предоставляет значение dwMagicUncompressedRTF для заглавного потока для идентификации некомпрессивного RTF, а флаг STORE_UNCOMPRESSED_RTF в **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)для магазина сообщений, чтобы указать, что он может хранить некомпрессивный RTF. </span><span class="sxs-lookup"><span data-stu-id="d7ef7-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="d7ef7-119">Чтобы получить содержимое этого свойства, позвоните **в OpenProperty,** а затем позвоните [WrapCompressedRTFStream](wrapcompressedrtfstream.md) с **MAPI_READ** флагом.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="d7ef7-120">Чтобы вписаться в это свойство, откройте его с **MAPI_MODIFY** **MAPI_CREATE** флагами.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="d7ef7-121">Это гарантирует, что новые данные полностью заменяют старые данные и что записи выполняются с помощью минимального количества обновлений магазина.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="d7ef7-122">Хранилища сообщений, поддерживают RTF, игнорируют любые изменения в белом пространстве в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="d7ef7-123">Когда **PR_BODY** хранится впервые, хранилище сообщений также создает и сохраняет это свойство.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="d7ef7-124">Если метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) впоследствии  вызывается и PR_BODY изменен, хранилище сообщений вызывает функцию [RTFSync](rtfsync.md) для обеспечения синхронизации с версией RTF.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="d7ef7-125">Если изменено только белое пространство, свойства остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="d7ef7-126">При этом сохраняется любое нетривиальный форматирование RTF, когда сообщение передается через клиенты и системы обмена сообщениями, не знаюющие RTF.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d7ef7-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d7ef7-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7ef7-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d7ef7-128">Protocol specifications</span></span>

<span data-ttu-id="d7ef7-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7ef7-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7ef7-130">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7ef7-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7ef7-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7ef7-132">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d7ef7-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7ef7-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7ef7-134">Кодирует и декодирует сжатый поток в телах сообщений RTF.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="d7ef7-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7ef7-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7ef7-136">Инкапсулирует дополнительные форматы контента (например, HTML) в свойстве тела RTF сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7ef7-137">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="d7ef7-137">Header files</span></span>

<span data-ttu-id="d7ef7-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7ef7-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7ef7-139">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7ef7-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7ef7-140">Mapitags.h</span></span>
  
> <span data-ttu-id="d7ef7-141">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7ef7-142">См. также</span><span class="sxs-lookup"><span data-stu-id="d7ef7-142">See also</span></span>



[<span data-ttu-id="d7ef7-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d7ef7-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7ef7-144">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d7ef7-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7ef7-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d7ef7-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7ef7-146">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="d7ef7-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

