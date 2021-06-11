---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Последнее изменение: 20 сентября 2017 г.'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326946"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="e866b-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e866b-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="e866b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e866b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e866b-105">Преобразует сообщение MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="e866b-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="e866b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e866b-106">Parameters</span></span>

 <span data-ttu-id="e866b-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="e866b-107">_pmsg_</span></span>
  
> <span data-ttu-id="e866b-108">[in] Указатель на сообщение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="e866b-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="e866b-109">См. mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="e866b-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="e866b-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="e866b-110">_pstm_</span></span>
  
> <span data-ttu-id="e866b-111">[вышел] [Интерфейс IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для вывода потока.</span><span class="sxs-lookup"><span data-stu-id="e866b-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="e866b-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e866b-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="e866b-113">[in] Флаги, которые указывают определенные действия для конвертера:</span><span class="sxs-lookup"><span data-stu-id="e866b-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="e866b-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="e866b-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="e866b-115">Конвертер должен разрешить 8-битные заготки.</span><span class="sxs-lookup"><span data-stu-id="e866b-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="e866b-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e866b-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="e866b-117">В X-Unsent сохраняется отправленная/неослабеваемая информация.</span><span class="sxs-lookup"><span data-stu-id="e866b-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="e866b-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e866b-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="e866b-119">Конвертер должен создать международное сообщение (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="e866b-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="e866b-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="e866b-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="e866b-121">Получатели сообщения MAPI BCC должны быть включены в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="e866b-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="e866b-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="e866b-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="e866b-123">Не включай Message-Id поле в исходяние сообщений.</span><span class="sxs-lookup"><span data-stu-id="e866b-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="e866b-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="e866b-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="e866b-125">Преобразователь должен игнорировать заглавные главы внешнего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e866b-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="e866b-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="e866b-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="e866b-127">Конвертер должен просто отправить простой текст.</span><span class="sxs-lookup"><span data-stu-id="e866b-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="e866b-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="e866b-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="e866b-129">Преобразователь передает сообщение SMTP.</span><span class="sxs-lookup"><span data-stu-id="e866b-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="e866b-130">Этот флаг всегда должен быть заданной.</span><span class="sxs-lookup"><span data-stu-id="e866b-130">This flag must always be set.</span></span>
    
<span data-ttu-id="e866b-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="e866b-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="e866b-132">Конвертер должен преобразовать из ФОРМАТа HTML в формат RTF в сообщении MIME.</span><span class="sxs-lookup"><span data-stu-id="e866b-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="e866b-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="e866b-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="e866b-134">Конвертер должен использовать формат транспортной нейтральной инкапсуляции (TNEF) в сообщении MIME.</span><span class="sxs-lookup"><span data-stu-id="e866b-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e866b-135">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e866b-135">Return values</span></span>

<span data-ttu-id="e866b-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e866b-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="e866b-137">Недействительные флаги были переданы,  *или pmsg*  или  *pstm*  является NULL.</span><span class="sxs-lookup"><span data-stu-id="e866b-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e866b-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="e866b-138">Remarks</span></span>

<span data-ttu-id="e866b-139">Поддерживается только для стандартных типов Outlook сообщений.</span><span class="sxs-lookup"><span data-stu-id="e866b-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e866b-140">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e866b-140">MFCMAPI reference</span></span>

<span data-ttu-id="e866b-141">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e866b-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e866b-142">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e866b-142">**File**</span></span>|<span data-ttu-id="e866b-143">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e866b-143">**Function**</span></span>|<span data-ttu-id="e866b-144">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e866b-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e866b-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="e866b-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e866b-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="e866b-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="e866b-147">MFCMAPI использует MimeToMAPI для преобразования файла EML в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="e866b-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="e866b-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="e866b-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e866b-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="e866b-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="e866b-150">MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в файл EML.</span><span class="sxs-lookup"><span data-stu-id="e866b-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e866b-151">См. также</span><span class="sxs-lookup"><span data-stu-id="e866b-151">See also</span></span>



[<span data-ttu-id="e866b-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e866b-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="e866b-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e866b-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="e866b-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="e866b-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="e866b-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="e866b-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="e866b-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="e866b-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="e866b-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="e866b-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="e866b-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="e866b-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="e866b-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="e866b-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="e866b-160">Каноническое свойство PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="e866b-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="e866b-161">������������ �������� PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="e866b-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="e866b-162">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="e866b-162">MAPI Constants</span></span>](mapi-constants.md)

