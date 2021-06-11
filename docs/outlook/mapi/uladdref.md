---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432837"
---
# <a name="uladdref"></a><span data-ttu-id="d5a2b-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="d5a2b-103">UlAddRef</span></span>

  
  
<span data-ttu-id="d5a2b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5a2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5a2b-105">Предоставляет альтернативный способ вызвать метод OLE **IUnknown::AddRef**.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5a2b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d5a2b-106">Header file:</span></span>  <br/> |<span data-ttu-id="d5a2b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5a2b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d5a2b-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d5a2b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d5a2b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d5a2b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d5a2b-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d5a2b-110">Called by:</span></span>  <br/> |<span data-ttu-id="d5a2b-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d5a2b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="d5a2b-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5a2b-112">Parameters</span></span>

 <span data-ttu-id="d5a2b-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="d5a2b-113">_punk_</span></span>
  
> <span data-ttu-id="d5a2b-114">[in] Указатель на интерфейс, полученный из **интерфейса IUnknown,** другими словами, любого интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d5a2b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5a2b-115">Return value</span></span>

<span data-ttu-id="d5a2b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5a2b-116">S_OK</span></span> 
  
> <span data-ttu-id="d5a2b-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d5a2b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="d5a2b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="d5a2b-119">Ошибка неожиданного или неизвестного происхождения не позволяет завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5a2b-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="d5a2b-120">Remarks</span></span>

 <span data-ttu-id="d5a2b-121">**UlAddRef** возвращает значение, возвращенное методом **IUnknown::AddRef,** которое является новым значением отсчета ссылок для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="d5a2b-122">Значение незеро.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="d5a2b-123">Дополнительные сведения об **интерфейсе IUnknown::AddRef** см. в [нем.](implementing-the-iunknown-interface.md)</span><span class="sxs-lookup"><span data-stu-id="d5a2b-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

