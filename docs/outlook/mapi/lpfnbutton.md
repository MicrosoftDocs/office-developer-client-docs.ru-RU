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
# <a name="lpfnbutton"></a><span data-ttu-id="74d12-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="74d12-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="74d12-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74d12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74d12-105">Определяет функцию вызова, которую MAPI вызывает для активации дополнительного кнопки в диалоговом окне адресной книги.</span><span class="sxs-lookup"><span data-stu-id="74d12-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="74d12-106">Эта кнопка обычно является кнопкой **"Сведения".**</span><span class="sxs-lookup"><span data-stu-id="74d12-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74d12-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="74d12-107">Header file:</span></span>  <br/> |<span data-ttu-id="74d12-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74d12-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="74d12-109">Определяемая функция, реализованная в:</span><span class="sxs-lookup"><span data-stu-id="74d12-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="74d12-110">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="74d12-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="74d12-111">Определяемая функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="74d12-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="74d12-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="74d12-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="74d12-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="74d12-113">Parameters</span></span>

 <span data-ttu-id="74d12-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="74d12-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="74d12-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span><span class="sxs-lookup"><span data-stu-id="74d12-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="74d12-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="74d12-116">_lpvContext_</span></span>
  
> <span data-ttu-id="74d12-117">[in] Указатель на произвольное значение, передав его функции вызова при вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="74d12-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="74d12-118">Это значение может представлять адрес важности для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="74d12-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="74d12-119">Как правило, для кода C++  _lpvContext_ представляет указатель на объект C++.</span><span class="sxs-lookup"><span data-stu-id="74d12-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="74d12-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="74d12-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="74d12-121">[in] Размер идентификатора записи,на который указывает параметр  _lpSelection_ (в bytes).</span><span class="sxs-lookup"><span data-stu-id="74d12-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="74d12-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="74d12-122">_lpSelection_</span></span>
  
> <span data-ttu-id="74d12-123">[in] Указатель на идентификатор записи, определяющий выделение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="74d12-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="74d12-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="74d12-124">_ulFlags_</span></span>
  
> <span data-ttu-id="74d12-125">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="74d12-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74d12-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74d12-126">Return value</span></span>

<span data-ttu-id="74d12-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="74d12-127">S_OK</span></span> 
  
> <span data-ttu-id="74d12-128">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="74d12-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74d12-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="74d12-129">Remarks</span></span>

<span data-ttu-id="74d12-130">Клиентские приложения вызов функции вызова на основе **прототипа LPFNBUTTON** для определения кнопки в диалоговом окне сведений.</span><span class="sxs-lookup"><span data-stu-id="74d12-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="74d12-131">Клиент передает указатель функции вызова в вызовах метода [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="74d12-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="74d12-132">Поставщики услуг вызывать функцию обработки на основе прототипа **LPFNBUTTON,** чтобы определить кнопку в диалоговом окне сведений.</span><span class="sxs-lookup"><span data-stu-id="74d12-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="74d12-133">Поставщик передает указатель на эту функцию обработки в вызовах метода [IMAPISupport::D etails.](imapisupport-details.md)</span><span class="sxs-lookup"><span data-stu-id="74d12-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="74d12-134">В обоих случаях, когда отображается диалоговое окно и пользователь нажмет заданная кнопка, MAPI вызывает **LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="74d12-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74d12-135">См. также</span><span class="sxs-lookup"><span data-stu-id="74d12-135">See also</span></span>



[<span data-ttu-id="74d12-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="74d12-136">BuildDisplayTable</span></span>](builddisplaytable.md)

