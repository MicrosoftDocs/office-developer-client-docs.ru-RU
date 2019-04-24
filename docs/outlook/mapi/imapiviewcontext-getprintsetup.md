---
title: Имапивиевконтекстжетпринтсетуп
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351127"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="92691-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="92691-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="92691-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92691-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92691-105">Получает текущие сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="92691-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="92691-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92691-106">Parameters</span></span>

 <span data-ttu-id="92691-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="92691-107">_ulFlags_</span></span>
  
> <span data-ttu-id="92691-108">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="92691-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="92691-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="92691-109">The following flag can be set:</span></span>
    
<span data-ttu-id="92691-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92691-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="92691-111">Возвращаемые строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="92691-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="92691-112">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="92691-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="92691-113">_Лппформпринтсетуп_</span><span class="sxs-lookup"><span data-stu-id="92691-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="92691-114">вышли Указатель на структуру, в которой хранятся сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="92691-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="92691-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92691-115">Return value</span></span>

<span data-ttu-id="92691-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="92691-116">S_OK</span></span> 
  
> <span data-ttu-id="92691-117">Сведения о печати успешно получены.</span><span class="sxs-lookup"><span data-stu-id="92691-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92691-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="92691-118">Remarks</span></span>

<span data-ttu-id="92691-119">Объекты формы вызывают метод **имапивиевконтекст:: жетпринтсетуп** для получения сведений о настройках принтера, прежде чем пытаться напечатать текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="92691-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="92691-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="92691-120">Notes to implementers</span></span>

<span data-ttu-id="92691-121">ВыДеляйте элементы **хдевмоде** и **хдевнаме** структуры [Формпринтсетуп](formprintsetup.md) с помощью функции Win32 **глобалаллок**.</span><span class="sxs-lookup"><span data-stu-id="92691-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="92691-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="92691-122">Notes to callers</span></span>

<span data-ttu-id="92691-123">Если ожидается, что элементы **хдевмоде** и **хдевнаме** структуры **формпринтсетуп** , на которые указывает параметр _лппформпринтсетуп_ , являются строками в Юникоде, установите _ulFlags_ в мапи_уникоде.</span><span class="sxs-lookup"><span data-stu-id="92691-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="92691-124">В противном случае **жетпринтсетуп** будет возвращать эти строки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="92691-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="92691-125">Освободите члены **хдевмоде** и **хдевнаме** структуры **Формпринтсетуп** , вызвав функцию Win32 **глобалфри**.</span><span class="sxs-lookup"><span data-stu-id="92691-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="92691-126">Освободите всю структуру **формпринтсетуп** , вызвав [мапифрибуффер](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="92691-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92691-127">См. также</span><span class="sxs-lookup"><span data-stu-id="92691-127">See also</span></span>



[<span data-ttu-id="92691-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="92691-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="92691-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92691-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

