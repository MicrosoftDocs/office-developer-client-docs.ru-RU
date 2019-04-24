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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339776"
---
# <a name="dismissmodeless"></a><span data-ttu-id="38521-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="38521-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="38521-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38521-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38521-105">Определяет функцию обратного вызова, которая вызывает MAPI при закрытии диалогового окна с немодальной адресной книгой.</span><span class="sxs-lookup"><span data-stu-id="38521-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38521-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="38521-106">Header file:</span></span>  <br/> |<span data-ttu-id="38521-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="38521-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="38521-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="38521-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="38521-109">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="38521-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="38521-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="38521-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="38521-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="38521-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="38521-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="38521-112">Parameters</span></span>

 <span data-ttu-id="38521-113">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="38521-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="38521-114">возврата Зависящее от реализации значение, которое обычно используется для передачи сведений о пользовательском интерфейсе в функцию.</span><span class="sxs-lookup"><span data-stu-id="38521-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="38521-115">Например, в Microsoft Windows этот параметр является дескриптором родительского окна для диалогового окна и относится к типу HWND, приведенному к **улонг_птр**.</span><span class="sxs-lookup"><span data-stu-id="38521-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="38521-116">Нулевое значение указывает, что родительское окно отсутствует.</span><span class="sxs-lookup"><span data-stu-id="38521-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="38521-117">_Лпвконтекст_</span><span class="sxs-lookup"><span data-stu-id="38521-117">_lpvContext_</span></span>
  
> <span data-ttu-id="38521-118">возврата Указатель на произвольное значение, переданное функции обратного вызова при ее вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="38521-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="38521-119">Это значение может представлять собой адрес, значимый клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="38521-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="38521-120">Как правило, для кода C++ _лпвконтекст_ является указателем на адрес экземпляра объекта c++.</span><span class="sxs-lookup"><span data-stu-id="38521-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38521-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38521-121">Return value</span></span>

<span data-ttu-id="38521-122">Нет</span><span class="sxs-lookup"><span data-stu-id="38521-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38521-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38521-123">Remarks</span></span>

<span data-ttu-id="38521-124">Когда клиентское приложение вызывает немодальное диалоговое окно адресной книги, оно включает в себя цикл обработки сообщений Windows, который вызывает функцию на основе прототипа [акцелератеабсди](accelerateabsdi.md) , который проверяет и обрабатывает сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="38521-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="38521-125">Когда диалоговое окно закрывается, MAPI вызывает функцию на основе **дисмиссмоделесс** , чтобы клиентское приложение не вызывало вызов функции на основе **акцелератеабсди** .</span><span class="sxs-lookup"><span data-stu-id="38521-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38521-126">См. также</span><span class="sxs-lookup"><span data-stu-id="38521-126">See also</span></span>



[<span data-ttu-id="38521-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="38521-127">ADRPARM</span></span>](adrparm.md)

