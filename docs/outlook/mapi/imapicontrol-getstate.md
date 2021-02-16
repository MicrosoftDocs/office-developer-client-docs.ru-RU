---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419011"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="88a58-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="88a58-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="88a58-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88a58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88a58-105">Извлекает значение, которое указывает, включен или отключен контроль кнопок.</span><span class="sxs-lookup"><span data-stu-id="88a58-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="88a58-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88a58-106">Parameters</span></span>

 <span data-ttu-id="88a58-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="88a58-107">_ulFlags_</span></span>
  
> <span data-ttu-id="88a58-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="88a58-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="88a58-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="88a58-109">_lpulState_</span></span>
  
> <span data-ttu-id="88a58-110">[out] Указатель на значение, которое указывает состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="88a58-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="88a58-111">Может быть возвращено одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="88a58-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="88a58-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="88a58-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="88a58-113">Кнопка отключена и не может быть нажата.</span><span class="sxs-lookup"><span data-stu-id="88a58-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="88a58-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="88a58-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="88a58-115">Кнопка управления включена и может быть нажата.</span><span class="sxs-lookup"><span data-stu-id="88a58-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="88a58-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88a58-116">Return value</span></span>

<span data-ttu-id="88a58-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="88a58-117">S_OK</span></span> 
  
> <span data-ttu-id="88a58-118">Состояние кнопки управления было успешно извлечено.</span><span class="sxs-lookup"><span data-stu-id="88a58-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88a58-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="88a58-119">Remarks</span></span>

<span data-ttu-id="88a58-120">Поставщики услуг реализуют метод **IMAPIControl::GetState,** чтобы предоставить MAPI состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="88a58-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="88a58-121">Если кнопка включена, она может реагировать на нажатие мыши или нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="88a58-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="88a58-122">Если она отключена, кнопка отображается затемнено и не реагирует на нажатие мыши или нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="88a58-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="88a58-123">Дополнительные сведения о реализации **GetState** и других методов [IMAPIControl : IUnknown](imapicontroliunknown.md) см. в реализации [объекта control.](control-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="88a58-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="88a58-124">См. также</span><span class="sxs-lookup"><span data-stu-id="88a58-124">See also</span></span>



[<span data-ttu-id="88a58-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="88a58-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="88a58-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="88a58-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

