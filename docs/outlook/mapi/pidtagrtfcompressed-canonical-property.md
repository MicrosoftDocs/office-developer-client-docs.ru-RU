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
ms.openlocfilehash: c88e6789b5b48e946d86a0458674a0fbe6b76356
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575450"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="6872e-103">Каноническое свойство PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="6872e-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="6872e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6872e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6872e-105">Содержит версию форматированный текст (RTF) текст сообщения, обычно в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="6872e-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6872e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6872e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6872e-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="6872e-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="6872e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6872e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6872e-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="6872e-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="6872e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6872e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6872e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6872e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6872e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6872e-112">Area:</span></span>  <br/> |<span data-ttu-id="6872e-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="6872e-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6872e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6872e-114">Remarks</span></span>

<span data-ttu-id="6872e-115">Это свойство содержит текст сообщения, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), но в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="6872e-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="6872e-116">Текст сообщения в формате RTF обычно хранятся в сжатом виде.</span><span class="sxs-lookup"><span data-stu-id="6872e-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="6872e-117">Тем не менее некоторые системы отсутствует форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="6872e-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="6872e-118">Чтобы обеспечить их, MAPI предоставляет значение dwMagicUncompressedRTF для заголовка потока для идентификации несжатую RTF и флаг **STORE_UNCOMPRESSED_RTF** в **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) в качестве сообщения хранить указывает, что она может хранить несжатый формат RTF.</span><span class="sxs-lookup"><span data-stu-id="6872e-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="6872e-119">Для получения значения этого свойства, вызовите **OpenProperty**, а затем вызывают [WrapCompressedRTFStream](wrapcompressedrtfstream.md) с флагом **MAPI_READ** .</span><span class="sxs-lookup"><span data-stu-id="6872e-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="6872e-120">Для записи в это свойство, откройте его с флаги **MAPI_MODIFY** и **MAPI_CREATE** .</span><span class="sxs-lookup"><span data-stu-id="6872e-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="6872e-121">Это гарантирует, что новые данные полностью заменить старый данные и операций записи с помощью минимальное число обновлений хранилища.</span><span class="sxs-lookup"><span data-stu-id="6872e-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="6872e-122">Хранилищ сообщений, которые поддерживают RTF игнорировать любые изменения пробелы в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="6872e-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="6872e-123">При **PR_BODY** хранится в первый раз, хранилище сообщений также создает и сохраняет это свойство.</span><span class="sxs-lookup"><span data-stu-id="6872e-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="6872e-124">Если вызывается метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , были ли изменены **PR_BODY** хранилище сообщений вызывает функцию [RTFSync](rtfsync.md) для синхронизации с версией RTF.</span><span class="sxs-lookup"><span data-stu-id="6872e-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="6872e-125">Только изменился пробелы свойства остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="6872e-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="6872e-126">Это позволяет сохранить все нестандартный формат RTF форматирования при передаче сообщения через поддерживающими RTF клиентов и системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6872e-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6872e-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6872e-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6872e-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6872e-128">Protocol specifications</span></span>

<span data-ttu-id="6872e-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6872e-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6872e-130">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6872e-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6872e-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6872e-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6872e-132">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="6872e-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6872e-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6872e-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6872e-134">Кодирует и декодирует сжатого потока в теле письма RTF.</span><span class="sxs-lookup"><span data-stu-id="6872e-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="6872e-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6872e-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6872e-136">Инкапсулирует Дополнительные форматы контента (например, HTML) в свойстве текст RTF сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="6872e-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6872e-137">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6872e-137">Header files</span></span>

<span data-ttu-id="6872e-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6872e-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="6872e-139">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6872e-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="6872e-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6872e-140">Mapitags.h</span></span>
  
> <span data-ttu-id="6872e-141">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6872e-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6872e-142">См. также</span><span class="sxs-lookup"><span data-stu-id="6872e-142">See also</span></span>



[<span data-ttu-id="6872e-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6872e-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6872e-144">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6872e-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6872e-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6872e-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6872e-146">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6872e-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

