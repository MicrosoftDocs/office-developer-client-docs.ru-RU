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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808828"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="969a5-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="969a5-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="969a5-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="969a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="969a5-105">Получает значение, указывающее, включено ли элемент управления button.</span><span class="sxs-lookup"><span data-stu-id="969a5-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="969a5-106">���������</span><span class="sxs-lookup"><span data-stu-id="969a5-106">Parameters</span></span>

 <span data-ttu-id="969a5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="969a5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="969a5-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="969a5-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="969a5-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="969a5-109">_lpulState_</span></span>
  
> <span data-ttu-id="969a5-110">[out] Указатель на значение, указывающее состояние элемента управления кнопка.</span><span class="sxs-lookup"><span data-stu-id="969a5-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="969a5-111">Можно получить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="969a5-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="969a5-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="969a5-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="969a5-113">Элемент управления button отключена и не может быть выбрана.</span><span class="sxs-lookup"><span data-stu-id="969a5-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="969a5-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="969a5-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="969a5-115">Элемент управления button включено, можно щелкнуть.</span><span class="sxs-lookup"><span data-stu-id="969a5-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="969a5-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="969a5-116">Return value</span></span>

<span data-ttu-id="969a5-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="969a5-117">S_OK</span></span> 
  
> <span data-ttu-id="969a5-118">Состояние элемента управления кнопка был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="969a5-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="969a5-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="969a5-119">Remarks</span></span>

<span data-ttu-id="969a5-120">Поставщики услуг реализуйте метод **IMAPIControl::GetState** для предоставления MAPI с состоянием элемента управления button.</span><span class="sxs-lookup"><span data-stu-id="969a5-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="969a5-121">Кнопка может отвечать на щелчок мыши или нажатия клавиш.</span><span class="sxs-lookup"><span data-stu-id="969a5-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="969a5-122">Если они отключены, кнопка недоступна и не отвечает на щелчок мыши или нажатия клавиш.</span><span class="sxs-lookup"><span data-stu-id="969a5-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="969a5-123">Дополнительные сведения о реализации **GetState** , а другой [IMAPIControl: IUnknown](imapicontroliunknown.md) методы, видеть [Реализации объекта элемента управления](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="969a5-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="969a5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="969a5-124">See also</span></span>



[<span data-ttu-id="969a5-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="969a5-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="969a5-126">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="969a5-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

