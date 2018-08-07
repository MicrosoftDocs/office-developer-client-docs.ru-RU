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
ms.openlocfilehash: dc830665f425b747d2fdb05641dc037a2e84f695
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808318"
---
# <a name="dismissmodeless"></a><span data-ttu-id="4da6a-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="4da6a-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="4da6a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4da6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4da6a-105">Определяет функцию обратного вызова, которая вызывает MAPI, когда он может закрыть диалоговое окно безрежимным адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4da6a-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4da6a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4da6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4da6a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4da6a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4da6a-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="4da6a-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4da6a-109">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="4da6a-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="4da6a-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="4da6a-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4da6a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4da6a-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="4da6a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4da6a-112">Parameters</span></span>

 <span data-ttu-id="4da6a-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4da6a-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="4da6a-114">[in] От реализации значение, обычно используется для передачи в функцию сведения о пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="4da6a-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="4da6a-115">Например в Microsoft Windows этот параметр является дескриптор родительского окна для диалогового окна и имеет тип HWND, привести к **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="4da6a-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="4da6a-116">Нулевое значение указывает, что нет родительского окна.</span><span class="sxs-lookup"><span data-stu-id="4da6a-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="4da6a-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="4da6a-117">_lpvContext_</span></span>
  
> <span data-ttu-id="4da6a-118">[in] Указатель произвольных значение передается функции обратного вызова, когда она вызывается средствами MAPI.</span><span class="sxs-lookup"><span data-stu-id="4da6a-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="4da6a-119">Это значение может представлять адрес важности для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="4da6a-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="4da6a-120">Обычно для кода C++ _lpvContext_ — это указатель на адрес экземпляр объекта C++.</span><span class="sxs-lookup"><span data-stu-id="4da6a-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4da6a-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4da6a-121">Return value</span></span>

<span data-ttu-id="4da6a-122">Нет</span><span class="sxs-lookup"><span data-stu-id="4da6a-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4da6a-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="4da6a-123">Remarks</span></span>

<span data-ttu-id="4da6a-124">Когда клиентское приложение вызывает диалоговое окно безрежимным адресной книги, он содержит в цикл сообщений Windows вызов функции, основанной на прототип [ACCELERATEABSDI](accelerateabsdi.md) , которая проверяет и обрабатывает сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="4da6a-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="4da6a-125">При закрытии диалоговое окно вызовов MAPI с **DISMISSMODELESS** на основе функции, чтобы клиентское приложение остановит вызов **ACCELERATEABSDI** на основе функции.</span><span class="sxs-lookup"><span data-stu-id="4da6a-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4da6a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="4da6a-126">See also</span></span>



[<span data-ttu-id="4da6a-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="4da6a-127">ADRPARM</span></span>](adrparm.md)

