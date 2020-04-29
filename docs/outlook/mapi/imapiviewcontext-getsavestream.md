---
title: имапивиевконтекстжетсавестреам
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
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="08dd2-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="08dd2-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="08dd2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08dd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08dd2-105">Получает поток, который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="08dd2-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="08dd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08dd2-106">Parameters</span></span>

 <span data-ttu-id="08dd2-107">_пулфлагс_</span><span class="sxs-lookup"><span data-stu-id="08dd2-107">_pulFlags_</span></span>
  
> <span data-ttu-id="08dd2-108">вышли Указатель на битовую маску флагов, определяющих способ сохранения текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="08dd2-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="08dd2-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="08dd2-109">The following flag can be set:</span></span>
    
<span data-ttu-id="08dd2-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08dd2-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="08dd2-111">Текст сообщения сохраняется в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="08dd2-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="08dd2-112">Если флаг MAPI_UNICODE не установлен, текст сохраняется в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="08dd2-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="08dd2-113">_пулформат_</span><span class="sxs-lookup"><span data-stu-id="08dd2-113">_pulFormat_</span></span>
  
> <span data-ttu-id="08dd2-114">вышли Указатель на битовую маску флагов, определяющих формат сохраняемого текста.</span><span class="sxs-lookup"><span data-stu-id="08dd2-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="08dd2-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="08dd2-115">The following flags can be set:</span></span>
    
<span data-ttu-id="08dd2-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="08dd2-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="08dd2-117">Текст сообщения должен быть сохранен в виде форматированного текста в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="08dd2-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="08dd2-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="08dd2-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="08dd2-119">Текст сообщения должен быть сохранен в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="08dd2-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="08dd2-120">_ппстм_</span><span class="sxs-lookup"><span data-stu-id="08dd2-120">_ppstm_</span></span>
  
> <span data-ttu-id="08dd2-121">вышли Указатель на указатель на поток, который будет содержать сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="08dd2-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08dd2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08dd2-122">Return value</span></span>

<span data-ttu-id="08dd2-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="08dd2-123">S_OK</span></span> 
  
> <span data-ttu-id="08dd2-124">Поток успешно получен.</span><span class="sxs-lookup"><span data-stu-id="08dd2-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08dd2-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="08dd2-125">Remarks</span></span>

<span data-ttu-id="08dd2-126">Объекты формы вызывают метод **имапивиевконтекст:: жетсавестреам** для получения потока объект, который реализует интерфейс **IStream** для поддержки обработки команды "Сохранить как" в средстве просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="08dd2-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="08dd2-127">Метод [имапиформ::D оверб](imapiform-doverb.md) , который реализован на сервере формы и вызывается средством просмотра форм для вызова команды, не должен возвращать сообщение, пока сообщение не будет полностью преобразовано в соответствующий текстовый формат и помещается в соответствующий поток.</span><span class="sxs-lookup"><span data-stu-id="08dd2-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="08dd2-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="08dd2-128">Notes to callers</span></span>

<span data-ttu-id="08dd2-129">Не записываете в поток, на который указывает _ппстм_ , перед вызовом **жетсавестреам**.</span><span class="sxs-lookup"><span data-stu-id="08dd2-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="08dd2-130">Когда возвращается **жетсавестреам** , не сбрасывать положение указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="08dd2-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="08dd2-131">Этот указатель должен находиться в конце сохраненного текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="08dd2-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08dd2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="08dd2-132">See also</span></span>



[<span data-ttu-id="08dd2-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08dd2-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

