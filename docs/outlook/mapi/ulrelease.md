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
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415847"
---
# <a name="ulrelease"></a><span data-ttu-id="5b343-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="5b343-103">UlRelease</span></span>

  
  
<span data-ttu-id="5b343-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b343-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b343-105">Предоставляет альтернативный способ вызова метода OLE **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="5b343-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b343-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5b343-106">Header file:</span></span>  <br/> |<span data-ttu-id="5b343-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b343-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5b343-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5b343-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5b343-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5b343-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5b343-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5b343-110">Called by:</span></span>  <br/> |<span data-ttu-id="5b343-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="5b343-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="5b343-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b343-112">Parameters</span></span>

 <span data-ttu-id="5b343-113">_1_</span><span class="sxs-lookup"><span data-stu-id="5b343-113">_punk_</span></span>
  
> <span data-ttu-id="5b343-114">[in] Указатель на интерфейс, производный от **интерфейса IUnknown,** другими словами, любой интерфейс MAPI.</span><span class="sxs-lookup"><span data-stu-id="5b343-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5b343-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b343-115">Return value</span></span>

<span data-ttu-id="5b343-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b343-116">S_OK</span></span> 
  
> <span data-ttu-id="5b343-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5b343-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="5b343-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="5b343-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="5b343-119">Ошибка непредвиденного или неизвестного источника помешала выполнению операции.</span><span class="sxs-lookup"><span data-stu-id="5b343-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b343-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b343-120">Remarks</span></span>

<span data-ttu-id="5b343-121">Количество ссылок — это количество существующих указателей на объект, который необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="5b343-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="5b343-122">Если  _параметром parameter_ является NULL, функция немедленно возвращается без вызова **IUnknown::Release**</span><span class="sxs-lookup"><span data-stu-id="5b343-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="5b343-123">**UlRelease** возвращает значение, возвращенное методом **IUnknown::Release,** которое может быть равно отсчету для объекта, который необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="5b343-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="5b343-124">Дополнительные сведения о **IUnknown::Release** см. в реализации [интерфейса IUnknown.](implementing-the-iunknown-interface.md)</span><span class="sxs-lookup"><span data-stu-id="5b343-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

