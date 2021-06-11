---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416834"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="d6fcc-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="d6fcc-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="d6fcc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6fcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6fcc-105">Слой **интерфейса IStorage** на **объект IStream.**</span><span class="sxs-lookup"><span data-stu-id="d6fcc-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6fcc-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d6fcc-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6fcc-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d6fcc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d6fcc-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d6fcc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d6fcc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d6fcc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d6fcc-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d6fcc-110">Called by:</span></span>  <br/> |<span data-ttu-id="d6fcc-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d6fcc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="d6fcc-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6fcc-112">Parameters</span></span>

 <span data-ttu-id="d6fcc-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="d6fcc-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="d6fcc-114">[in] Указатель на **объект IUnknown,** реализующий **IStream.**</span><span class="sxs-lookup"><span data-stu-id="d6fcc-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="d6fcc-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d6fcc-115">_lpInterface_</span></span>
  
> <span data-ttu-id="d6fcc-116">[in] Указатель на идентификатор интерфейса (IID) для объекта потока.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="d6fcc-117">Любое из следующих значений можно передать в  _параметре lpInterface:_ NULL, IID_IStream или IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="d6fcc-118">Передача NULL в  _lpInterface_ такая же, как передача IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="d6fcc-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6fcc-119">_ulFlags_</span></span>
  
> <span data-ttu-id="d6fcc-120">[in] Bitmask флагов, которые контролируют, как должен быть создан объект хранилища по отношению к потоку.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="d6fcc-121">Параметр по умолчанию STGSTRM_RESET, который предоставляет объекту хранилища только для чтения доступ и запускает его в нулевом положении потока.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="d6fcc-122">Следующие флаги можно установить в любой комбинации, за исключением отмеченных:</span><span class="sxs-lookup"><span data-stu-id="d6fcc-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="d6fcc-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="d6fcc-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="d6fcc-124">Создает новый объект хранения для объекта потока.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="d6fcc-125">Этот флаг нельзя установить, если STGSTRM_RESET заданной.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="d6fcc-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="d6fcc-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="d6fcc-127">Запускает хранилище в текущем положении потока.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="d6fcc-128">Этот флаг нельзя установить, если STGSTRM_RESET заданной.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="d6fcc-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d6fcc-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="d6fcc-130">Позволяет поставщику вызываемой службы записывать на возвращенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="d6fcc-131">Этот флаг нельзя установить, если STGSTRM_RESET заданной.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="d6fcc-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="d6fcc-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="d6fcc-133">Запускает хранилище с нулевой позиции.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-133">Starts storage at position zero.</span></span> <span data-ttu-id="d6fcc-134">Этот флаг нельзя установить, если заданной является другой флаг.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="d6fcc-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="d6fcc-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="d6fcc-136">[вышел] Указатель на указатель на возвращенный **объект IStorage.**</span><span class="sxs-lookup"><span data-stu-id="d6fcc-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6fcc-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6fcc-137">Return value</span></span>

<span data-ttu-id="d6fcc-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6fcc-138">S_OK</span></span> 
  
> <span data-ttu-id="d6fcc-139">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6fcc-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6fcc-140">Remarks</span></span>

<span data-ttu-id="d6fcc-141">Поставщики магазинов сообщений поддерживают **функцию HrIStorageFromStream** с помощью **интерфейса IStorage** для вложений.</span><span class="sxs-lookup"><span data-stu-id="d6fcc-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="d6fcc-142">Поставщики магазинов должны реализовать **интерфейс IStream.**</span><span class="sxs-lookup"><span data-stu-id="d6fcc-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="d6fcc-143">**HrIStorageFromStream** предоставляет **интерфейс IStorage** для **объекта IStream.**</span><span class="sxs-lookup"><span data-stu-id="d6fcc-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="d6fcc-144">В _lpUnkIn_ можно передать **интерфейс ILockBytes** или **IStream.**</span><span class="sxs-lookup"><span data-stu-id="d6fcc-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

