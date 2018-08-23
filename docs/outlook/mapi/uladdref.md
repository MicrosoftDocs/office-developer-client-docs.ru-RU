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
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592375"
---
# <a name="uladdref"></a><span data-ttu-id="9cb48-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="9cb48-103">UlAddRef</span></span>

  
  
<span data-ttu-id="9cb48-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cb48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cb48-105">Предоставляет альтернативный способ для вызова метода OLE **IUnknown::AddRef**.</span><span class="sxs-lookup"><span data-stu-id="9cb48-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cb48-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9cb48-106">Header file:</span></span>  <br/> |<span data-ttu-id="9cb48-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cb48-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9cb48-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="9cb48-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9cb48-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9cb48-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9cb48-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="9cb48-110">Called by:</span></span>  <br/> |<span data-ttu-id="9cb48-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="9cb48-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="9cb48-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cb48-112">Parameters</span></span>

 <span data-ttu-id="9cb48-113">_панк_</span><span class="sxs-lookup"><span data-stu-id="9cb48-113">_punk_</span></span>
  
> <span data-ttu-id="9cb48-114">[in] Указатель на интерфейс на основе интерфейс **IUnknown** другими словами любого интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="9cb48-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9cb48-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9cb48-115">Return value</span></span>

<span data-ttu-id="9cb48-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9cb48-116">S_OK</span></span> 
  
> <span data-ttu-id="9cb48-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9cb48-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="9cb48-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="9cb48-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="9cb48-119">Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="9cb48-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9cb48-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="9cb48-120">Remarks</span></span>

 <span data-ttu-id="9cb48-121">**UlAddRef** возвращает значение, возвращаемое методом **IUnknown::AddRef** , который является новое значение счетчика ссылок для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9cb48-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="9cb48-122">Значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9cb48-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="9cb48-123">Дополнительные сведения о **IUnknown::AddRef**см [Интерфейс IUnknown](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="9cb48-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

