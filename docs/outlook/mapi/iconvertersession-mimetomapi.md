---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723035"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="4fc3f-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="4fc3f-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="4fc3f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fc3f-105">Преобразование MIME-поток сообщений MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="4fc3f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4fc3f-106">Parameters</span></span>

 <span data-ttu-id="4fc3f-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="4fc3f-107">_pstm_</span></span>
  
> <span data-ttu-id="4fc3f-108">[in] Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) поток MIME.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="4fc3f-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="4fc3f-109">_pmsg_</span></span>
  
> <span data-ttu-id="4fc3f-110">[out] Указатель на сообщение, чтобы загрузить.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="4fc3f-111">В разделе mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="4fc3f-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="4fc3f-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="4fc3f-113">[in] Это значение должно быть **значение null**.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="4fc3f-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fc3f-114">_ulFlags_</span></span>
  
> <span data-ttu-id="4fc3f-115">[in] Этот параметр определяет дополнительных действий, которые требуется предпринять при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="4fc3f-116">Он должен быть нуль (0), если не определенное действие необходимо принять или сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4fc3f-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="4fc3f-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc3f-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="4fc3f-118">Отправленные и неотправленные данные сохраняются в неотправленные X.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="4fc3f-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="4fc3f-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="4fc3f-120">MIME-поток — сообщение MAPI протокола SMTP (простой).</span><span class="sxs-lookup"><span data-stu-id="4fc3f-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="4fc3f-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="4fc3f-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="4fc3f-122">Получателей Скрытой копии MIME-поток должно быть включено в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="4fc3f-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="4fc3f-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="4fc3f-124">Чтобы форматированный текст (RTF) должны быть преобразованы в сообщении MAPI HTML-текста в потоке MIME.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="4fc3f-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4fc3f-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="4fc3f-126">Преобразователь должен обрабатывать MIME-поток как международные сообщение (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="4fc3f-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="4fc3f-127">Не поддерживается в Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fc3f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fc3f-128">Return value</span></span>

<span data-ttu-id="4fc3f-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4fc3f-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="4fc3f-130">Указывает, что _pstm_ имеет **значение null**, _pmsg_ имеет **значение null**или _ulFlags_ является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4fc3f-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="4fc3f-131">Remarks</span></span>

<span data-ttu-id="4fc3f-132">Если указаны **CCSF_USE_RTF** как часть _ulFlags_ и хранилище сообщений назначения поддерживает HTML и RTF, сообщение MAPI преобразуются в HTML или RTF.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="4fc3f-133">Если сообщение будет преобразовываться в формат RTF, сжимаются преобразованные формата RTF, весь HTML-код будут внедрены в строку сжатый формат RTF, а строка будет содержаться в [Каноническое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="4fc3f-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4fc3f-134">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4fc3f-134">MFCMAPI reference</span></span>

<span data-ttu-id="4fc3f-135">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4fc3f-136">**Файл**</span><span class="sxs-lookup"><span data-stu-id="4fc3f-136">**File**</span></span>|<span data-ttu-id="4fc3f-137">**Функция**</span><span class="sxs-lookup"><span data-stu-id="4fc3f-137">**Function**</span></span>|<span data-ttu-id="4fc3f-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="4fc3f-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4fc3f-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="4fc3f-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="4fc3f-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="4fc3f-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="4fc3f-141">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="4fc3f-142">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="4fc3f-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="4fc3f-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="4fc3f-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="4fc3f-144">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fc3f-145">См. также</span><span class="sxs-lookup"><span data-stu-id="4fc3f-145">See also</span></span>



[<span data-ttu-id="4fc3f-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fc3f-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="4fc3f-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="4fc3f-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="4fc3f-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="4fc3f-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="4fc3f-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="4fc3f-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="4fc3f-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="4fc3f-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="4fc3f-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="4fc3f-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="4fc3f-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="4fc3f-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="4fc3f-153">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc3f-153">MAPI Constants</span></span>](mapi-constants.md)

