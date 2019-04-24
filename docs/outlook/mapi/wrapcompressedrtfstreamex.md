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
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="c62aa-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="c62aa-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="c62aa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c62aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c62aa-105">Распаковывает текст сообщения электронной почты, который находится в формате RTF, указывает формат распакованного потока, при необходимости преобразует Распакованный поток в исходный формат и возвращает либо несжатый поток, либо преобразованный машинный поток.</span><span class="sxs-lookup"><span data-stu-id="c62aa-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c62aa-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c62aa-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c62aa-107">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="c62aa-107">Exported by:</span></span>  <br/> |<span data-ttu-id="c62aa-108">MSMapi32. dll</span><span class="sxs-lookup"><span data-stu-id="c62aa-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c62aa-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c62aa-109">Called by:</span></span>  <br/> |<span data-ttu-id="c62aa-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="c62aa-110">Client</span></span>  <br/> |
|<span data-ttu-id="c62aa-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c62aa-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="c62aa-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="c62aa-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="c62aa-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="c62aa-113">Parameters</span></span>

<span data-ttu-id="c62aa-114">_Лпкомпресседртфстреам_</span><span class="sxs-lookup"><span data-stu-id="c62aa-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="c62aa-115">возврата Это указатель на поток, Открытый на [канонИческое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="c62aa-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="c62aa-116">_Пвксинфо_</span><span class="sxs-lookup"><span data-stu-id="c62aa-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="c62aa-117">возврата Это указатель на</span><span class="sxs-lookup"><span data-stu-id="c62aa-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="c62aa-118">Структура [ртф_вксинфо](rtf_wcsinfo.md) , содержащая параметры функции.</span><span class="sxs-lookup"><span data-stu-id="c62aa-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="c62aa-119">_Лппункомпресседртфстреам_</span><span class="sxs-lookup"><span data-stu-id="c62aa-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="c62aa-120">вышли Это указатель на расположение, в котором возвращается поток для распакованного RTF.</span><span class="sxs-lookup"><span data-stu-id="c62aa-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="c62aa-121">_Претинфо_</span><span class="sxs-lookup"><span data-stu-id="c62aa-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="c62aa-122">вышли Это указатель на структуру [ртф_вксретинфо](rtf_wcsretinfo.md) , которая содержит сведения о формате возвращенного распакованного потока.</span><span class="sxs-lookup"><span data-stu-id="c62aa-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c62aa-123">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c62aa-123">Return values</span></span>

<span data-ttu-id="c62aa-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="c62aa-124">S_OK</span></span> 
  
- <span data-ttu-id="c62aa-125">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c62aa-125">The function call is successful.</span></span>
    
<span data-ttu-id="c62aa-126">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="c62aa-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="c62aa-127">Это возвращается в том случае, если флаг **мапи_нативе_боди** сочетается с флагом **Мапи_модифи** в поле **ulFlags** структуры **ртф_вксинфо** , на которую указывает *пвксинфо* .</span><span class="sxs-lookup"><span data-stu-id="c62aa-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c62aa-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="c62aa-128">Remarks</span></span>

<span data-ttu-id="c62aa-129">**Врапкомпресседртфстреамекс** позволяет получить доступ к тексту сообщения электронной почты, инкапсулированного в сжатом формате RTF, путем распаковки потока, возвращения распакованного потока и его формата, а также собственного потока основного текста.</span><span class="sxs-lookup"><span data-stu-id="c62aa-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="c62aa-130">Собственный поток основного текста может быть в формате RTF, обычного текста или HTML.</span><span class="sxs-lookup"><span data-stu-id="c62aa-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="c62aa-131">Объектная модель Microsoft Office Outlook предоставляет свойство **Body** для объектов **MailItem** и [свойство MailItem. BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) , которое указывает формат основного текста.</span><span class="sxs-lookup"><span data-stu-id="c62aa-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="c62aa-132">При проектировании решение, не пользующееся доверием Outlook, вызывает диалоговые окна безопасности, созданные в Outlook Security Guard.</span><span class="sxs-lookup"><span data-stu-id="c62aa-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="c62aa-133">Использование экспортированной функции MAPI **врапкомпресседртфстреамекс** позволяет решению использовать MAPI вместо объектной модели Outlook и избегать использования диалоговых окон безопасности.</span><span class="sxs-lookup"><span data-stu-id="c62aa-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="c62aa-134">Так как **флаг\_нативе_боди MAPI** не может быть объединен с флагом **MAPI\_Modify** в поле **ulFlags** структуры **RTF\_вксинфо** , на который указывает *пвксинфо*, можно получить доступ только к собственному поток основного текста в режиме "только чтение".</span><span class="sxs-lookup"><span data-stu-id="c62aa-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="c62aa-135">Чтобы получить доступ к основному потоку основного текста в режиме чтения и записи, следует использовать функцию **врапкомпресседртфстреам** .</span><span class="sxs-lookup"><span data-stu-id="c62aa-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c62aa-136">См. также</span><span class="sxs-lookup"><span data-stu-id="c62aa-136">See also</span></span>

- [<span data-ttu-id="c62aa-137">Получение текста сообщения в сжатом формате RTF и его преобразование в исходный формат</span><span class="sxs-lookup"><span data-stu-id="c62aa-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

