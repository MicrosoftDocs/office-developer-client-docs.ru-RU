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
# <a name="accelerateabsdi"></a><span data-ttu-id="3b8aa-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="3b8aa-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="3b8aa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b8aa-105">Определяет функцию обратного вызова для обработки сочетаний клавиш в диалоговом окне немодальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b8aa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3b8aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b8aa-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3b8aa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3b8aa-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3b8aa-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="3b8aa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8aa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3b8aa-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="3b8aa-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="3b8aa-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="3b8aa-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="3b8aa-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b8aa-112">Parameters</span></span>

 <span data-ttu-id="3b8aa-113">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="3b8aa-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="3b8aa-114">возврата Зависящее от реализации значение, используемое для передачи сведений о пользовательском интерфейсе в функцию.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="3b8aa-115">В приложениях, работающих в Microsoft Windows, _улуипарам_ является дескриптором родительского окна для диалогового окна и относится к типу HWND, приведенному к **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="3b8aa-116">Нулевое значение указывает, что родительское окно отсутствует.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="3b8aa-117">_лпвмсг_</span><span class="sxs-lookup"><span data-stu-id="3b8aa-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="3b8aa-118">возврата Указатель на сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b8aa-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b8aa-119">Return value</span></span>

<span data-ttu-id="3b8aa-120">Функция с прототипом **акцелератеабсди** возвращает значение true, если обрабатывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b8aa-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b8aa-121">Remarks</span></span>

<span data-ttu-id="3b8aa-122">Функция, основанная на прототипе **акцелератеабсди** , используется только с немодальным диалоговым окном, то есть только в том случае, если клиентское приложение установило флаг DIALOG_SDI в элементе _ulFlags_ структуры [адрпарм](adrparm.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8aa-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="3b8aa-123">Немодальное диалоговое окно использует цикл обработки сообщений Windows клиентского приложения, а не собственный цикл.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="3b8aa-124">Приложение, которое управляет циклом обработки сообщений, не знает, какие сочетания клавиш использует диалоговое окно, поэтому она вызывает функцию на основе **акцелератеабсди** для проверки и использования сочетаний клавиш, таких как CTRL + P для печати.</span><span class="sxs-lookup"><span data-stu-id="3b8aa-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="3b8aa-125">Клиентский цикл обработки сообщений вызывает функцию на основе **акцелератеабсди** , когда клиент вызывает диалоговое окно с немодальной адресной книгой с помощью метода [IAddrBook:: Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8aa-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="3b8aa-126">Этот вызов завершается, когда MAPI вызывает функцию на основе прототипа функции [дисмиссмоделесс](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8aa-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

