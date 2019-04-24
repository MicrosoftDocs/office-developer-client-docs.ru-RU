---
title: Иконвертерсессионмиметомапи
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326931"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="d900d-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="d900d-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="d900d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d900d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d900d-105">Преобразует поток MIME в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="d900d-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="d900d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d900d-106">Parameters</span></span>

 <span data-ttu-id="d900d-107">_пстм_</span><span class="sxs-lookup"><span data-stu-id="d900d-107">_pstm_</span></span>
  
> <span data-ttu-id="d900d-108">возврата Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="d900d-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="d900d-109">_ПМСГ_</span><span class="sxs-lookup"><span data-stu-id="d900d-109">_pmsg_</span></span>
  
> <span data-ttu-id="d900d-110">вышли Указатель на сообщение для загрузки.</span><span class="sxs-lookup"><span data-stu-id="d900d-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="d900d-111">Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="d900d-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="d900d-112">_Псзсрксрв_</span><span class="sxs-lookup"><span data-stu-id="d900d-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="d900d-113">возврата Это значение должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="d900d-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="d900d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d900d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="d900d-115">возврата Этот параметр определяет все специальные действия, выполняемые во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="d900d-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="d900d-116">Он должен иметь значение ноль (0), если не нужно предпринимать какие-либо действия или сочетания следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d900d-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="d900d-117">ККСФ_ЕМБЕДДЕД_МЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="d900d-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="d900d-118">Отправленные и неотправленные сведения хранятся в неотправленном виде X-a.</span><span class="sxs-lookup"><span data-stu-id="d900d-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="d900d-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="d900d-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="d900d-120">MIME-поток предназначен для простого сообщения протокола передачи MAPI.</span><span class="sxs-lookup"><span data-stu-id="d900d-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="d900d-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="d900d-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="d900d-122">Получатели СКРЫТой копии MIME необходимо включить в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="d900d-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="d900d-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="d900d-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="d900d-124">Основной текст HTML-потока MIME должен быть преобразован в формат RTF в сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="d900d-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="d900d-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d900d-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="d900d-126">Конвертер должен обрабатывать поток MIME в виде международного сообщения (ЕАИ/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="d900d-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="d900d-127">Не поддерживается в Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="d900d-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d900d-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d900d-128">Return value</span></span>

<span data-ttu-id="d900d-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d900d-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="d900d-130">Указывает, что _пстм_ имеет **значение NULL**, _ПМСГ_ имеет **значение NULL**или _ulFlags_ является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d900d-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d900d-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="d900d-131">Remarks</span></span>

<span data-ttu-id="d900d-132">Если вы указали **кксф_усе_ртф** в составе _ulFlags_ и конечный банк сообщений поддерживает как HTML, так и RTF, сообщение MAPI будет преобразовано в формат HTML или RTF.</span><span class="sxs-lookup"><span data-stu-id="d900d-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="d900d-133">Если сообщение преобразуется в формат RTF, преобразованный формат будет сжат в формате RTF, любой HTML-код будет внедрен в сжатую строку RTF, а строка будет содержаться в [канонИческое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="d900d-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d900d-134">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d900d-134">MFCMAPI reference</span></span>

<span data-ttu-id="d900d-135">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d900d-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d900d-136">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d900d-136">**File**</span></span>|<span data-ttu-id="d900d-137">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d900d-137">**Function**</span></span>|<span data-ttu-id="d900d-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d900d-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d900d-139">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="d900d-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d900d-140">Импортемлтоимессаже</span><span class="sxs-lookup"><span data-stu-id="d900d-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="d900d-141">MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="d900d-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="d900d-142">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="d900d-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d900d-143">Експортимессажетоемл</span><span class="sxs-lookup"><span data-stu-id="d900d-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="d900d-144">MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.</span><span class="sxs-lookup"><span data-stu-id="d900d-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d900d-145">См. также</span><span class="sxs-lookup"><span data-stu-id="d900d-145">See also</span></span>



[<span data-ttu-id="d900d-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d900d-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="d900d-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="d900d-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="d900d-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="d900d-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="d900d-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="d900d-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="d900d-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="d900d-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="d900d-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="d900d-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="d900d-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="d900d-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="d900d-153">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="d900d-153">MAPI Constants</span></span>](mapi-constants.md)

