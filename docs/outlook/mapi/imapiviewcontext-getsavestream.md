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
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="9e993-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="9e993-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="9e993-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e993-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e993-105">Извлекает поток, который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e993-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="9e993-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e993-106">Parameters</span></span>

 <span data-ttu-id="9e993-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e993-107">_pulFlags_</span></span>
  
> <span data-ttu-id="9e993-108">[out] Указатель на битовуюметку флагов, которая управляет тем, как следует сохранить текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e993-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="9e993-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9e993-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9e993-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e993-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9e993-111">Текст сообщения сохранен в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="9e993-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="9e993-112">Если флаг MAPI_UNICODE не установлен, текст будет сохранен в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e993-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="9e993-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="9e993-113">_pulFormat_</span></span>
  
> <span data-ttu-id="9e993-114">[out] Указатель на битовуюmask флагов, которая управляет форматом сохраненного текста.</span><span class="sxs-lookup"><span data-stu-id="9e993-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="9e993-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9e993-115">The following flags can be set:</span></span>
    
<span data-ttu-id="9e993-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="9e993-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="9e993-117">Текст сообщения должен быть сохранен в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="9e993-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="9e993-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="9e993-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="9e993-119">Текст сообщения должен быть сохранен в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="9e993-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="9e993-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="9e993-120">_ppstm_</span></span>
  
> <span data-ttu-id="9e993-121">[out] Указатель на указатель на поток, который будет содержать сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="9e993-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e993-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e993-122">Return value</span></span>

<span data-ttu-id="9e993-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e993-123">S_OK</span></span> 
  
> <span data-ttu-id="9e993-124">Поток был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="9e993-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e993-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e993-125">Remarks</span></span>

<span data-ttu-id="9e993-126">Объекты форм вызывают метод **IMAPIViewContext::GetSaveStream,** чтобы получить поток объекта, реализующий **интерфейс IStream** для поддержки обработки команды "Сохранить как" в представлении формы.</span><span class="sxs-lookup"><span data-stu-id="9e993-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="9e993-127">Метод [IMAPIForm::D oVerb,](imapiform-doverb.md) который реализуется на сервере форм и вызывается просмотром формы для вызова команды, не должен возвращаться, пока сообщение не будет полностью преобразовано в соответствующий текстовый формат и помещено в соответствующий поток.</span><span class="sxs-lookup"><span data-stu-id="9e993-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9e993-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9e993-128">Notes to callers</span></span>

<span data-ttu-id="9e993-129">Не записывай в поток, на который указывает _ppstm,_ перед вызовом **GetSaveStream.**</span><span class="sxs-lookup"><span data-stu-id="9e993-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="9e993-130">При **возвращении GetSaveStream** не сбрасывать положение указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="9e993-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="9e993-131">Этот указатель должен оставаться в конце сохраненного текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e993-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e993-132">См. также</span><span class="sxs-lookup"><span data-stu-id="9e993-132">See also</span></span>



[<span data-ttu-id="9e993-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e993-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

