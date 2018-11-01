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
ms.openlocfilehash: a89f6dd14e8bbea9d0d4145dc05bf332af95234a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573636"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="7d778-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="7d778-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="7d778-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d778-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d778-105">Задает ширину потока MIME, который возвращает преобразователь в [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)обтекания.</span><span class="sxs-lookup"><span data-stu-id="7d778-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="7d778-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d778-106">Parameters</span></span>

 <span data-ttu-id="7d778-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="7d778-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="7d778-108">[in] Следует ли перенос текста или нет.</span><span class="sxs-lookup"><span data-stu-id="7d778-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="7d778-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="7d778-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="7d778-110">[in] Текст, перенос ширины для использования.</span><span class="sxs-lookup"><span data-stu-id="7d778-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d778-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d778-111">Return value</span></span>

<span data-ttu-id="7d778-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d778-112">S_OK</span></span>
  
> <span data-ttu-id="7d778-113">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7d778-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d778-114">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7d778-114">MFCMAPI reference</span></span>

<span data-ttu-id="7d778-115">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7d778-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d778-116">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7d778-116">**File**</span></span>|<span data-ttu-id="7d778-117">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7d778-117">**Function**</span></span>|<span data-ttu-id="7d778-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7d778-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d778-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="7d778-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="7d778-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="7d778-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="7d778-121">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d778-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="7d778-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="7d778-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="7d778-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="7d778-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="7d778-124">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="7d778-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d778-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7d778-125">See also</span></span>



[<span data-ttu-id="7d778-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d778-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="7d778-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="7d778-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="7d778-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="7d778-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="7d778-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="7d778-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="7d778-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="7d778-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="7d778-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="7d778-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="7d778-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="7d778-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="7d778-133">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="7d778-133">MAPI Constants</span></span>](mapi-constants.md)

