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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 81771a263a7496042d4950b465c0d5b03290399b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808795"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="d4d51-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="d4d51-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="d4d51-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4d51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4d51-105">Задает ширину потока MIME, который возвращает преобразователь в [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)обтекания.</span><span class="sxs-lookup"><span data-stu-id="d4d51-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="d4d51-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d4d51-106">Parameters</span></span>

 <span data-ttu-id="d4d51-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="d4d51-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="d4d51-108">[in] Следует ли перенос текста или нет.</span><span class="sxs-lookup"><span data-stu-id="d4d51-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="d4d51-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="d4d51-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="d4d51-110">[in] Текст, перенос ширины для использования.</span><span class="sxs-lookup"><span data-stu-id="d4d51-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d4d51-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d4d51-111">Return value</span></span>

<span data-ttu-id="d4d51-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d4d51-112">S_OK</span></span>
  
> <span data-ttu-id="d4d51-113">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d4d51-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d4d51-114">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="d4d51-114">MFCMAPI reference</span></span>

<span data-ttu-id="d4d51-115">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="d4d51-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d4d51-116">**����**</span><span class="sxs-lookup"><span data-stu-id="d4d51-116">**File**</span></span>|<span data-ttu-id="d4d51-117">**�������**</span><span class="sxs-lookup"><span data-stu-id="d4d51-117">**Function**</span></span>|<span data-ttu-id="d4d51-118">**�����������**</span><span class="sxs-lookup"><span data-stu-id="d4d51-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4d51-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d4d51-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d4d51-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="d4d51-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="d4d51-121">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="d4d51-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="d4d51-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d4d51-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d4d51-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="d4d51-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="d4d51-124">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="d4d51-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4d51-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d4d51-125">See also</span></span>



[<span data-ttu-id="d4d51-126">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4d51-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="d4d51-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="d4d51-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="d4d51-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="d4d51-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="d4d51-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="d4d51-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="d4d51-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="d4d51-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="d4d51-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="d4d51-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="d4d51-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="d4d51-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="d4d51-133">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d51-133">MAPI Constants</span></span>](mapi-constants.md)

