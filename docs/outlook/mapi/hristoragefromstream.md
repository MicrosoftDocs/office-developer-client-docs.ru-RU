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
ms.openlocfilehash: 39f28d5a8e9c8c7f3dfc6a8d09cf022cea08800c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563927"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="19451-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="19451-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="19451-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19451-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19451-105">Слои интерфейс **IStorage** на объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="19451-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19451-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="19451-106">Header file:</span></span>  <br/> |<span data-ttu-id="19451-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="19451-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="19451-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="19451-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="19451-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="19451-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="19451-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="19451-110">Called by:</span></span>  <br/> |<span data-ttu-id="19451-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="19451-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="19451-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="19451-112">Parameters</span></span>

 <span data-ttu-id="19451-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="19451-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="19451-114">[in] Указатель на **интерфейс IUnknown** объект, реализующий **IStream**.</span><span class="sxs-lookup"><span data-stu-id="19451-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="19451-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="19451-115">_lpInterface_</span></span>
  
> <span data-ttu-id="19451-116">[in] Указатель на объект stream с идентификатором интерфейса (ИД интерфейса).</span><span class="sxs-lookup"><span data-stu-id="19451-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="19451-117">Может быть передан в параметре _lpInterface_ , какие-либо из следующих значений: значение NULL, IID_IStream или IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="19451-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="19451-118">Указать значение NULL для _lpInterface_ совпадает с передачей IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="19451-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="19451-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19451-119">_ulFlags_</span></span>
  
> <span data-ttu-id="19451-120">[in] Битовая маска флаги, который определяет, как должен быть создан относительно в потоке объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="19451-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="19451-121">Значение по умолчанию — STGSTRM_RESET, который предоставляет доступ только для чтения объекта хранилища и запускает его в нулевой позиции потока.</span><span class="sxs-lookup"><span data-stu-id="19451-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="19451-122">Следующие флаги могут устанавливаться в любом сочетании, за исключением как было указано:</span><span class="sxs-lookup"><span data-stu-id="19451-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="19451-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="19451-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="19451-124">Создает новый объект хранилища для объекта потока.</span><span class="sxs-lookup"><span data-stu-id="19451-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="19451-125">Не удается установить этот флаг, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="19451-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="19451-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="19451-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="19451-127">Запускает хранилища в текущей позиции потока.</span><span class="sxs-lookup"><span data-stu-id="19451-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="19451-128">Не удается установить этот флаг, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="19451-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="19451-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="19451-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="19451-130">Позволяет вызова поставщику услуг для записи возвращенные хранилища.</span><span class="sxs-lookup"><span data-stu-id="19451-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="19451-131">Не удается установить этот флаг, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="19451-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="19451-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="19451-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="19451-133">Запускает хранилища в нулевой позиции.</span><span class="sxs-lookup"><span data-stu-id="19451-133">Starts storage at position zero.</span></span> <span data-ttu-id="19451-134">Не удается установить этот флаг, если установить любой другой флаг.</span><span class="sxs-lookup"><span data-stu-id="19451-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="19451-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="19451-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="19451-136">[out] Указатель на указатель на возвращенный объект **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="19451-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19451-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19451-137">Return value</span></span>

<span data-ttu-id="19451-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="19451-138">S_OK</span></span> 
  
> <span data-ttu-id="19451-139">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="19451-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19451-140">���������</span><span class="sxs-lookup"><span data-stu-id="19451-140">Remarks</span></span>

<span data-ttu-id="19451-141">Сообщение хранилища поставщики поддерживают функцию **HrIStorageFromStream** , с помощью интерфейса **IStorage** для вложений.</span><span class="sxs-lookup"><span data-stu-id="19451-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="19451-142">Поставщики Store должна реализовать интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="19451-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="19451-143">**HrIStorageFromStream** предоставляет интерфейс **IStorage** для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="19451-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="19451-144">Можно передать **ILockBytes** или интерфейс **IStream** в _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="19451-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

