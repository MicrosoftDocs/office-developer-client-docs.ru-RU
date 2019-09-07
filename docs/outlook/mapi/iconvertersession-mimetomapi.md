---
title: иконвертерсессионмиметомапи
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
description: 'Дата последнего изменения: 06 сентября 2019 г.'
ms.openlocfilehash: f6f671cbfd5e14d602aaa31d31e54e859f068593
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790773"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="60997-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="60997-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="60997-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60997-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60997-105">Преобразует поток MIME в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="60997-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="60997-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="60997-106">Parameters</span></span>

 <span data-ttu-id="60997-107">_пстм_</span><span class="sxs-lookup"><span data-stu-id="60997-107">_pstm_</span></span>
  
> <span data-ttu-id="60997-108">возврата Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="60997-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="60997-109">_пмсг_</span><span class="sxs-lookup"><span data-stu-id="60997-109">_pmsg_</span></span>
  
> <span data-ttu-id="60997-110">возврата Указатель на сообщение для загрузки.</span><span class="sxs-lookup"><span data-stu-id="60997-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="60997-111">Вызывающий абонент должен предоставить сообщение для заполнения API, поэтому объект должен идти [in].</span><span class="sxs-lookup"><span data-stu-id="60997-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="60997-112">Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="60997-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="60997-113">_псзсрксрв_</span><span class="sxs-lookup"><span data-stu-id="60997-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="60997-114">возврата Это значение должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="60997-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="60997-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60997-115">_ulFlags_</span></span>
  
> <span data-ttu-id="60997-116">возврата Этот параметр определяет все специальные действия, выполняемые во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="60997-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="60997-117">Он должен иметь значение ноль (0), если не нужно предпринимать какие-либо действия или сочетания следующих значений:</span><span class="sxs-lookup"><span data-stu-id="60997-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="60997-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="60997-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="60997-119">Отправленные и неотправленные сведения хранятся в неотправленном виде X-a.</span><span class="sxs-lookup"><span data-stu-id="60997-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="60997-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="60997-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="60997-121">MIME-поток предназначен для простого сообщения протокола передачи MAPI.</span><span class="sxs-lookup"><span data-stu-id="60997-121">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="60997-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="60997-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="60997-123">Получатели скрытой копии MIME необходимо включить в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="60997-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="60997-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="60997-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="60997-125">Основной текст HTML-потока MIME должен быть преобразован в формат RTF в сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="60997-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="60997-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="60997-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="60997-127">Конвертер должен обрабатывать поток MIME в виде международного сообщения (ЕАИ/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="60997-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="60997-128">Не поддерживается в Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="60997-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60997-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60997-129">Return value</span></span>

<span data-ttu-id="60997-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60997-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="60997-131">Указывает, что _пстм_ имеет **значение NULL**, _ПМСГ_ имеет **значение NULL**или _ulFlags_ является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="60997-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="60997-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="60997-132">Remarks</span></span>

<span data-ttu-id="60997-133">Если вы указали **CCSF_USE_RTF** в составе _ulFlags_ и конечный банк сообщений поддерживает как HTML, так и RTF, сообщение MAPI будет преобразовано в формат HTML или RTF.</span><span class="sxs-lookup"><span data-stu-id="60997-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="60997-134">Если сообщение преобразуется в формат RTF, преобразованный формат будет сжат в формате RTF, любой HTML-код будет внедрен в сжатую строку RTF, а строка будет содержаться в [каноническое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="60997-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="60997-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="60997-135">MFCMAPI reference</span></span>

<span data-ttu-id="60997-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="60997-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="60997-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="60997-137">**File**</span></span>|<span data-ttu-id="60997-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="60997-138">**Function**</span></span>|<span data-ttu-id="60997-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="60997-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="60997-140">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="60997-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="60997-141">импортемлтоимессаже</span><span class="sxs-lookup"><span data-stu-id="60997-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="60997-142">MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="60997-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="60997-143">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="60997-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="60997-144">експортимессажетоемл</span><span class="sxs-lookup"><span data-stu-id="60997-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="60997-145">MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.</span><span class="sxs-lookup"><span data-stu-id="60997-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60997-146">См. также</span><span class="sxs-lookup"><span data-stu-id="60997-146">See also</span></span>



[<span data-ttu-id="60997-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60997-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="60997-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="60997-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="60997-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="60997-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="60997-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="60997-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="60997-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="60997-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="60997-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="60997-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="60997-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="60997-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="60997-154">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="60997-154">MAPI Constants</span></span>](mapi-constants.md)

