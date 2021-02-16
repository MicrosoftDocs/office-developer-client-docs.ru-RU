---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423589"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="cb181-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="cb181-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="cb181-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb181-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb181-105">Задает ширину обтекания текстом для потока MIME, который преобразователь вернет в [IConverterSession::MAPIToMIMEStm.](iconvertersession-mapitomimestm.md)</span><span class="sxs-lookup"><span data-stu-id="cb181-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="cb181-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb181-106">Parameters</span></span>

 <span data-ttu-id="cb181-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="cb181-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="cb181-108">[in] Следует ли обтекать текст.</span><span class="sxs-lookup"><span data-stu-id="cb181-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="cb181-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="cb181-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="cb181-110">[in] Ширина обтекаемого текста.</span><span class="sxs-lookup"><span data-stu-id="cb181-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cb181-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb181-111">Return value</span></span>

<span data-ttu-id="cb181-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb181-112">S_OK</span></span>
  
> <span data-ttu-id="cb181-113">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="cb181-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb181-114">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cb181-114">MFCMAPI reference</span></span>

<span data-ttu-id="cb181-115">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cb181-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb181-116">**Файл**</span><span class="sxs-lookup"><span data-stu-id="cb181-116">**File**</span></span>|<span data-ttu-id="cb181-117">**Функция**</span><span class="sxs-lookup"><span data-stu-id="cb181-117">**Function**</span></span>|<span data-ttu-id="cb181-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="cb181-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb181-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="cb181-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="cb181-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="cb181-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="cb181-121">MFCMAPI использует MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="cb181-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="cb181-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="cb181-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="cb181-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="cb181-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="cb181-124">MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в EML-файл.</span><span class="sxs-lookup"><span data-stu-id="cb181-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb181-125">См. также</span><span class="sxs-lookup"><span data-stu-id="cb181-125">See also</span></span>



[<span data-ttu-id="cb181-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb181-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="cb181-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="cb181-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="cb181-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="cb181-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="cb181-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="cb181-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="cb181-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="cb181-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="cb181-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="cb181-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="cb181-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="cb181-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="cb181-133">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="cb181-133">MAPI Constants</span></span>](mapi-constants.md)

