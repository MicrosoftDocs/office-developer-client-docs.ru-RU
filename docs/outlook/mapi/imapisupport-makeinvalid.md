---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 595d5fdba28634b038838921102d3125135452a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809128"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="cb49b-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="cb49b-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="cb49b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb49b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb49b-105">Помечает объект недоступным.</span><span class="sxs-lookup"><span data-stu-id="cb49b-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="cb49b-106">���������</span><span class="sxs-lookup"><span data-stu-id="cb49b-106">Parameters</span></span>

 <span data-ttu-id="cb49b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cb49b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cb49b-108">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cb49b-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cb49b-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="cb49b-109">_lpObject_</span></span>
  
> <span data-ttu-id="cb49b-110">[in] Указатель на объект становятся недействительными.</span><span class="sxs-lookup"><span data-stu-id="cb49b-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="cb49b-111">Интерфейс объекта должен быть производным от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cb49b-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="cb49b-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="cb49b-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="cb49b-113">[in] Объект присутствует счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="cb49b-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="cb49b-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="cb49b-114">_cMethods_</span></span>
  
> <span data-ttu-id="cb49b-115">[in] Число методов в vtable объекта.</span><span class="sxs-lookup"><span data-stu-id="cb49b-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cb49b-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cb49b-116">Return value</span></span>

<span data-ttu-id="cb49b-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="cb49b-117">S_OK</span></span> 
  
> <span data-ttu-id="cb49b-118">Успешно помечено как могут использовать объект.</span><span class="sxs-lookup"><span data-stu-id="cb49b-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb49b-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb49b-119">Remarks</span></span>

<span data-ttu-id="cb49b-120">Метод **IMAPISupport::MakeInvalid** применяется для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="cb49b-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="cb49b-121">Объект становятся недействительными должен быть производным от **IUnknown** интерфейс или из интерфейса, производным от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cb49b-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="cb49b-122">**MakeInvalid** помечает объект недоступным, заменив vtable объекта vtable заглушка следующего размера, выполнение методов **IUnknown::AddRef** и **функции IUnknown::Release** , как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="cb49b-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="cb49b-123">Тем не менее другие методы не удается, возврат значения MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="cb49b-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cb49b-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cb49b-124">Notes to callers</span></span>

<span data-ttu-id="cb49b-125">Поставщики службы и службы сообщений обычно вызов **MakeInvalid** во время завершения работы.</span><span class="sxs-lookup"><span data-stu-id="cb49b-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="cb49b-126">Тем не менее **MakeInvalid** может быть вызван в любое время.</span><span class="sxs-lookup"><span data-stu-id="cb49b-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="cb49b-127">К примеру клиент освобождает объект без освобождения некоторые из ее вложенных объектов, можно вызвать **MakeInvalid** непосредственно к выпуску этих вложенных.</span><span class="sxs-lookup"><span data-stu-id="cb49b-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="cb49b-128">Необходимо быть владельцем объекта, который предпринимается попытка объявить недействительным.</span><span class="sxs-lookup"><span data-stu-id="cb49b-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="cb49b-129">Он должен быть менее 16 байт и иметь по крайней мере три метода в его vtable.</span><span class="sxs-lookup"><span data-stu-id="cb49b-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="cb49b-130">Можно вызвать **MakeInvalid** и затем выполнить любые действия, завершение работы, такие как пропуск структур данных, связанного, которая обычно выполняется во время выпуска объекта.</span><span class="sxs-lookup"><span data-stu-id="cb49b-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="cb49b-131">Код для поддержки объекта не требуется их хранения в памяти, так как MAPI освобождает память, вызвав [MAPIFreeBuffer](mapifreebuffer.md) , а затем освобождает объект.</span><span class="sxs-lookup"><span data-stu-id="cb49b-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="cb49b-132">Можно освободить ресурсы, вызвать **MakeInvalid**и игнорировать недействительным объекта.</span><span class="sxs-lookup"><span data-stu-id="cb49b-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cb49b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="cb49b-133">See also</span></span>



[<span data-ttu-id="cb49b-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="cb49b-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="cb49b-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb49b-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

