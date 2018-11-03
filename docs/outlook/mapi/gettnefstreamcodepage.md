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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399657"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="a3e56-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="a3e56-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="a3e56-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3e56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3e56-105">Определяет кодовую страницу для потока Transport-Neutral Encapsulation формата TNEF ().</span><span class="sxs-lookup"><span data-stu-id="a3e56-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3e56-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a3e56-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3e56-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="a3e56-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="a3e56-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a3e56-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3e56-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3e56-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3e56-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a3e56-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3e56-111">Клиентские приложения и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="a3e56-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="a3e56-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3e56-112">Parameters</span></span>

 <span data-ttu-id="a3e56-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="a3e56-113">_lpStream_</span></span>
  
> <span data-ttu-id="a3e56-114">[in] Указатель на хранилище потока объекта OLE **IStream** интерфейс предоставление источника для потока сообщения в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="a3e56-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="a3e56-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="a3e56-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="a3e56-116">[out] Указатель на страницу кода потока.</span><span class="sxs-lookup"><span data-stu-id="a3e56-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="a3e56-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="a3e56-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="a3e56-118">[out] Указатель на страницу subcode потока.</span><span class="sxs-lookup"><span data-stu-id="a3e56-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3e56-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3e56-119">Return value</span></span>

 <span data-ttu-id="a3e56-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="a3e56-120">**S_OK**</span></span>
  
> <span data-ttu-id="a3e56-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a3e56-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="a3e56-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="a3e56-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="a3e56-123">Возникла ошибка при чтении атрибута в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="a3e56-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="a3e56-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="a3e56-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="a3e56-125">Поток не поток TNEF либо произошла ошибка при чтении атрибута attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="a3e56-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3e56-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3e56-126">Remarks</span></span>

<span data-ttu-id="a3e56-127">Используйте функцию **GetTnefStreamCodepage** для чтения атрибута **attOemCodepage** поток TNEF для определения кода страницы и страницы дополнительный код.</span><span class="sxs-lookup"><span data-stu-id="a3e56-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="a3e56-128">Если **attOemCodepage** не найден, **GetTnefStreamCodepage** возвращает кодовую страницу 437 и страницы subcode 0.</span><span class="sxs-lookup"><span data-stu-id="a3e56-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3e56-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a3e56-129">See also</span></span>



[<span data-ttu-id="a3e56-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="a3e56-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

