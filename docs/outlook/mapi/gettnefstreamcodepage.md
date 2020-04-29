---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299435"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="e15ac-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="e15ac-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="e15ac-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e15ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e15ac-105">Определяет кодовую страницу для потока TNEF (протокол инкапсуляции формата инкапсуляции).</span><span class="sxs-lookup"><span data-stu-id="e15ac-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e15ac-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e15ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="e15ac-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="e15ac-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="e15ac-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e15ac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e15ac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e15ac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e15ac-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e15ac-110">Called by:</span></span>  <br/> |<span data-ttu-id="e15ac-111">Клиентские приложения и поставщики услуг.</span><span class="sxs-lookup"><span data-stu-id="e15ac-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="e15ac-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e15ac-112">Parameters</span></span>

 <span data-ttu-id="e15ac-113">_лпстреам_</span><span class="sxs-lookup"><span data-stu-id="e15ac-113">_lpStream_</span></span>
  
> <span data-ttu-id="e15ac-114">возврата Указатель на объект потока хранилища OLE **IStream** , предоставляющий источник сообщения для потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="e15ac-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="e15ac-115">_лпулкодепаже_</span><span class="sxs-lookup"><span data-stu-id="e15ac-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="e15ac-116">вышли Указатель на кодовую страницу в потоке.</span><span class="sxs-lookup"><span data-stu-id="e15ac-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="e15ac-117">_лпулсубкодепаже_</span><span class="sxs-lookup"><span data-stu-id="e15ac-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="e15ac-118">вышли Указатель на страницу подкода потока.</span><span class="sxs-lookup"><span data-stu-id="e15ac-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e15ac-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e15ac-119">Return value</span></span>

 <span data-ttu-id="e15ac-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="e15ac-120">**S_OK**</span></span>
  
> <span data-ttu-id="e15ac-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="e15ac-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="e15ac-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="e15ac-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="e15ac-123">Произошла ошибка при чтении атрибута в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="e15ac-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="e15ac-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="e15ac-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="e15ac-125">Поток не являлся потоком TNEF или возникла ошибка при чтении атрибута Аттоемкодепаже.</span><span class="sxs-lookup"><span data-stu-id="e15ac-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e15ac-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="e15ac-126">Remarks</span></span>

<span data-ttu-id="e15ac-127">Используйте функцию **жеттнефстреамкодепаже** для считывания атрибута **аттоемкодепаже** потока TNEF, чтобы определить кодовую страницу и страницу подкода.</span><span class="sxs-lookup"><span data-stu-id="e15ac-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="e15ac-128">Если **аттоемкодепаже** не найден, **жеттнефстреамкодепаже** возвращает кодовую страницу 437 и страницу подкода 0.</span><span class="sxs-lookup"><span data-stu-id="e15ac-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e15ac-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e15ac-129">See also</span></span>



[<span data-ttu-id="e15ac-130">аттоемкодепаже</span><span class="sxs-lookup"><span data-stu-id="e15ac-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

