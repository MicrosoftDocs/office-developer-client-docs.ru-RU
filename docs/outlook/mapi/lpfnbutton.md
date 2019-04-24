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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357444"
---
# <a name="lpfnbutton"></a><span data-ttu-id="78656-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="78656-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="78656-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78656-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78656-105">Определяет функцию обратного вызова, которая вызывается MAPI для активации необязательного элемента управления "Кнопка" в диалоговом окне Адресная книга.</span><span class="sxs-lookup"><span data-stu-id="78656-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="78656-106">Как правило, эта кнопка является кнопкой **подробных сведений** .</span><span class="sxs-lookup"><span data-stu-id="78656-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78656-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="78656-107">Header file:</span></span>  <br/> |<span data-ttu-id="78656-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="78656-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="78656-109">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="78656-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="78656-110">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="78656-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="78656-111">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="78656-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="78656-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="78656-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="78656-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="78656-113">Parameters</span></span>

 <span data-ttu-id="78656-114">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="78656-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="78656-115">возврата Дескриптор родительских окон для всех диалоговых окон или окон, отображаемых этой функцией.</span><span class="sxs-lookup"><span data-stu-id="78656-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="78656-116">_Лпвконтекст_</span><span class="sxs-lookup"><span data-stu-id="78656-116">_lpvContext_</span></span>
  
> <span data-ttu-id="78656-117">возврата Указатель на произвольное значение, переданное функции обратного вызова при ее вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="78656-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="78656-118">Это значение может представлять собой адрес, значимый клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="78656-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="78656-119">Как правило, для кода C++ _лпвконтекст_ представляет указатель на объект c++.</span><span class="sxs-lookup"><span data-stu-id="78656-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="78656-120">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="78656-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="78656-121">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _лпселектион_ .</span><span class="sxs-lookup"><span data-stu-id="78656-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="78656-122">_Лпселектион_</span><span class="sxs-lookup"><span data-stu-id="78656-122">_lpSelection_</span></span>
  
> <span data-ttu-id="78656-123">возврата Указатель на идентификатор записи, определяющий выделенный фрагмент в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="78656-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="78656-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78656-124">_ulFlags_</span></span>
  
> <span data-ttu-id="78656-125">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="78656-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78656-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78656-126">Return value</span></span>

<span data-ttu-id="78656-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="78656-127">S_OK</span></span> 
  
> <span data-ttu-id="78656-128">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="78656-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78656-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="78656-129">Remarks</span></span>

<span data-ttu-id="78656-130">Клиентские приложения вызывают функцию обратного вызова на основе прототипа **лпфнбуттон** , чтобы определить кнопку в диалоговом окне Details (сведения).</span><span class="sxs-lookup"><span data-stu-id="78656-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="78656-131">Клиент передает указатель на функцию обратного вызова в вызове метода [IAddrBook::D етаилс](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="78656-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="78656-132">Поставщики услуг вызывают функцию-ловушку на основе прототипа **лпфнбуттон** , чтобы определить кнопку в диалоговом окне "сведения".</span><span class="sxs-lookup"><span data-stu-id="78656-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="78656-133">Поставщик передает указатель на эту функцию-ловушку при вызове метода [имаписуппорт::D етаилс](imapisupport-details.md) .</span><span class="sxs-lookup"><span data-stu-id="78656-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="78656-134">В обоих случаях при отображении диалогового окна, когда пользователь выбирает определенную кнопку, MAPI вызывает **лпфнбуттон**.</span><span class="sxs-lookup"><span data-stu-id="78656-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78656-135">См. также</span><span class="sxs-lookup"><span data-stu-id="78656-135">See also</span></span>



[<span data-ttu-id="78656-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="78656-136">BuildDisplayTable</span></span>](builddisplaytable.md)

