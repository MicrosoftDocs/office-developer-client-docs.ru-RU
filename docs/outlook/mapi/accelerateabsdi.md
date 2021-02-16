---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420376"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="16c93-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="16c93-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="16c93-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16c93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16c93-105">Определяет функцию вызова для обработки клавиш ускорителей в диалоговом окне без режима адресной книги.</span><span class="sxs-lookup"><span data-stu-id="16c93-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16c93-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="16c93-106">Header file:</span></span>  <br/> |<span data-ttu-id="16c93-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16c93-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="16c93-108">Определяемая функция, реализованная в:</span><span class="sxs-lookup"><span data-stu-id="16c93-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="16c93-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="16c93-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="16c93-110">Определяемая функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="16c93-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="16c93-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="16c93-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="16c93-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="16c93-112">Parameters</span></span>

 <span data-ttu-id="16c93-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="16c93-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="16c93-114">[in] Значение, специфичная для реализации, используемая для передачи сведений пользовательского интерфейса в функцию.</span><span class="sxs-lookup"><span data-stu-id="16c93-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="16c93-115">В приложениях, работающих в Microsoft Windows, _ulUIParam_ — это родительский окне для диалоговых окон, тип HWND, приведите к ULONG_PTR **.**</span><span class="sxs-lookup"><span data-stu-id="16c93-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="16c93-116">Нулевое значение указывает, что родительского окна нет.</span><span class="sxs-lookup"><span data-stu-id="16c93-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="16c93-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="16c93-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="16c93-118">[in] Указатель на сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="16c93-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="16c93-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16c93-119">Return value</span></span>

<span data-ttu-id="16c93-120">Функция с прототипом **ACCELERATEABSDI** возвращает true, если обрабатывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="16c93-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="16c93-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="16c93-121">Remarks</span></span>

<span data-ttu-id="16c93-122">Функция, основанная на прототипе **ACCELERATEABSDI,** используется только в диалоговом окне без режима, то есть только в том случае, если клиентские приложения установили флаг DIALOG_SDI в члене _ulFlags_ структуры [ADRPARM.](adrparm.md)</span><span class="sxs-lookup"><span data-stu-id="16c93-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="16c93-123">Диалоговое окно без режима делится циклом сообщений Windows клиентского приложения, а не собственным циклом.</span><span class="sxs-lookup"><span data-stu-id="16c93-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="16c93-124">Приложение, которое управляет циклом сообщений, не знает, какие клавиши ускорителя использует диалоговое окно, поэтому оно вызывает функцию на основе **ACCELERATEABSDI** для проверки и работы с ускорителями, такими как CTRL+P для печати.</span><span class="sxs-lookup"><span data-stu-id="16c93-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="16c93-125">Цикл сообщений клиента вызывает функцию на основе **ACCELERATEABSDI,** когда клиент вызывает диалоговое окно без режима адресной книги с методом [IAddrBook::Address.](iaddrbook-address.md)</span><span class="sxs-lookup"><span data-stu-id="16c93-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="16c93-126">Этот вызов завершается, когда MAPI вызывает функцию на основе прототипа [функции DISMISSMODELESS.](dismissmodeless.md)</span><span class="sxs-lookup"><span data-stu-id="16c93-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

