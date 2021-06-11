---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Последнее изменение: 06 сентября 2019 г.'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160288"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="4a9e0-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="4a9e0-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="4a9e0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a9e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a9e0-105">Преобразует поток MIME в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="4a9e0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a9e0-106">Parameters</span></span>

 <span data-ttu-id="4a9e0-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="4a9e0-107">_pstm_</span></span>
  
> <span data-ttu-id="4a9e0-108">[in] [Интерфейс IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) к потоку MIME.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="4a9e0-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="4a9e0-109">_pmsg_</span></span>
  
> <span data-ttu-id="4a9e0-110">[in] Указатель на сообщение для загрузки.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="4a9e0-111">Чтобы заполнить API, вызываемая должна предоставить сообщение, поэтому объект должен пройти [в].</span><span class="sxs-lookup"><span data-stu-id="4a9e0-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="4a9e0-112">См. mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="4a9e0-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="4a9e0-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="4a9e0-114">[in] Это значение должно быть **null**.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="4a9e0-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4a9e0-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4a9e0-116">[in] Этот параметр определяет любые специальные действия, которые необходимо принять во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="4a9e0-117">Ноль (0), если не нужно принимать каких-либо конкретных действий, или сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4a9e0-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="4a9e0-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4a9e0-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="4a9e0-119">В X-Unsent сохраняется отправленная/неослабеваемая информация.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="4a9e0-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="4a9e0-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="4a9e0-121">Поток MIME для сообщения Простой протокол передачи почты (SMTP).</span><span class="sxs-lookup"><span data-stu-id="4a9e0-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="4a9e0-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="4a9e0-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="4a9e0-123">Получатели BCC потока MIME должны быть включены в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="4a9e0-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="4a9e0-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="4a9e0-125">HTML-текст потока MIME должен быть преобразован в формат rich Text Format (RTF) в сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="4a9e0-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4a9e0-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="4a9e0-127">Конвертер должен обрабатывать поток MIME как международное сообщение (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="4a9e0-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="4a9e0-128">Не поддерживается Outlook 2013 г.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a9e0-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a9e0-129">Return value</span></span>

<span data-ttu-id="4a9e0-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4a9e0-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="4a9e0-131">Указывает,  _что pstm является_ **null,**  _pmsg_ является **null** или  _ulFlags_ является недействительным.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4a9e0-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a9e0-132">Remarks</span></span>

<span data-ttu-id="4a9e0-133">Если вы указали CCSF_USE_RTF как часть _ulFlags,_ а хранилище сообщений назначения поддерживает HTML и RTF, сообщение MAPI будет преобразовано в HTML или RTF. </span><span class="sxs-lookup"><span data-stu-id="4a9e0-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="4a9e0-134">Если сообщение преобразовано в RTF, преобразованный формат будет сжат RTF, любой HTML будет встроен в сжатую строку RTF, а строка будет содержаться в каноническом свойстве [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="4a9e0-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4a9e0-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4a9e0-135">MFCMAPI reference</span></span>

<span data-ttu-id="4a9e0-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4a9e0-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="4a9e0-137">**File**</span></span>|<span data-ttu-id="4a9e0-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="4a9e0-138">**Function**</span></span>|<span data-ttu-id="4a9e0-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="4a9e0-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a9e0-140">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="4a9e0-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="4a9e0-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="4a9e0-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="4a9e0-142">MFCMAPI использует MimeToMAPI для преобразования файла EML в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="4a9e0-143">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="4a9e0-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="4a9e0-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="4a9e0-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="4a9e0-145">MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в файл EML.</span><span class="sxs-lookup"><span data-stu-id="4a9e0-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a9e0-146">См. также</span><span class="sxs-lookup"><span data-stu-id="4a9e0-146">See also</span></span>



[<span data-ttu-id="4a9e0-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a9e0-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="4a9e0-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="4a9e0-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="4a9e0-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="4a9e0-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="4a9e0-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="4a9e0-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="4a9e0-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="4a9e0-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="4a9e0-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="4a9e0-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="4a9e0-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="4a9e0-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="4a9e0-154">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="4a9e0-154">MAPI Constants</span></span>](mapi-constants.md)

