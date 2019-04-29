---
title: Иконвертерсессионсеттекствраппинг
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
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="bf3cf-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="bf3cf-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="bf3cf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf3cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf3cf-105">Задает ширину обтекания текста для потока MIME, который будет возвращен преобразователем в [иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="bf3cf-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="bf3cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf3cf-106">Parameters</span></span>

 <span data-ttu-id="bf3cf-107">*Фвраптекст*</span><span class="sxs-lookup"><span data-stu-id="bf3cf-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="bf3cf-108">возврата Указывает, следует ли переносить текст или нет.</span><span class="sxs-lookup"><span data-stu-id="bf3cf-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="bf3cf-109">*Улврапвидс*</span><span class="sxs-lookup"><span data-stu-id="bf3cf-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="bf3cf-110">возврата Используемая ширина обтекания текста.</span><span class="sxs-lookup"><span data-stu-id="bf3cf-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf3cf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf3cf-111">Return value</span></span>

<span data-ttu-id="bf3cf-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf3cf-112">S_OK</span></span>
  
> <span data-ttu-id="bf3cf-113">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="bf3cf-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf3cf-114">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bf3cf-114">MFCMAPI reference</span></span>

<span data-ttu-id="bf3cf-115">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bf3cf-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf3cf-116">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bf3cf-116">**File**</span></span>|<span data-ttu-id="bf3cf-117">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bf3cf-117">**Function**</span></span>|<span data-ttu-id="bf3cf-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bf3cf-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf3cf-119">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="bf3cf-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="bf3cf-120">Импортемлтоимессаже</span><span class="sxs-lookup"><span data-stu-id="bf3cf-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="bf3cf-121">MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf3cf-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="bf3cf-122">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="bf3cf-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="bf3cf-123">Експортимессажетоемл</span><span class="sxs-lookup"><span data-stu-id="bf3cf-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="bf3cf-124">MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.</span><span class="sxs-lookup"><span data-stu-id="bf3cf-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf3cf-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bf3cf-125">See also</span></span>



[<span data-ttu-id="bf3cf-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf3cf-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="bf3cf-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="bf3cf-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="bf3cf-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="bf3cf-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="bf3cf-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="bf3cf-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="bf3cf-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="bf3cf-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="bf3cf-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="bf3cf-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="bf3cf-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="bf3cf-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="bf3cf-133">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="bf3cf-133">MAPI Constants</span></span>](mapi-constants.md)

