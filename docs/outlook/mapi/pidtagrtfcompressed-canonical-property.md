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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394897"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="88833-103">Каноническое свойство PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="88833-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="88833-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88833-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88833-105">Содержит версию форматированный текст (RTF) текст сообщения, обычно в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="88833-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88833-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="88833-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88833-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="88833-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="88833-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="88833-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88833-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="88833-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="88833-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="88833-110">Data type:</span></span>  <br/> |<span data-ttu-id="88833-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="88833-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="88833-112">Область:</span><span class="sxs-lookup"><span data-stu-id="88833-112">Area:</span></span>  <br/> |<span data-ttu-id="88833-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="88833-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88833-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="88833-114">Remarks</span></span>

<span data-ttu-id="88833-115">Это свойство содержит текст сообщения, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), но в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="88833-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="88833-116">Текст сообщения в формате RTF обычно хранятся в сжатом виде.</span><span class="sxs-lookup"><span data-stu-id="88833-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="88833-117">Тем не менее некоторые системы отсутствует форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="88833-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="88833-118">Чтобы обеспечить их, MAPI предоставляет значение dwMagicUncompressedRTF для заголовка потока для идентификации несжатую RTF и флаг **STORE_UNCOMPRESSED_RTF** в **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) в качестве сообщения хранить указывает, что она может хранить несжатый формат RTF.</span><span class="sxs-lookup"><span data-stu-id="88833-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="88833-119">Для получения значения этого свойства, вызовите **OpenProperty**, а затем вызывают [WrapCompressedRTFStream](wrapcompressedrtfstream.md) с флагом **MAPI_READ** .</span><span class="sxs-lookup"><span data-stu-id="88833-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="88833-120">Для записи в это свойство, откройте его с флаги **MAPI_MODIFY** и **MAPI_CREATE** .</span><span class="sxs-lookup"><span data-stu-id="88833-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="88833-121">Это гарантирует, что новые данные полностью заменить старый данные и операций записи с помощью минимальное число обновлений хранилища.</span><span class="sxs-lookup"><span data-stu-id="88833-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="88833-122">Хранилищ сообщений, которые поддерживают RTF игнорировать любые изменения пробелы в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="88833-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="88833-123">При **PR_BODY** хранится в первый раз, хранилище сообщений также создает и сохраняет это свойство.</span><span class="sxs-lookup"><span data-stu-id="88833-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="88833-124">Если вызывается метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , были ли изменены **PR_BODY** хранилище сообщений вызывает функцию [RTFSync](rtfsync.md) для синхронизации с версией RTF.</span><span class="sxs-lookup"><span data-stu-id="88833-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="88833-125">Только изменился пробелы свойства остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="88833-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="88833-126">Это позволяет сохранить все нестандартный формат RTF форматирования при передаче сообщения через поддерживающими RTF клиентов и системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="88833-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="88833-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="88833-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88833-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="88833-128">Protocol specifications</span></span>

<span data-ttu-id="88833-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88833-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88833-130">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="88833-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88833-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88833-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88833-132">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="88833-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="88833-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88833-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88833-134">Кодирует и декодирует сжатого потока в теле письма RTF.</span><span class="sxs-lookup"><span data-stu-id="88833-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="88833-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88833-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88833-136">Инкапсулирует Дополнительные форматы контента (например, HTML) в свойстве текст RTF сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="88833-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88833-137">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="88833-137">Header files</span></span>

<span data-ttu-id="88833-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88833-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="88833-139">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="88833-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="88833-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="88833-140">Mapitags.h</span></span>
  
> <span data-ttu-id="88833-141">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="88833-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88833-142">См. также</span><span class="sxs-lookup"><span data-stu-id="88833-142">See also</span></span>



[<span data-ttu-id="88833-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="88833-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88833-144">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="88833-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88833-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="88833-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88833-146">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="88833-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

