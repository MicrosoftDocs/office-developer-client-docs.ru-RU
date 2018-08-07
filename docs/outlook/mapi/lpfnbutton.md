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
ms.openlocfilehash: e1f15a5f031f5c5a9568b8a36722eaac011b814c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809656"
---
# <a name="lpfnbutton"></a><span data-ttu-id="716ec-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="716ec-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="716ec-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="716ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="716ec-105">Определяет функцию обратного вызова, которая вызывает MAPI для активации элемента управления необязательно кнопка в диалоговом окне адресной книги.</span><span class="sxs-lookup"><span data-stu-id="716ec-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="716ec-106">Эта кнопка обычно имеет кнопку **сведения** .</span><span class="sxs-lookup"><span data-stu-id="716ec-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="716ec-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="716ec-107">Header file:</span></span>  <br/> |<span data-ttu-id="716ec-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="716ec-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="716ec-109">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="716ec-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="716ec-110">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="716ec-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="716ec-111">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="716ec-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="716ec-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="716ec-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="716ec-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="716ec-113">Parameters</span></span>

 <span data-ttu-id="716ec-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="716ec-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="716ec-115">[in] Дескриптор родительского windows для любого диалоговые окна или окон, эта функция отображает.</span><span class="sxs-lookup"><span data-stu-id="716ec-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="716ec-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="716ec-116">_lpvContext_</span></span>
  
> <span data-ttu-id="716ec-117">[in] Указатель произвольных значение передается функции обратного вызова, когда она вызывается средствами MAPI.</span><span class="sxs-lookup"><span data-stu-id="716ec-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="716ec-118">Это значение может представлять адрес важности для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="716ec-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="716ec-119">Обычно для кода C++ _lpvContext_ представляет указатель на объект C++.</span><span class="sxs-lookup"><span data-stu-id="716ec-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="716ec-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="716ec-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="716ec-121">[in] Размер, в байтах, идентификатор записи, на который указывает параметр _lpSelection_ .</span><span class="sxs-lookup"><span data-stu-id="716ec-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="716ec-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="716ec-122">_lpSelection_</span></span>
  
> <span data-ttu-id="716ec-123">[in] Указатель на идентификатор записи, определяющий выделение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="716ec-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="716ec-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="716ec-124">_ulFlags_</span></span>
  
> <span data-ttu-id="716ec-125">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="716ec-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="716ec-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="716ec-126">Return value</span></span>

<span data-ttu-id="716ec-127">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="716ec-127">S_OK</span></span> 
  
> <span data-ttu-id="716ec-128">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="716ec-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="716ec-129">���������</span><span class="sxs-lookup"><span data-stu-id="716ec-129">Remarks</span></span>

<span data-ttu-id="716ec-130">Клиентские приложения звонков на основании прототип **LPFNBUTTON** определение кнопки в диалоговом окне сведения о функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="716ec-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="716ec-131">Клиент передает указатель на функцию обратного вызова в вызовы метода [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="716ec-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="716ec-132">Поставщиков услуг вызова на основании прототип **LPFNBUTTON** определение кнопки в диалоговом окне сведения о функции обработчик.</span><span class="sxs-lookup"><span data-stu-id="716ec-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="716ec-133">Поставщик передает указатель этой функции обработчика в вызовы метода [IMAPISupport::Details](imapisupport-details.md) .</span><span class="sxs-lookup"><span data-stu-id="716ec-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="716ec-134">В обоих случаях если отображается диалоговое окно и пользователь выбирает определенный кнопка MAPI вызывает **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="716ec-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="716ec-135">См. также</span><span class="sxs-lookup"><span data-stu-id="716ec-135">See also</span></span>



[<span data-ttu-id="716ec-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="716ec-136">BuildDisplayTable</span></span>](builddisplaytable.md)

