---
title: имапиконтролжетстате
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
# <a name="imapicontrolgetstate"></a><span data-ttu-id="f7abb-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="f7abb-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="f7abb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7abb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7abb-105">Получает значение, которое указывает, включен ли элемент управления "Кнопка" или отключен.</span><span class="sxs-lookup"><span data-stu-id="f7abb-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="f7abb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7abb-106">Parameters</span></span>

 <span data-ttu-id="f7abb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7abb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f7abb-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="f7abb-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f7abb-109">_лпулстате_</span><span class="sxs-lookup"><span data-stu-id="f7abb-109">_lpulState_</span></span>
  
> <span data-ttu-id="f7abb-110">вышли Указатель на значение, указывающее состояние элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="f7abb-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="f7abb-111">Можно возвратить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f7abb-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="f7abb-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="f7abb-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="f7abb-113">Элемент управления "Кнопка" отключен и не может быть выбран.</span><span class="sxs-lookup"><span data-stu-id="f7abb-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="f7abb-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="f7abb-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="f7abb-115">Элемент управления Button включен и может быть выбран.</span><span class="sxs-lookup"><span data-stu-id="f7abb-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7abb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7abb-116">Return value</span></span>

<span data-ttu-id="f7abb-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7abb-117">S_OK</span></span> 
  
> <span data-ttu-id="f7abb-118">Состояние элемента управления "Кнопка" успешно извлечено.</span><span class="sxs-lookup"><span data-stu-id="f7abb-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7abb-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7abb-119">Remarks</span></span>

<span data-ttu-id="f7abb-120">Поставщики услуг реализуют метод **имапиконтрол::** , который обеспечивает MAPI с состоянием элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="f7abb-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="f7abb-121">Если кнопка включена, она может реагировать на нажатие кнопки мыши или нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="f7abb-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="f7abb-122">Если эта кнопка отключена, кнопка отображается серым цветом и не реагирует на щелчок мышью или нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="f7abb-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="f7abb-123">Дополнительные сведения о **том, как реализовать метод** GetObject и другие методы [имапиконтрол: IUnknown](imapicontroliunknown.md) , можно найти в разделе [Реализация объекта Control](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f7abb-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7abb-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f7abb-124">See also</span></span>



[<span data-ttu-id="f7abb-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="f7abb-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="f7abb-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7abb-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

