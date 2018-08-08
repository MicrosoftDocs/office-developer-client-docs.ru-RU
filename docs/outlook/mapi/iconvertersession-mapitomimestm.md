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
ms.openlocfilehash: b59114926d44ba613efbbde1c8dd5d17c26756c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808784"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="42f22-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="42f22-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="42f22-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42f22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42f22-105">Преобразование сообщения MAPI в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="42f22-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="42f22-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42f22-106">Parameters</span></span>

 <span data-ttu-id="42f22-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="42f22-107">_pmsg_</span></span>
  
> <span data-ttu-id="42f22-108">[in] Указатель на сообщение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="42f22-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="42f22-109">В разделе mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="42f22-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="42f22-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="42f22-110">_pstm_</span></span>
  
> <span data-ttu-id="42f22-111">[out] Интерфейс [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) для вывода в потоке.</span><span class="sxs-lookup"><span data-stu-id="42f22-111">[out] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="42f22-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="42f22-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="42f22-113">[in] Флаги, указывающие конкретные действия для преобразователя:</span><span class="sxs-lookup"><span data-stu-id="42f22-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="42f22-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="42f22-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="42f22-115">Преобразователь, должна поддерживать 8-разрядных заголовков.</span><span class="sxs-lookup"><span data-stu-id="42f22-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="42f22-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="42f22-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="42f22-117">Отправленные и неотправленные данные сохраняются в неотправленные X.</span><span class="sxs-lookup"><span data-stu-id="42f22-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="42f22-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="42f22-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="42f22-119">Преобразователь следует создавать международные сообщения (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="42f22-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="42f22-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="42f22-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="42f22-121">Получателей Скрытой копии сообщения MAPI должно быть включено в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="42f22-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="42f22-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="42f22-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="42f22-123">Не включайте поле идентификатор сообщения в исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="42f22-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="42f22-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="42f22-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="42f22-125">Преобразователь следует игнорировать заголовки сообщений за пределы организации.</span><span class="sxs-lookup"><span data-stu-id="42f22-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="42f22-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="42f22-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="42f22-127">Преобразователь только что следует отправить обычный текст.</span><span class="sxs-lookup"><span data-stu-id="42f22-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="42f22-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="42f22-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="42f22-129">Преобразователь, передается SMTP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="42f22-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="42f22-130">Этот флаг всегда должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="42f22-130">This flag must always be set.</span></span>
    
<span data-ttu-id="42f22-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="42f22-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="42f22-132">Преобразователь следует преобразовать из HTML в формат RTF в сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="42f22-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="42f22-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="42f22-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="42f22-134">Преобразователь следует использовать формат транспорта Neutral Encapsulation формата TNEF в сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="42f22-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="42f22-135">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="42f22-135">Return values</span></span>

<span data-ttu-id="42f22-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="42f22-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="42f22-137">Были переданы недопустимые флаги или *pmsg* или *pstm* имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="42f22-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42f22-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="42f22-138">Remarks</span></span>

<span data-ttu-id="42f22-139">Поддерживается только для стандартных типов сообщений Outlook.</span><span class="sxs-lookup"><span data-stu-id="42f22-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="42f22-140">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="42f22-140">MFCMAPI reference</span></span>

<span data-ttu-id="42f22-141">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="42f22-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="42f22-142">**����**</span><span class="sxs-lookup"><span data-stu-id="42f22-142">**File**</span></span>|<span data-ttu-id="42f22-143">**�������**</span><span class="sxs-lookup"><span data-stu-id="42f22-143">**Function**</span></span>|<span data-ttu-id="42f22-144">**�����������**</span><span class="sxs-lookup"><span data-stu-id="42f22-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="42f22-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="42f22-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="42f22-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="42f22-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="42f22-147">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="42f22-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="42f22-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="42f22-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="42f22-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="42f22-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="42f22-150">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="42f22-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42f22-151">См. также</span><span class="sxs-lookup"><span data-stu-id="42f22-151">See also</span></span>



[<span data-ttu-id="42f22-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42f22-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="42f22-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="42f22-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="42f22-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="42f22-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="42f22-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="42f22-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="42f22-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="42f22-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="42f22-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="42f22-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="42f22-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="42f22-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="42f22-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="42f22-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="42f22-160">Каноническое свойство PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="42f22-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="42f22-161">������������ �������� PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="42f22-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="42f22-162">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="42f22-162">MAPI Constants</span></span>](mapi-constants.md)

