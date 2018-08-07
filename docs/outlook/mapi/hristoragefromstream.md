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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: bd2d0a662585e8aba91250786f88dd310fe37e32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808687"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="68b7e-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="68b7e-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="68b7e-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68b7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68b7e-105">Слои интерфейс **IStorage** на объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="68b7e-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68b7e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="68b7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="68b7e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="68b7e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="68b7e-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="68b7e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="68b7e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="68b7e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="68b7e-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="68b7e-110">Called by:</span></span>  <br/> |<span data-ttu-id="68b7e-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="68b7e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="68b7e-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="68b7e-112">Parameters</span></span>

 <span data-ttu-id="68b7e-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="68b7e-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="68b7e-114">[in] Указатель на **интерфейс IUnknown** объект, реализующий **IStream**.</span><span class="sxs-lookup"><span data-stu-id="68b7e-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="68b7e-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="68b7e-115">_lpInterface_</span></span>
  
> <span data-ttu-id="68b7e-116">[in] Указатель на объект stream с идентификатором интерфейса (ИД интерфейса).</span><span class="sxs-lookup"><span data-stu-id="68b7e-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="68b7e-117">Может быть передан в параметре _lpInterface_ , какие-либо из следующих значений: значение NULL, IID_IStream или IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="68b7e-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="68b7e-118">Указать значение NULL для _lpInterface_ совпадает с передачей IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="68b7e-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="68b7e-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68b7e-119">_ulFlags_</span></span>
  
> <span data-ttu-id="68b7e-120">[in] Битовая маска флаги, который определяет, как должен быть создан относительно в потоке объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="68b7e-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="68b7e-121">Значение по умолчанию — STGSTRM_RESET, который предоставляет доступ только для чтения объекта хранилища и запускает его в нулевой позиции потока.</span><span class="sxs-lookup"><span data-stu-id="68b7e-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="68b7e-122">Следующие флаги могут устанавливаться в любом сочетании, за исключением как было указано:</span><span class="sxs-lookup"><span data-stu-id="68b7e-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="68b7e-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="68b7e-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="68b7e-124">Создает новый объект хранилища для объекта потока.</span><span class="sxs-lookup"><span data-stu-id="68b7e-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="68b7e-125">Не удается установить этот флаг, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="68b7e-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="68b7e-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="68b7e-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="68b7e-127">Запускает хранилища в текущей позиции потока.</span><span class="sxs-lookup"><span data-stu-id="68b7e-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="68b7e-128">Не удается установить этот флаг, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="68b7e-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="68b7e-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="68b7e-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="68b7e-130">Позволяет вызова поставщику услуг для записи возвращенные хранилища.</span><span class="sxs-lookup"><span data-stu-id="68b7e-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="68b7e-131">Не удается установить этот флаг, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="68b7e-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="68b7e-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="68b7e-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="68b7e-133">Запускает хранилища в нулевой позиции.</span><span class="sxs-lookup"><span data-stu-id="68b7e-133">Starts storage at position zero.</span></span> <span data-ttu-id="68b7e-134">Не удается установить этот флаг, если установить любой другой флаг.</span><span class="sxs-lookup"><span data-stu-id="68b7e-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="68b7e-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="68b7e-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="68b7e-136">[out] Указатель на указатель на возвращенный объект **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="68b7e-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68b7e-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="68b7e-138">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="68b7e-138">S_OK</span></span> 
  
> <span data-ttu-id="68b7e-139">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="68b7e-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68b7e-140">���������</span><span class="sxs-lookup"><span data-stu-id="68b7e-140">Remarks</span></span>

<span data-ttu-id="68b7e-141">Сообщение хранилища поставщики поддерживают функцию **HrIStorageFromStream** , с помощью интерфейса **IStorage** для вложений.</span><span class="sxs-lookup"><span data-stu-id="68b7e-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="68b7e-142">Поставщики Store должна реализовать интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="68b7e-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="68b7e-143">**HrIStorageFromStream** предоставляет интерфейс **IStorage** для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="68b7e-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="68b7e-144">Можно передать **ILockBytes** или интерфейс **IStream** в _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="68b7e-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

