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
# <a name="hristoragefromstream"></a><span data-ttu-id="7c30e-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="7c30e-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="7c30e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c30e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c30e-105">Слои интерфейс **IStorage** в объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="7c30e-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c30e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7c30e-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c30e-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="7c30e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7c30e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7c30e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c30e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7c30e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7c30e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7c30e-110">Called by:</span></span>  <br/> |<span data-ttu-id="7c30e-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="7c30e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="7c30e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c30e-112">Parameters</span></span>

 <span data-ttu-id="7c30e-113">_лпункин_</span><span class="sxs-lookup"><span data-stu-id="7c30e-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="7c30e-114">возврата Указатель на объект **IUnknown** , реализующий **IStream**.</span><span class="sxs-lookup"><span data-stu-id="7c30e-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="7c30e-115">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="7c30e-115">_lpInterface_</span></span>
  
> <span data-ttu-id="7c30e-116">возврата Указатель на идентификатор интерфейса (IID) для объекта Stream.</span><span class="sxs-lookup"><span data-stu-id="7c30e-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="7c30e-117">В параметре _лпинтерфаце_ можно передать любое из следующих значений: NULL, IID_IStream или IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="7c30e-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="7c30e-118">Передача значения NULL в _лпинтерфаце_ выполняется так же, как передача IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="7c30e-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="7c30e-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7c30e-119">_ulFlags_</span></span>
  
> <span data-ttu-id="7c30e-120">возврата Битовая маска флагов, которые управляют способом создания объекта хранилища относительно потока.</span><span class="sxs-lookup"><span data-stu-id="7c30e-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="7c30e-121">Значение по умолчанию — STGSTRM_RESET, которое предоставляет объекту хранилища доступ только для чтения и запускает его в позиции 0 потока.</span><span class="sxs-lookup"><span data-stu-id="7c30e-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="7c30e-122">Следующие флаги можно задавать в любом сочетании, за исключением отмеченных.</span><span class="sxs-lookup"><span data-stu-id="7c30e-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="7c30e-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="7c30e-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="7c30e-124">Создает новый объект Storage для объекта Stream.</span><span class="sxs-lookup"><span data-stu-id="7c30e-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="7c30e-125">Этот флаг не может быть установлен, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="7c30e-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="7c30e-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="7c30e-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="7c30e-127">Запускает хранилище в текущей позиции потока.</span><span class="sxs-lookup"><span data-stu-id="7c30e-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="7c30e-128">Этот флаг не может быть установлен, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="7c30e-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="7c30e-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7c30e-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="7c30e-130">Позволяет поставщику службы вызовов записывать в возвращенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="7c30e-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="7c30e-131">Этот флаг не может быть установлен, если установлен флаг STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="7c30e-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="7c30e-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="7c30e-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="7c30e-133">Запускает хранилище в нулевой позиции.</span><span class="sxs-lookup"><span data-stu-id="7c30e-133">Starts storage at position zero.</span></span> <span data-ttu-id="7c30e-134">Этот флаг не может быть установлен, если задан любой другой флаг.</span><span class="sxs-lookup"><span data-stu-id="7c30e-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="7c30e-135">_лппсторажеаут_</span><span class="sxs-lookup"><span data-stu-id="7c30e-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="7c30e-136">вышли Указатель на указатель на возвращенный объект **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="7c30e-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7c30e-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c30e-137">Return value</span></span>

<span data-ttu-id="7c30e-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c30e-138">S_OK</span></span> 
  
> <span data-ttu-id="7c30e-139">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7c30e-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c30e-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="7c30e-140">Remarks</span></span>

<span data-ttu-id="7c30e-141">Поставщики хранилища сообщений поддерживают функцию **христоражефромстреам** , используя интерфейс **IStorage** для вложений.</span><span class="sxs-lookup"><span data-stu-id="7c30e-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="7c30e-142">Поставщики хранилища должны реализовать интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="7c30e-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="7c30e-143">**Христоражефромстреам** предоставляет интерфейс **IStorage** для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="7c30e-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="7c30e-144">Можно передать либо интерфейс **ILockBytes** , либо интерфейс **IStream** в _лпункин_.</span><span class="sxs-lookup"><span data-stu-id="7c30e-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

