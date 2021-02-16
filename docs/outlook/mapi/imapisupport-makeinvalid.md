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
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="25a84-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="25a84-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="25a84-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25a84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25a84-105">Пометка объекта как непригодного для 2013 г.</span><span class="sxs-lookup"><span data-stu-id="25a84-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="25a84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25a84-106">Parameters</span></span>

 <span data-ttu-id="25a84-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="25a84-107">_ulFlags_</span></span>
  
> <span data-ttu-id="25a84-108">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="25a84-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="25a84-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="25a84-109">_lpObject_</span></span>
  
> <span data-ttu-id="25a84-110">[in] Указатель на объект, который необходимо сделать недействительным.</span><span class="sxs-lookup"><span data-stu-id="25a84-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="25a84-111">Интерфейс объекта должен быть производным от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="25a84-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="25a84-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="25a84-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="25a84-113">[in] Настоящее количество ссылок объекта.</span><span class="sxs-lookup"><span data-stu-id="25a84-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="25a84-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="25a84-114">_cMethods_</span></span>
  
> <span data-ttu-id="25a84-115">[in] Количество методов в vtable объекта.</span><span class="sxs-lookup"><span data-stu-id="25a84-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25a84-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25a84-116">Return value</span></span>

<span data-ttu-id="25a84-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="25a84-117">S_OK</span></span> 
  
> <span data-ttu-id="25a84-118">Объект успешно помечен как непригодный для 2013.</span><span class="sxs-lookup"><span data-stu-id="25a84-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25a84-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="25a84-119">Remarks</span></span>

<span data-ttu-id="25a84-120">Метод **IMAPISupport::MakeInvalid** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="25a84-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="25a84-121">Недопустимый объект должен быть производным от интерфейса **IUnknown** или интерфейса, производного от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="25a84-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="25a84-122">**MakeInvalid** пометит объект как непригодный для работы, заменив его vtable на загую vtable аналогичного размера, в котором методы **IUnknown::AddRef** и **IUnknown::Release** выполняются ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="25a84-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="25a84-123">Однако любые другие методы не удастся, возвращая значение MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="25a84-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="25a84-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="25a84-124">Notes to callers</span></span>

<span data-ttu-id="25a84-125">Поставщики услуг и службы сообщений обычно **звонят на makeInvalid** во время завершения работы.</span><span class="sxs-lookup"><span data-stu-id="25a84-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="25a84-126">Однако **MakeInvalid** может быть вызван в любое время.</span><span class="sxs-lookup"><span data-stu-id="25a84-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="25a84-127">Например, если клиент отпускает объект, не отпуская некоторые его подобекты, можно вызвать **MakeInvalid** немедленно, чтобы освободить эти подпроекты.</span><span class="sxs-lookup"><span data-stu-id="25a84-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="25a84-128">Необходимо владеть объектом, который вы попытались сделать недействительным.</span><span class="sxs-lookup"><span data-stu-id="25a84-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="25a84-129">Он должен иметь длину не менее 16 т и иметь по крайней мере три метода в своей вести.</span><span class="sxs-lookup"><span data-stu-id="25a84-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="25a84-130">Можно вызвать **MakeInvalid,** а затем выполнить любые работы по отключению, такие как удаление связанных структур данных, которые обычно выполняются во время выпуска объекта.</span><span class="sxs-lookup"><span data-stu-id="25a84-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="25a84-131">Код для поддержки объекта не должен храниться в памяти, так как MAPI освобождает память, вызывая [MAPIFreeBuffer,](mapifreebuffer.md) а затем освобождает объект.</span><span class="sxs-lookup"><span data-stu-id="25a84-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="25a84-132">Вы можете освободить ресурсы, вызвать **MakeInvalid,** а затем игнорировать недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="25a84-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25a84-133">См. также</span><span class="sxs-lookup"><span data-stu-id="25a84-133">See also</span></span>



[<span data-ttu-id="25a84-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="25a84-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="25a84-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="25a84-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

