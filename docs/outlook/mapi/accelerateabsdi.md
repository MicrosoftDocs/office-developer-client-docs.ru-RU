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
ms.openlocfilehash: 101e74f3e35e3664dd29e59f166b2f0af6e1dcba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592040"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="edc63-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="edc63-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="edc63-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edc63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edc63-105">Определяет функцию обратного вызова для процесса сочетания клавиш в диалоговом окне безрежимным адресная книга.</span><span class="sxs-lookup"><span data-stu-id="edc63-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edc63-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="edc63-106">Header file:</span></span>  <br/> |<span data-ttu-id="edc63-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edc63-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="edc63-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="edc63-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="edc63-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="edc63-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="edc63-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="edc63-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="edc63-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="edc63-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="edc63-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="edc63-112">Parameters</span></span>

 <span data-ttu-id="edc63-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="edc63-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="edc63-114">[in] От реализации значение, используемое для передачи сведения о пользовательском интерфейсе функции.</span><span class="sxs-lookup"><span data-stu-id="edc63-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="edc63-115">В приложениях, использующих на Microsoft Windows _ulUIParam_ является дескриптор родительского окна для диалогового окна и типа HWND, привести к **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="edc63-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="edc63-116">Нулевое значение указывает, что нет родительского окна.</span><span class="sxs-lookup"><span data-stu-id="edc63-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="edc63-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="edc63-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="edc63-118">[in] Указатель на сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="edc63-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edc63-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="edc63-119">Return value</span></span>

<span data-ttu-id="edc63-120">Функция с прототип **ACCELERATEABSDI** возвращает TRUE, если он обрабатывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="edc63-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="edc63-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="edc63-121">Remarks</span></span>

<span data-ttu-id="edc63-122">Функции, основанной на прототип **ACCELERATEABSDI** используется только с безрежимным диалоговое окно, то есть только в том случае, если клиентское приложение значение флага DIALOG_SDI в член _ulFlags_ структуры [ADRPARM](adrparm.md) .</span><span class="sxs-lookup"><span data-stu-id="edc63-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="edc63-123">Безрежимные диалоговое окно общего клиентского приложения Windows цикл обработки сообщений, а не через собственный цикл обработки.</span><span class="sxs-lookup"><span data-stu-id="edc63-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="edc63-124">Приложения, который управляет цикл обработки сообщений, не знать, какие сочетания клавиш, используется диалоговое окно, поэтому он вызывает **ACCELERATEABSDI** на основе функцию, чтобы проверить, а также для выполнения сочетания клавиш, например CTRL + P для печати.</span><span class="sxs-lookup"><span data-stu-id="edc63-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="edc63-125">Вызовы цикла сообщений клиента **ACCELERATEABSDI** на основе функции, когда клиент вызывает диалоговое окно безрежимным адресной книги с помощью метода [IAddrBook::Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="edc63-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="edc63-126">Этот вызов будет завершен при MAPI вызывает функцию на основании прототипа функции [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="edc63-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

