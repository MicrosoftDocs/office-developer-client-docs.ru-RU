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
ms.openlocfilehash: 7981dc8550485aa22859c4a8dc25541bedf1217c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809256"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="49c3e-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="49c3e-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="49c3e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49c3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49c3e-105">Получает поток, в который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="49c3e-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="49c3e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="49c3e-106">Parameters</span></span>

 <span data-ttu-id="49c3e-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="49c3e-107">_pulFlags_</span></span>
  
> <span data-ttu-id="49c3e-108">[out] Указатель на битовую маску флагов, который определяет, как должны сохраняться текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="49c3e-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="49c3e-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="49c3e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="49c3e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49c3e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="49c3e-111">Текст сообщения сохраняются в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="49c3e-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="49c3e-112">Если флаг MAPI_UNICODE не установлен, текст сохраняется в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="49c3e-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="49c3e-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="49c3e-113">_pulFormat_</span></span>
  
> <span data-ttu-id="49c3e-114">[out] Указатель на битовую маску флагов, который управляет формата текста, сохраненного.</span><span class="sxs-lookup"><span data-stu-id="49c3e-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="49c3e-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="49c3e-115">The following flags can be set:</span></span>
    
<span data-ttu-id="49c3e-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="49c3e-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="49c3e-117">Текст сообщения является сохраняются как форматированный текст в форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="49c3e-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="49c3e-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="49c3e-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="49c3e-119">Текст сообщения является сохранен в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="49c3e-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="49c3e-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="49c3e-120">_ppstm_</span></span>
  
> <span data-ttu-id="49c3e-121">[out] Указатель на указатель в поток, который будет содержать сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="49c3e-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="49c3e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="49c3e-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="49c3e-123">S_OK</span></span> 
  
> <span data-ttu-id="49c3e-124">Поток был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="49c3e-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49c3e-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="49c3e-125">Remarks</span></span>

<span data-ttu-id="49c3e-126">Объекты формы вызовите метод **IMAPIViewContext::GetSaveStream** для извлечения потока объект, реализующий интерфейс **IStream** для обработки команды Сохранить как в средстве просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="49c3e-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="49c3e-127">Метод [IMAPIForm::DoVerb](imapiform-doverb.md) , который реализован на сервере формы и вызывается средством просмотра формы для вызова команды, не должен возвращать, пока сообщение полностью преобразуется в соответствующий текстовый формат и помещаются в соответствующие потока.</span><span class="sxs-lookup"><span data-stu-id="49c3e-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="49c3e-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="49c3e-128">Notes to callers</span></span>

<span data-ttu-id="49c3e-129">Не записывать в поток, который указывает _ppstm_ до вызова метода **GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="49c3e-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="49c3e-130">При возврате **GetSaveStream** , не сбрасывает позицию указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="49c3e-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="49c3e-131">В этом указатель должен оставаться в конце текста сохраненные сообщения.</span><span class="sxs-lookup"><span data-stu-id="49c3e-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49c3e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="49c3e-132">See also</span></span>



[<span data-ttu-id="49c3e-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49c3e-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

