---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428188"
---
# <a name="dismissmodeless"></a><span data-ttu-id="d2d19-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="d2d19-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="d2d19-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2d19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2d19-105">Определяет функцию вызова, вызываемую MAPI при отклонении диалогового окна без режима адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d2d19-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2d19-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d2d19-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2d19-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2d19-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d2d19-108">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="d2d19-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="d2d19-109">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="d2d19-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="d2d19-110">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="d2d19-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="d2d19-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2d19-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="d2d19-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d2d19-112">Parameters</span></span>

 <span data-ttu-id="d2d19-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d2d19-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="d2d19-114">[in] Значение, определенное для реализации, обычно используется для передачи сведений об пользовательском интерфейсе в функцию.</span><span class="sxs-lookup"><span data-stu-id="d2d19-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="d2d19-115">Например, в Microsoft Windows этот параметр является родительской ручкой окна для диалогового окна и имеет тип HWND, отбрасыв в **ULONG_PTR.**</span><span class="sxs-lookup"><span data-stu-id="d2d19-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="d2d19-116">Значение нуля указывает на отсутствие родительского окна.</span><span class="sxs-lookup"><span data-stu-id="d2d19-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="d2d19-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="d2d19-117">_lpvContext_</span></span>
  
> <span data-ttu-id="d2d19-118">[in] Указатель на произвольное значение, переданного функции вызова при вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="d2d19-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="d2d19-119">Это значение может представлять адрес значения для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="d2d19-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="d2d19-120">Как правило, для кода C++  _lpvContext_ является указателем на адрес экземпляра объекта C++.</span><span class="sxs-lookup"><span data-stu-id="d2d19-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d2d19-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2d19-121">Return value</span></span>

<span data-ttu-id="d2d19-122">Нет</span><span class="sxs-lookup"><span data-stu-id="d2d19-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2d19-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2d19-123">Remarks</span></span>

<span data-ttu-id="d2d19-124">Когда клиентская заявка вызывает диалоговое окно без режима адресной книги, оно включает в цикл Windows сообщения вызов функции на основе прототипа [ACCELERATEABSDI,](accelerateabsdi.md) который проверяет и обрабатывает клавиши акселератора.</span><span class="sxs-lookup"><span data-stu-id="d2d19-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="d2d19-125">Когда диалоговое окно закрыто, MAPI вызывает основанную **на DISMISSMODELESS** функцию, чтобы клиентские приложения перестали вызывать функцию **ACCELERATEABSDI.**</span><span class="sxs-lookup"><span data-stu-id="d2d19-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2d19-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d2d19-126">See also</span></span>



[<span data-ttu-id="d2d19-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="d2d19-127">ADRPARM</span></span>](adrparm.md)

