---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431514"
---
# <a name="lpfnbutton"></a><span data-ttu-id="2b4e6-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="2b4e6-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="2b4e6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b4e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b4e6-105">Определяет функцию вызова, вызываемую MAPI для активации необязательного управления кнопками в диалоговом окне адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="2b4e6-106">Эта кнопка обычно является кнопкой **Details.**</span><span class="sxs-lookup"><span data-stu-id="2b4e6-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b4e6-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2b4e6-107">Header file:</span></span>  <br/> |<span data-ttu-id="2b4e6-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b4e6-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2b4e6-109">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="2b4e6-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2b4e6-110">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="2b4e6-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="2b4e6-111">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="2b4e6-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2b4e6-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="2b4e6-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2b4e6-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="2b4e6-113">Parameters</span></span>

 <span data-ttu-id="2b4e6-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2b4e6-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="2b4e6-115">[in] Ручка родительских окон для любых диалогов или окон эта функция отображает.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="2b4e6-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="2b4e6-116">_lpvContext_</span></span>
  
> <span data-ttu-id="2b4e6-117">[in] Указатель на произвольное значение, переданного функции вызова при вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="2b4e6-118">Это значение может представлять адрес значения для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="2b4e6-119">Как правило, для кода C++  _lpvContext_ представляет указатель на объект C++.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="2b4e6-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2b4e6-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="2b4e6-121">[in] Размер в bytes идентификатора записи, на который указывает параметр _lpSelection._</span><span class="sxs-lookup"><span data-stu-id="2b4e6-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="2b4e6-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="2b4e6-122">_lpSelection_</span></span>
  
> <span data-ttu-id="2b4e6-123">[in] Указатель на идентификатор записи, определяющий выбор в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="2b4e6-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2b4e6-124">_ulFlags_</span></span>
  
> <span data-ttu-id="2b4e6-125">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2b4e6-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b4e6-126">Return value</span></span>

<span data-ttu-id="2b4e6-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b4e6-127">S_OK</span></span> 
  
> <span data-ttu-id="2b4e6-128">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b4e6-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b4e6-129">Remarks</span></span>

<span data-ttu-id="2b4e6-130">Клиентские приложения называют функцию вызова на основе прототипа **LPFNBUTTON,** чтобы определить кнопку в диалоговом окне подробностей.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="2b4e6-131">Клиент передает указатель на функцию вызова вызовов в [метод IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="2b4e6-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="2b4e6-132">Поставщики услуг называют функцию крюка на основе прототипа **LPFNBUTTON,** чтобы определить кнопку в диалоговом окне подробностей.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="2b4e6-133">Поставщик передает указатель на эту функцию крючка в вызовах к методу [IMAPISupport::D etails.](imapisupport-details.md)</span><span class="sxs-lookup"><span data-stu-id="2b4e6-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="2b4e6-134">В обоих случаях, когда диалоговое окно отображается и пользователь выбирает заданная кнопка, MAPI вызывает **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="2b4e6-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b4e6-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2b4e6-135">See also</span></span>



[<span data-ttu-id="2b4e6-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="2b4e6-136">BuildDisplayTable</span></span>](builddisplaytable.md)

