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
description: 'Последнее изменение: 20 сентября 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400119"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="22a60-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="22a60-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="22a60-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22a60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22a60-105">Преобразование сообщения MAPI в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="22a60-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="22a60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22a60-106">Parameters</span></span>

 <span data-ttu-id="22a60-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="22a60-107">_pmsg_</span></span>
  
> <span data-ttu-id="22a60-108">[in] Указатель на сообщение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="22a60-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="22a60-109">В разделе mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="22a60-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="22a60-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="22a60-110">_pstm_</span></span>
  
> <span data-ttu-id="22a60-111">[out] Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для вывода в потоке.</span><span class="sxs-lookup"><span data-stu-id="22a60-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="22a60-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22a60-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="22a60-113">[in] Флаги, указывающие конкретные действия для преобразователя:</span><span class="sxs-lookup"><span data-stu-id="22a60-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="22a60-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="22a60-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="22a60-115">Преобразователь, должна поддерживать 8-разрядных заголовков.</span><span class="sxs-lookup"><span data-stu-id="22a60-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="22a60-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="22a60-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="22a60-117">Отправленные и неотправленные данные сохраняются в неотправленные X.</span><span class="sxs-lookup"><span data-stu-id="22a60-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="22a60-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="22a60-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="22a60-119">Преобразователь следует создавать международные сообщения (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="22a60-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="22a60-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="22a60-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="22a60-121">Получателей Скрытой копии сообщения MAPI должно быть включено в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="22a60-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="22a60-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="22a60-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="22a60-123">Не включайте поле идентификатор сообщения в исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="22a60-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="22a60-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="22a60-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="22a60-125">Преобразователь следует игнорировать заголовки сообщений за пределы организации.</span><span class="sxs-lookup"><span data-stu-id="22a60-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="22a60-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="22a60-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="22a60-127">Преобразователь только что следует отправить обычный текст.</span><span class="sxs-lookup"><span data-stu-id="22a60-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="22a60-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="22a60-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="22a60-129">Преобразователь, передается SMTP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="22a60-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="22a60-130">Этот флаг всегда должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="22a60-130">This flag must always be set.</span></span>
    
<span data-ttu-id="22a60-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="22a60-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="22a60-132">Преобразователь следует преобразовать из HTML в формат RTF в сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="22a60-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="22a60-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="22a60-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="22a60-134">Преобразователь следует использовать формат транспорта Neutral Encapsulation формата TNEF в сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="22a60-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="22a60-135">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="22a60-135">Return values</span></span>

<span data-ttu-id="22a60-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="22a60-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="22a60-137">Были переданы недопустимые флаги или *pmsg* или *pstm* имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="22a60-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="22a60-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="22a60-138">Remarks</span></span>

<span data-ttu-id="22a60-139">Поддерживается только для стандартных типов сообщений Outlook.</span><span class="sxs-lookup"><span data-stu-id="22a60-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="22a60-140">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="22a60-140">MFCMAPI reference</span></span>

<span data-ttu-id="22a60-141">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="22a60-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="22a60-142">**Файл**</span><span class="sxs-lookup"><span data-stu-id="22a60-142">**File**</span></span>|<span data-ttu-id="22a60-143">**Функция**</span><span class="sxs-lookup"><span data-stu-id="22a60-143">**Function**</span></span>|<span data-ttu-id="22a60-144">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="22a60-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="22a60-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="22a60-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="22a60-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="22a60-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="22a60-147">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="22a60-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="22a60-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="22a60-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="22a60-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="22a60-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="22a60-150">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="22a60-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22a60-151">См. также</span><span class="sxs-lookup"><span data-stu-id="22a60-151">See also</span></span>



[<span data-ttu-id="22a60-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22a60-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="22a60-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="22a60-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="22a60-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="22a60-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="22a60-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="22a60-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="22a60-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="22a60-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="22a60-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="22a60-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="22a60-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="22a60-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="22a60-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="22a60-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="22a60-160">Каноническое свойство PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="22a60-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="22a60-161">Каноническое свойство PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="22a60-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="22a60-162">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="22a60-162">MAPI Constants</span></span>](mapi-constants.md)

