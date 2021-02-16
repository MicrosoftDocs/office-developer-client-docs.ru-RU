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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325776"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="59876-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="59876-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="59876-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59876-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59876-105">Распечатывает текст сообщения электронной почты в сжатом формате RTF, указывает формат расжатого потока, при желании преобразует расжатый поток в свой собственный формат и возвращает либо расжатый поток, либо преобразованный собственный поток.</span><span class="sxs-lookup"><span data-stu-id="59876-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="59876-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="59876-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59876-107">Экспортируется с помощью:</span><span class="sxs-lookup"><span data-stu-id="59876-107">Exported by:</span></span>  <br/> |<span data-ttu-id="59876-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="59876-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="59876-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="59876-109">Called by:</span></span>  <br/> |<span data-ttu-id="59876-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="59876-110">Client</span></span>  <br/> |
|<span data-ttu-id="59876-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="59876-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="59876-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="59876-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="59876-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="59876-113">Parameters</span></span>

<span data-ttu-id="59876-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="59876-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="59876-115">[in] Это указатель на поток, который открывается в каноническом свойстве [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="59876-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="59876-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="59876-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="59876-117">[in] Это указатель на</span><span class="sxs-lookup"><span data-stu-id="59876-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="59876-118">[RTF_WCSINFO,](rtf_wcsinfo.md) которая содержит параметры функции.</span><span class="sxs-lookup"><span data-stu-id="59876-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="59876-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="59876-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="59876-120">[out] Это указатель на расположение, в котором возвращается поток для расшифрованного RTF.</span><span class="sxs-lookup"><span data-stu-id="59876-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="59876-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="59876-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="59876-122">[out] Это указатель на [структуру](rtf_wcsretinfo.md) RTF_WCSRETINFO, которая содержит сведения о формате возвращаемого раскодрованного потока.</span><span class="sxs-lookup"><span data-stu-id="59876-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="59876-123">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59876-123">Return values</span></span>

<span data-ttu-id="59876-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="59876-124">S_OK</span></span> 
  
- <span data-ttu-id="59876-125">Вызов функции успешно.</span><span class="sxs-lookup"><span data-stu-id="59876-125">The function call is successful.</span></span>
    
<span data-ttu-id="59876-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59876-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="59876-127">Возвращается, если флаг **MAPI_NATIVE_BODY** с флагом **MAPI_MODIFY** в поле **ulFlags** структуры  RTF_WCSINFO, на который указывает *pWCSInfo.*</span><span class="sxs-lookup"><span data-stu-id="59876-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="59876-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="59876-128">Remarks</span></span>

<span data-ttu-id="59876-129">**WrapCompressedRTFStreamEx** позволяет получить доступ к тексту сообщения электронной почты, инкапсулированного в сжатый RTF путем сжатия потока, возвращает расжатый поток и его формат, а также, при желании, собственный поток тела.</span><span class="sxs-lookup"><span data-stu-id="59876-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="59876-130">Встроенный поток текста может быть в формате RTF, обычном тексте или HTML.</span><span class="sxs-lookup"><span data-stu-id="59876-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="59876-131">Объектная Microsoft Office Outlook предоставляет свойство **Body** для объектов **MailItem** и [свойство MailItem.BodyFormat (Outlook),](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) которое указывает формат текста текста.</span><span class="sxs-lookup"><span data-stu-id="59876-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="59876-132">По проекту решение, которое не является доверенным в Outlook, вызывает диалоговые окна безопасности, созданные с помощью Безопасности Outlook.</span><span class="sxs-lookup"><span data-stu-id="59876-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="59876-133">Использование экспортируемой функции MAPI **WrapCompressedRTFStreamEx** позволяет решению использовать MAPI вместо объектной модели Outlook и избегать использования этих диалоговых окной безопасности.</span><span class="sxs-lookup"><span data-stu-id="59876-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="59876-134">Так как флаг **MAPI \_ NATIVE_BODY** нельзя объединить с флагом **MAPI \_ MODIFY** в поле **ulFlags** структуры **\_ WCSINFO RTF,** на который указывает *pWCSInfo,* доступ к потоку тела можно получить только в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="59876-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="59876-135">Чтобы получить доступ к потоку тела в режиме чтения и записи, необходимо использовать функцию **WrapCompressedRTFStream.**</span><span class="sxs-lookup"><span data-stu-id="59876-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59876-136">См. также</span><span class="sxs-lookup"><span data-stu-id="59876-136">See also</span></span>

- [<span data-ttu-id="59876-137">Извлечение тела сообщения в сжатом формате RTF и его преобразование в собственный формат</span><span class="sxs-lookup"><span data-stu-id="59876-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

