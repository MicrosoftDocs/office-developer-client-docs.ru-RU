---
title: Имапивиевконтекстжетсавестреам
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351130"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="7c7e0-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="7c7e0-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="7c7e0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c7e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c7e0-105">Получает поток, который будет использоваться для сохранения текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="7c7e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c7e0-106">Parameters</span></span>

 <span data-ttu-id="7c7e0-107">_Пулфлагс_</span><span class="sxs-lookup"><span data-stu-id="7c7e0-107">_pulFlags_</span></span>
  
> <span data-ttu-id="7c7e0-108">вышли Указатель на битовую маску флагов, определяющих способ сохранения текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="7c7e0-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7c7e0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7c7e0-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c7e0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7c7e0-111">Текст сообщения сохраняется в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="7c7e0-112">Если флаг МАПИ_УНИКОДЕ не установлен, текст сохраняется в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="7c7e0-113">_Пулформат_</span><span class="sxs-lookup"><span data-stu-id="7c7e0-113">_pulFormat_</span></span>
  
> <span data-ttu-id="7c7e0-114">вышли Указатель на битовую маску флагов, определяющих формат сохраняемого текста.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="7c7e0-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7c7e0-115">The following flags can be set:</span></span>
    
<span data-ttu-id="7c7e0-116">САВЕ_ФОРМАТ_РИЧТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="7c7e0-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="7c7e0-117">Текст сообщения должен быть сохранен в виде форматированного текста в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="7c7e0-118">САВЕ_ФОРМАТ_ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="7c7e0-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="7c7e0-119">Текст сообщения должен быть сохранен в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="7c7e0-120">_ппстм_</span><span class="sxs-lookup"><span data-stu-id="7c7e0-120">_ppstm_</span></span>
  
> <span data-ttu-id="7c7e0-121">вышли Указатель на указатель на поток, который будет содержать сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c7e0-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c7e0-122">Return value</span></span>

<span data-ttu-id="7c7e0-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c7e0-123">S_OK</span></span> 
  
> <span data-ttu-id="7c7e0-124">Поток успешно получен.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c7e0-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="7c7e0-125">Remarks</span></span>

<span data-ttu-id="7c7e0-126">Объекты формы вызывают метод **имапивиевконтекст:: жетсавестреам** для получения потока объект, который реализует интерфейс **IStream** для поддержки обработки команды "Сохранить как" в средстве просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="7c7e0-127">Метод [имапиформ::D оверб](imapiform-doverb.md) , который реализован на сервере формы и вызывается средством просмотра форм для вызова команды, не должен возвращать сообщение, пока сообщение не будет полностью преобразовано в соответствующий текстовый формат и помещается в соответствующий поток.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7c7e0-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7c7e0-128">Notes to callers</span></span>

<span data-ttu-id="7c7e0-129">Не записываете в поток, на который указывает _ппстм_ , перед вызовом **жетсавестреам**.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="7c7e0-130">Когда возвращается **жетсавестреам** , не сбрасывать положение указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="7c7e0-131">Этот указатель должен находиться в конце сохраненного текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="7c7e0-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c7e0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="7c7e0-132">See also</span></span>



[<span data-ttu-id="7c7e0-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c7e0-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

