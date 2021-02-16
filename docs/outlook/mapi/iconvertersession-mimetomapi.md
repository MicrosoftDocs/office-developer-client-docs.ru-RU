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
description: 'Last modified: September 06, 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160288"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="b8d0e-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="b8d0e-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="b8d0e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8d0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8d0e-105">Преобразует поток MIME в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="b8d0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8d0e-106">Parameters</span></span>

 <span data-ttu-id="b8d0e-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="b8d0e-107">_pstm_</span></span>
  
> <span data-ttu-id="b8d0e-108">[in] [Интерфейс IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="b8d0e-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="b8d0e-109">_pmsg_</span></span>
  
> <span data-ttu-id="b8d0e-110">[in] Указатель на сообщение для загрузки.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="b8d0e-111">Вызываемая группа должна предоставить сообщение, чтобы API заполнил его, поэтому объект должен пройти [в].</span><span class="sxs-lookup"><span data-stu-id="b8d0e-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="b8d0e-112">Определение типа **LPMESSAGE** см. в mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="b8d0e-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="b8d0e-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="b8d0e-114">[in] Это значение должно быть **null.**</span><span class="sxs-lookup"><span data-stu-id="b8d0e-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="b8d0e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8d0e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b8d0e-116">[in] Этот параметр определяет любые специальные действия, которые необходимо принять во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="b8d0e-117">Значение должно быть нулем (0), если не нужно никаких конкретных действий, или сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b8d0e-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="b8d0e-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b8d0e-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="b8d0e-119">Отправленные или неавентные сведения сохраняются в X-Unsent.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="b8d0e-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="b8d0e-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="b8d0e-121">Поток MIME для сообщения SMTP.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="b8d0e-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="b8d0e-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="b8d0e-123">Получатели BCC потока MIME должны быть включены в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="b8d0e-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="b8d0e-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="b8d0e-125">Текст HTML-текста потока MIME должен быть преобразован в формат RTF в сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="b8d0e-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b8d0e-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="b8d0e-127">Преобразователь должен обрабатывать поток MIME как международное сообщение (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="b8d0e-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="b8d0e-128">Не поддерживается в Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8d0e-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8d0e-129">Return value</span></span>

<span data-ttu-id="b8d0e-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b8d0e-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="b8d0e-131">Указывает,  _что pstm_ имеет **null,**  _pmsg_ — **null,**  _или ulFlags_ является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b8d0e-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8d0e-132">Remarks</span></span>

<span data-ttu-id="b8d0e-133">Если вы указали CCSF_USE_RTF как часть _ulFlags,_ а конечное хранилище сообщений поддерживает htmL и RTF, сообщение MAPI будет преобразовано в HTML или RTF. </span><span class="sxs-lookup"><span data-stu-id="b8d0e-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="b8d0e-134">Если сообщение преобразуется в формат RTF, преобразованный формат будет сжатым форматом RTF, любой HTML-код будет внедрен в сжатую строку RTF, а строка будет содержаться в каноническом свойстве [PidTagRtfCompressed.](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b8d0e-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8d0e-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b8d0e-135">MFCMAPI reference</span></span>

<span data-ttu-id="b8d0e-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8d0e-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b8d0e-137">**File**</span></span>|<span data-ttu-id="b8d0e-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b8d0e-138">**Function**</span></span>|<span data-ttu-id="b8d0e-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b8d0e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8d0e-140">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="b8d0e-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="b8d0e-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="b8d0e-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="b8d0e-142">MFCMAPI использует MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="b8d0e-143">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="b8d0e-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="b8d0e-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="b8d0e-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="b8d0e-145">MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в EML-файл.</span><span class="sxs-lookup"><span data-stu-id="b8d0e-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8d0e-146">См. также</span><span class="sxs-lookup"><span data-stu-id="b8d0e-146">See also</span></span>



[<span data-ttu-id="b8d0e-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8d0e-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="b8d0e-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="b8d0e-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="b8d0e-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="b8d0e-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="b8d0e-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="b8d0e-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="b8d0e-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="b8d0e-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="b8d0e-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="b8d0e-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="b8d0e-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="b8d0e-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="b8d0e-154">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="b8d0e-154">MAPI Constants</span></span>](mapi-constants.md)

