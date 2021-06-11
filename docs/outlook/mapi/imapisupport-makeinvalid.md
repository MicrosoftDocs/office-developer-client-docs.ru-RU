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
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427495"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="6c9d7-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="6c9d7-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="6c9d7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c9d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c9d7-105">Пометит объект как непригодный.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="6c9d7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6c9d7-106">Parameters</span></span>

 <span data-ttu-id="6c9d7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c9d7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6c9d7-108">Зарезервировано; должно быть нулевой.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6c9d7-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="6c9d7-109">_lpObject_</span></span>
  
> <span data-ttu-id="6c9d7-110">[in] Указатель на объект, который будет признан недействительным.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="6c9d7-111">Интерфейс объекта должен быть получен из **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="6c9d7-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="6c9d7-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="6c9d7-113">[in] Настоящее количество ссылок объекта.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="6c9d7-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="6c9d7-114">_cMethods_</span></span>
  
> <span data-ttu-id="6c9d7-115">[in] Количество методов в vtable объекта.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c9d7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c9d7-116">Return value</span></span>

<span data-ttu-id="6c9d7-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c9d7-117">S_OK</span></span> 
  
> <span data-ttu-id="6c9d7-118">Объект был успешно помечен как непригодный для пользоваемых объектов.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c9d7-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c9d7-119">Remarks</span></span>

<span data-ttu-id="6c9d7-120">Метод **IMAPISupport::MakeInvalid** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="6c9d7-121">Объект, который должен быть признан недействительным, должен быть получен из **интерфейса IUnknown** или интерфейса, полученного из **IUnknown.**</span><span class="sxs-lookup"><span data-stu-id="6c9d7-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="6c9d7-122">**MakeInvalid** отмечает объект как непригодный для работы, заменив vtable объекта на загребный vtable аналогичного размера, в котором методы **IUnknown::AddRef** и **IUnknown::Release** выполняются как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="6c9d7-123">Однако любые другие методы сбой, возвращая значение MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c9d7-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6c9d7-124">Notes to callers</span></span>

<span data-ttu-id="6c9d7-125">Поставщики услуг и службы сообщений обычно звонят **в MakeInvalid** во время остановки.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="6c9d7-126">Однако **MakeInvalid** можно назвать в любое время.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="6c9d7-127">Например, если клиент выпускает объект, не выпуская некоторые из его субобектов, вы можете немедленно вызвать **MakeInvalid,** чтобы освободить эти субобпроекты.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="6c9d7-128">Вы должны владеть объектом, который вы попытаете признать недействительным.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="6c9d7-129">Она должна быть длиной не менее 16 bytes и иметь по крайней мере три метода в ее vtable.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="6c9d7-130">Можно вызвать **MakeInvalid** и выполнить любые работы по остановке, например удаление связанных структур данных, которые обычно выполняются во время выпуска объекта.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="6c9d7-131">Код для поддержки объекта не должен храниться в памяти, так как MAPI освобождает память, вызывая [MAPIFreeBuffer,](mapifreebuffer.md) а затем освобождает объект.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="6c9d7-132">Можно освободить ресурсы, вызвать **MakeInvalid,** а затем игнорировать недействительный объект.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c9d7-133">См. также</span><span class="sxs-lookup"><span data-stu-id="6c9d7-133">See also</span></span>



[<span data-ttu-id="6c9d7-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="6c9d7-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="6c9d7-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c9d7-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

