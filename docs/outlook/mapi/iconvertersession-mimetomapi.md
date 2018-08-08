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
ms.openlocfilehash: 03a67371c67d5f0ac346470ec7ab38bb67d5ce2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808785"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="1c718-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="1c718-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="1c718-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c718-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c718-105">Преобразование MIME-поток сообщений MAPI.</span><span class="sxs-lookup"><span data-stu-id="1c718-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="1c718-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c718-106">Parameters</span></span>

 <span data-ttu-id="1c718-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="1c718-107">_pstm_</span></span>
  
> <span data-ttu-id="1c718-108">[in] Интерфейс [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) поток MIME.</span><span class="sxs-lookup"><span data-stu-id="1c718-108">[in] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="1c718-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="1c718-109">_pmsg_</span></span>
  
> <span data-ttu-id="1c718-110">[out] Указатель на сообщение, чтобы загрузить.</span><span class="sxs-lookup"><span data-stu-id="1c718-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="1c718-111">В разделе mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="1c718-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="1c718-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="1c718-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="1c718-113">[in] Это значение должно быть **значение null**.</span><span class="sxs-lookup"><span data-stu-id="1c718-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="1c718-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c718-114">_ulFlags_</span></span>
  
> <span data-ttu-id="1c718-115">[in] Этот параметр определяет дополнительных действий, которые требуется предпринять при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="1c718-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="1c718-116">Он должен быть нуль (0), если не определенное действие необходимо принять или сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1c718-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="1c718-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="1c718-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="1c718-118">Отправленные и неотправленные данные сохраняются в неотправленные X.</span><span class="sxs-lookup"><span data-stu-id="1c718-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="1c718-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="1c718-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="1c718-120">MIME-поток — сообщение MAPI протокола SMTP (простой).</span><span class="sxs-lookup"><span data-stu-id="1c718-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="1c718-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="1c718-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="1c718-122">Получателей Скрытой копии MIME-поток должно быть включено в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="1c718-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="1c718-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="1c718-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="1c718-124">Чтобы форматированный текст (RTF) должны быть преобразованы в сообщении MAPI HTML-текста в потоке MIME.</span><span class="sxs-lookup"><span data-stu-id="1c718-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c718-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1c718-125">Return value</span></span>

<span data-ttu-id="1c718-126">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1c718-126">E_INVALIDARG</span></span>
  
> <span data-ttu-id="1c718-127">Указывает, что _pstm_ имеет **значение null**, _pmsg_ имеет **значение null**или _ulFlags_ является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="1c718-127">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1c718-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="1c718-128">Remarks</span></span>

<span data-ttu-id="1c718-129">Если указаны **CCSF_USE_RTF** как часть _ulFlags_ и хранилище сообщений назначения поддерживает HTML и RTF, сообщение MAPI преобразуются в HTML или RTF.</span><span class="sxs-lookup"><span data-stu-id="1c718-129">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="1c718-130">Если сообщение будет преобразовываться в формат RTF, сжимаются преобразованные формата RTF, весь HTML-код будут внедрены в строку сжатый формат RTF, а строка будет содержаться в [Каноническое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="1c718-130">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c718-131">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="1c718-131">MFCMAPI reference</span></span>

<span data-ttu-id="1c718-132">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="1c718-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c718-133">**����**</span><span class="sxs-lookup"><span data-stu-id="1c718-133">**File**</span></span>|<span data-ttu-id="1c718-134">**�������**</span><span class="sxs-lookup"><span data-stu-id="1c718-134">**Function**</span></span>|<span data-ttu-id="1c718-135">**�����������**</span><span class="sxs-lookup"><span data-stu-id="1c718-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c718-136">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="1c718-136">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1c718-137">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="1c718-137">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="1c718-138">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="1c718-138">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="1c718-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="1c718-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1c718-140">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="1c718-140">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="1c718-141">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="1c718-141">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c718-142">См. также</span><span class="sxs-lookup"><span data-stu-id="1c718-142">See also</span></span>



[<span data-ttu-id="1c718-143">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1c718-143">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="1c718-144">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="1c718-144">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="1c718-145">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="1c718-145">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="1c718-146">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="1c718-146">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="1c718-147">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="1c718-147">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="1c718-148">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="1c718-148">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="1c718-149">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="1c718-149">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="1c718-150">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="1c718-150">MAPI Constants</span></span>](mapi-constants.md)

