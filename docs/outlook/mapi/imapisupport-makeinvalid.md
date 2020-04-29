---
title: имаписуппортмакеинвалид
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
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="9e52b-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="9e52b-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="9e52b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e52b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e52b-105">Помечает объект как непригодный к использованию.</span><span class="sxs-lookup"><span data-stu-id="9e52b-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="9e52b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e52b-106">Parameters</span></span>

 <span data-ttu-id="9e52b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e52b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9e52b-108">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9e52b-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9e52b-109">_лпобжект_</span><span class="sxs-lookup"><span data-stu-id="9e52b-109">_lpObject_</span></span>
  
> <span data-ttu-id="9e52b-110">возврата Указатель на объект, который необходимо сделать недействительным.</span><span class="sxs-lookup"><span data-stu-id="9e52b-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="9e52b-111">Интерфейс объекта должен быть производным от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9e52b-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="9e52b-112">_улрефкаунт_</span><span class="sxs-lookup"><span data-stu-id="9e52b-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="9e52b-113">возврата Текущее значение счетчика ссылок объекта.</span><span class="sxs-lookup"><span data-stu-id="9e52b-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="9e52b-114">_кмесодс_</span><span class="sxs-lookup"><span data-stu-id="9e52b-114">_cMethods_</span></span>
  
> <span data-ttu-id="9e52b-115">возврата Количество методов в таблице vtable объекта.</span><span class="sxs-lookup"><span data-stu-id="9e52b-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e52b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e52b-116">Return value</span></span>

<span data-ttu-id="9e52b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e52b-117">S_OK</span></span> 
  
> <span data-ttu-id="9e52b-118">Объект успешно помечен как непригодный для использования.</span><span class="sxs-lookup"><span data-stu-id="9e52b-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e52b-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e52b-119">Remarks</span></span>

<span data-ttu-id="9e52b-120">Метод **имаписуппорт:: макеинвалид** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="9e52b-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="9e52b-121">Объект, который необходимо сделать недействительным, должен быть производным от интерфейса **IUnknown** или от интерфейса, производного от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9e52b-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="9e52b-122">**Макеинвалид** помечает объект как непригодный для использования с помощью замены виртуальной таблицы vtable аналогичного размера, в котором методы **IUnknown:: AddRef** и **IUnknown:: Release** выполняются должным образом.</span><span class="sxs-lookup"><span data-stu-id="9e52b-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="9e52b-123">Однако при этом не удается выполнить все другие методы, возвращая значение MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="9e52b-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9e52b-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9e52b-124">Notes to callers</span></span>

<span data-ttu-id="9e52b-125">Поставщики услуг и службы сообщений обычно вызывают **макеинвалид** во время завершения работы.</span><span class="sxs-lookup"><span data-stu-id="9e52b-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="9e52b-126">Однако **макеинвалид** можно вызвать в любое время.</span><span class="sxs-lookup"><span data-stu-id="9e52b-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="9e52b-127">Например, если клиент освобождает объект, не освобождая некоторые из его подобъектов, вы можете вызвать **макеинвалид** немедленно, чтобы освободить эти подобъекты.</span><span class="sxs-lookup"><span data-stu-id="9e52b-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="9e52b-128">Необходимо быть владельцем объекта, который вы пытались сделать недействительным.</span><span class="sxs-lookup"><span data-stu-id="9e52b-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="9e52b-129">Он должен иметь по крайней мере 16 байт и иметь по крайней мере три метода в виртуальной таблице vtable.</span><span class="sxs-lookup"><span data-stu-id="9e52b-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="9e52b-130">Вы можете вызвать **макеинвалид** и затем выполнить какие-либо действия по завершению работы, например отменять связанные структуры данных, которые обычно выполняются во время выпуска объекта.</span><span class="sxs-lookup"><span data-stu-id="9e52b-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="9e52b-131">Код для поддержки объекта не должен храниться в памяти, так как MAPI освобождает память, вызывая [мапифрибуффер](mapifreebuffer.md) , а затем освобождает объект.</span><span class="sxs-lookup"><span data-stu-id="9e52b-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="9e52b-132">Вы можете освободить ресурсы, вызвать **макеинвалид**, а затем проигнорировать недействительный объект.</span><span class="sxs-lookup"><span data-stu-id="9e52b-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e52b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="9e52b-133">See also</span></span>



[<span data-ttu-id="9e52b-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9e52b-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9e52b-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e52b-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

