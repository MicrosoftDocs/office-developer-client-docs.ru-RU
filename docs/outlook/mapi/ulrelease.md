---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812545"
---
# <a name="ulrelease"></a><span data-ttu-id="96d0b-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="96d0b-103">UlRelease</span></span>

  
  
<span data-ttu-id="96d0b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96d0b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96d0b-105">Предоставляет альтернативный способ для вызова метода OLE **функции IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="96d0b-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96d0b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="96d0b-106">Header file:</span></span>  <br/> |<span data-ttu-id="96d0b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96d0b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="96d0b-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="96d0b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="96d0b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="96d0b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="96d0b-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="96d0b-110">Called by:</span></span>  <br/> |<span data-ttu-id="96d0b-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="96d0b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="96d0b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="96d0b-112">Parameters</span></span>

 <span data-ttu-id="96d0b-113">_панк_</span><span class="sxs-lookup"><span data-stu-id="96d0b-113">_punk_</span></span>
  
> <span data-ttu-id="96d0b-114">[in] Указатель на интерфейс на основе интерфейс **IUnknown** другими словами любого интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="96d0b-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="96d0b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="96d0b-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="96d0b-116">S_OK</span></span> 
  
> <span data-ttu-id="96d0b-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="96d0b-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="96d0b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="96d0b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="96d0b-119">Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="96d0b-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96d0b-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="96d0b-120">Remarks</span></span>

<span data-ttu-id="96d0b-121">Счетчик — число существующие указатели на элемент, который нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="96d0b-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="96d0b-122">Если параметр _punk_ имеет значение NULL, функция возвращает сразу же без вызова **функции IUnknown::Release**</span><span class="sxs-lookup"><span data-stu-id="96d0b-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="96d0b-123">**UlRelease** возвращает значение, возвращаемое методом **функции IUnknown::Release** , который может быть равно количеству ссылку для объекта нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="96d0b-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="96d0b-124">Дополнительные сведения о **функции IUnknown::Release**см [Интерфейс IUnknown](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="96d0b-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

