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
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="5b85e-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="5b85e-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="5b85e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b85e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b85e-105">Декомпрессирует тело сообщения электронной почты, которое находится в сжатом формате богатого текста (RTF), указывает формат декомпрессируемого потока, необязательным образом преобразует декомпрессируемый поток в свой родной формат и возвращает либо декомпрессованный поток, либо преобразованный родной поток.</span><span class="sxs-lookup"><span data-stu-id="5b85e-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5b85e-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5b85e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b85e-107">Экспортируемая по:</span><span class="sxs-lookup"><span data-stu-id="5b85e-107">Exported by:</span></span>  <br/> |<span data-ttu-id="5b85e-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="5b85e-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="5b85e-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5b85e-109">Called by:</span></span>  <br/> |<span data-ttu-id="5b85e-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="5b85e-110">Client</span></span>  <br/> |
|<span data-ttu-id="5b85e-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5b85e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5b85e-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="5b85e-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="5b85e-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="5b85e-113">Parameters</span></span>

<span data-ttu-id="5b85e-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="5b85e-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="5b85e-115">[in] Это указатель потока, открываемого в каноническом свойстве [сообщения PidTagRtfCompressed.](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5b85e-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="5b85e-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="5b85e-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="5b85e-117">[in] Это указатель на</span><span class="sxs-lookup"><span data-stu-id="5b85e-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="5b85e-118">[RTF_WCSINFO,](rtf_wcsinfo.md) которая содержит параметры функции.</span><span class="sxs-lookup"><span data-stu-id="5b85e-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="5b85e-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="5b85e-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="5b85e-120">[вышел] Это указатель на расположение, в котором возвращается поток для декомпрессированного RTF.</span><span class="sxs-lookup"><span data-stu-id="5b85e-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="5b85e-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="5b85e-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="5b85e-122">[вышел] Это указатель на структуру [RTF_WCSRETINFO,](rtf_wcsretinfo.md) которая содержит сведения о формате возвращенного декомпрессированного потока.</span><span class="sxs-lookup"><span data-stu-id="5b85e-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5b85e-123">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5b85e-123">Return values</span></span>

<span data-ttu-id="5b85e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b85e-124">S_OK</span></span> 
  
- <span data-ttu-id="5b85e-125">Вызов функции является успешным.</span><span class="sxs-lookup"><span data-stu-id="5b85e-125">The function call is successful.</span></span>
    
<span data-ttu-id="5b85e-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b85e-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="5b85e-127">Это возвращается, **если флаг MAPI_NATIVE_BODY** совмещен  с флагом MAPI_MODIFY в **поле ulFlags** структуры RTF_WCSINFO, на который указывает *pWCSInfo* . </span><span class="sxs-lookup"><span data-stu-id="5b85e-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5b85e-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b85e-128">Remarks</span></span>

<span data-ttu-id="5b85e-129">**WrapCompressedRTFStreamEx** позволяет получить доступ к тексту сообщения электронной почты, инкапсулированного в сжатом RTF путем декомпрессии потока, возвращает декомпрессированный поток и его формат, а также необязательно родной поток тела.</span><span class="sxs-lookup"><span data-stu-id="5b85e-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="5b85e-130">Поток родного тела может быть в RTF, простом тексте или HTML.</span><span class="sxs-lookup"><span data-stu-id="5b85e-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="5b85e-131">Объектная Microsoft Office Outlook предоставляет свойство  Body для объектов **MailItem** и [свойство MailItem.BodyFormat (Outlook),](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) которое указывает формат текста тела.</span><span class="sxs-lookup"><span data-stu-id="5b85e-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="5b85e-132">По проекту решение, которому не доверяют Outlook вызывает диалоговые окна безопасности, созданные Outlook security Guard.</span><span class="sxs-lookup"><span data-stu-id="5b85e-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="5b85e-133">Использование экспортируемой функции **MAPI WrapCompressedRTFStreamEx** позволяет решению использовать MAPI вместо объектной модели Outlook и избегать этих диалоговых ящиков безопасности.</span><span class="sxs-lookup"><span data-stu-id="5b85e-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="5b85e-134">Так как флаг **mapi \_ NATIVE_BODY** нельзя сочетать с флагом **MAPI \_ MODIFY** в поле **ulFlags** структуры **\_ WCSINFO RTF,** на который указывает *pWCSInfo,* доступ к родному потоку тела можно получить только в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5b85e-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="5b85e-135">Чтобы получить доступ к родному потоку тела в режиме чтения и записи, необходимо использовать функцию **WrapCompressedRTFStream.**</span><span class="sxs-lookup"><span data-stu-id="5b85e-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b85e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="5b85e-136">See also</span></span>

- [<span data-ttu-id="5b85e-137">Извлечение тела сообщения в сжатых RTF и преобразование его в свой родной формат</span><span class="sxs-lookup"><span data-stu-id="5b85e-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

