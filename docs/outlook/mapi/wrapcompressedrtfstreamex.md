---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391733"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="badee-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="badee-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="badee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="badee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="badee-105">Распаковывает тело сообщения электронной почты, который является в сжатом форматированный текст (RTF), указывает формат распакованных потока, при необходимости преобразует распакованных потока в его собственном формате и возвращает распакованных поток или преобразовать собственного потока.</span><span class="sxs-lookup"><span data-stu-id="badee-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="badee-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="badee-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="badee-107">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="badee-107">Exported by:</span></span>  <br/> |<span data-ttu-id="badee-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="badee-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="badee-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="badee-109">Called by:</span></span>  <br/> |<span data-ttu-id="badee-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="badee-110">Client</span></span>  <br/> |
|<span data-ttu-id="badee-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="badee-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="badee-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="badee-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="badee-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="badee-113">Parameters</span></span>

<span data-ttu-id="badee-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="badee-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="badee-115">[in] Это указатель на поток, который открывается на [PidTagRtfCompressed каноническое свойства](pidtagrtfcompressed-canonical-property.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="badee-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="badee-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="badee-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="badee-117">[in] Это указатель</span><span class="sxs-lookup"><span data-stu-id="badee-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="badee-118">Структура [RTF_WCSINFO](rtf_wcsinfo.md) , содержащая параметры для функции.</span><span class="sxs-lookup"><span data-stu-id="badee-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="badee-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="badee-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="badee-120">[out] Это указатель на место, где возвращается поток для распакованных RTF.</span><span class="sxs-lookup"><span data-stu-id="badee-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="badee-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="badee-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="badee-122">[out] Это указатель на структуру [RTF_WCSRETINFO](rtf_wcsretinfo.md) , который содержит сведения о формате возвращенные распакованных потока.</span><span class="sxs-lookup"><span data-stu-id="badee-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="badee-123">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="badee-123">Return values</span></span>

<span data-ttu-id="badee-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="badee-124">S_OK</span></span> 
  
- <span data-ttu-id="badee-125">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="badee-125">The function call is successful.</span></span>
    
<span data-ttu-id="badee-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="badee-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="badee-127">Возвращается, если флаг **MAPI_NATIVE_BODY** используется в сочетании с флагом **MAPI_MODIFY** в поле **ulFlags** структуры **RTF_WCSINFO** , на которую указывает *pWCSInfo* .</span><span class="sxs-lookup"><span data-stu-id="badee-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="badee-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="badee-128">Remarks</span></span>

<span data-ttu-id="badee-129">**WrapCompressedRTFStreamEx** позволяет получить доступ к тело сообщения электронной почты, инкапсулированную в сжатом формате RTF, распаковки в потоке возвращает распакованных потока и его формате, а также в потоке собственный текст.</span><span class="sxs-lookup"><span data-stu-id="badee-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="badee-130">Поток собственный текст может быть в формате RTF, обычный текст или HTML.</span><span class="sxs-lookup"><span data-stu-id="badee-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="badee-131">Объектная модель Microsoft Office Outlook предоставляет свойство **Body** **MailItem** объектов и [Свойств MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) , которое указывает формат основного текста.</span><span class="sxs-lookup"><span data-stu-id="badee-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="badee-132">В архитектуре решение, которое не является доверенным для Outlook вызывает диалоговые окна безопасности, созданные с охрана Outlook.</span><span class="sxs-lookup"><span data-stu-id="badee-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="badee-133">С помощью функции экспортированного MAPI **WrapCompressedRTFStreamEx** позволяет решение, которое требуется использовать вместо объектной модели Outlook MAPI и избежать этих диалоговых окон безопасности.</span><span class="sxs-lookup"><span data-stu-id="badee-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="badee-134">Так как **MAPI\_NATIVE_BODY** флаг нельзя использовать вместе с **MAPI\_изменить** флаг в поле **ulFlags** **RTF\_WCSINFO** структура указывает *pWCSInfo*доступны только собственный поток текста в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="badee-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="badee-135">Чтобы получить доступ к потоку собственный текст в режиме чтения и записи, следует использовать функцию **WrapCompressedRTFStream** .</span><span class="sxs-lookup"><span data-stu-id="badee-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="badee-136">См. также</span><span class="sxs-lookup"><span data-stu-id="badee-136">See also</span></span>

- [<span data-ttu-id="badee-137">Получение текста сообщения в виде сжатого RTF-файла и его преобразование в исходный формат</span><span class="sxs-lookup"><span data-stu-id="badee-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

