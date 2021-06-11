---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408427"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="e5e58-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="e5e58-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="e5e58-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5e58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5e58-105">Извлекает поток, который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e5e58-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="e5e58-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e5e58-106">Parameters</span></span>

 <span data-ttu-id="e5e58-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5e58-107">_pulFlags_</span></span>
  
> <span data-ttu-id="e5e58-108">[вышел] Указатель на битмаску флагов, которые контролируют, как следует сохранить текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="e5e58-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="e5e58-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e5e58-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e5e58-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5e58-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e5e58-111">Текст сообщения сохранен в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="e5e58-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="e5e58-112">Если флаг MAPI_UNICODE не установлен, текст сохранен в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e5e58-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="e5e58-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="e5e58-113">_pulFormat_</span></span>
  
> <span data-ttu-id="e5e58-114">[вышел] Указатель на битмаску флагов, которые контролируют формат сохраненного текста.</span><span class="sxs-lookup"><span data-stu-id="e5e58-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="e5e58-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e5e58-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e5e58-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="e5e58-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="e5e58-117">Текст сообщения должен быть сохранен в формате текста в формате Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="e5e58-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="e5e58-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="e5e58-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="e5e58-119">Текст сообщения должен быть сохранен в виде простого текста.</span><span class="sxs-lookup"><span data-stu-id="e5e58-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="e5e58-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="e5e58-120">_ppstm_</span></span>
  
> <span data-ttu-id="e5e58-121">[вышел] Указатель на указатель на поток, который будет содержать сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="e5e58-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5e58-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5e58-122">Return value</span></span>

<span data-ttu-id="e5e58-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5e58-123">S_OK</span></span> 
  
> <span data-ttu-id="e5e58-124">Поток был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="e5e58-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5e58-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5e58-125">Remarks</span></span>

<span data-ttu-id="e5e58-126">Объекты формы называют метод **IMAPIViewContext::GetSaveStream** для получения потока объекта, реализуемого интерфейсом **IStream** для поддержки обработки глагола Save As в виде просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="e5e58-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="e5e58-127">Метод [IMAPIForm::D oVerb,](imapiform-doverb.md) который реализуется на сервере форм и вызывается для вызова глагола для просмотра форм, не должен возвращаться, пока сообщение не будет полностью преобразовано в соответствующий текстовый формат и помещено в соответствующий поток.</span><span class="sxs-lookup"><span data-stu-id="e5e58-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e5e58-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e5e58-128">Notes to callers</span></span>

<span data-ttu-id="e5e58-129">Не записывай в поток, на который указывает _ppstm,_ прежде чем звонить **в GetSaveStream.**</span><span class="sxs-lookup"><span data-stu-id="e5e58-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="e5e58-130">Когда **GetSaveStream** возвращается, не сбрасывать положение указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="e5e58-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="e5e58-131">Этот указатель должен оставаться в конце сохраненного текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="e5e58-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5e58-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e5e58-132">See also</span></span>



[<span data-ttu-id="e5e58-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5e58-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

