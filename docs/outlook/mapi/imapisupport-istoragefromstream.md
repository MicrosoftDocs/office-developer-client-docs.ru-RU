---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a73c87f172b4c97379bb9cd117679d3947c188af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809130"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="e5fce-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="e5fce-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="e5fce-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5fce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5fce-105">Реализует объект хранилища для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="e5fce-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="e5fce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5fce-106">Parameters</span></span>

 <span data-ttu-id="e5fce-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="e5fce-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="e5fce-108">[in] Указатель на объект stream.</span><span class="sxs-lookup"><span data-stu-id="e5fce-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="e5fce-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e5fce-109">_lpInterface_</span></span>
  
> <span data-ttu-id="e5fce-110">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к потоку, на который указывает _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="e5fce-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="e5fce-111">Допустимы любые из следующих значений: IID_IStream, IID_ILockBytes, или **значение null**, это означает, что интерфейс [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) должен использоваться для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="e5fce-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="e5fce-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5fce-112">_ulFlags_</span></span>
  
> <span data-ttu-id="e5fce-113">[in] Битовая маска флаги, который определяет, как должны создаваться по отношению к объекту потока объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5fce-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="e5fce-114">По умолчанию хранение создается с доступом только для чтения и начинается поток в нулевой позиции в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e5fce-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="e5fce-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="e5fce-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e5fce-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="e5fce-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="e5fce-117">Следует создавать новый объект хранилища для объекта потока.</span><span class="sxs-lookup"><span data-stu-id="e5fce-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="e5fce-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e5fce-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="e5fce-119">Объект хранилища будет запускаться в текущей позиции потока.</span><span class="sxs-lookup"><span data-stu-id="e5fce-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="e5fce-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e5fce-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="e5fce-121">Вызывающего должны иметь разрешение на чтение и запись на объект возвращенные хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5fce-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="e5fce-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="e5fce-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="e5fce-123">Объект хранилища будет запускаться в нулевой позиции.</span><span class="sxs-lookup"><span data-stu-id="e5fce-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="e5fce-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="e5fce-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="e5fce-125">[out] Указатель на указатель на объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5fce-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5fce-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="e5fce-127">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e5fce-127">S_OK</span></span> 
  
> <span data-ttu-id="e5fce-128">Объект хранилища успешно создан.</span><span class="sxs-lookup"><span data-stu-id="e5fce-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5fce-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="e5fce-129">Remarks</span></span>

<span data-ttu-id="e5fce-130">Метод **IMAPISupport::IStorageFromStream** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="e5fce-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e5fce-131">Поставщики услуг вызова **IStorageFromStream** для создания объекта хранилища для открытия отдельного свойства.</span><span class="sxs-lookup"><span data-stu-id="e5fce-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="e5fce-132">Поставщики услуг, которые имеют собственные реализации интерфейса [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) не нужно вызвать **IStorageFromStream**.</span><span class="sxs-lookup"><span data-stu-id="e5fce-132">Service providers that have their own implementation of the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="e5fce-133">Объекта хранилища, созданные **IStorageFromStream** вызывает метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) поток для увеличения его счетчик ссылок и уменьшает счетчик после выхода хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5fce-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e5fce-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e5fce-134">Notes to callers</span></span>

<span data-ttu-id="e5fce-135">При вызове метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) одного из объектов для открытия свойства с помощью интерфейса **IStorage** выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="e5fce-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="e5fce-136">Откройте объект потока с разрешением на чтение и запись для свойства.</span><span class="sxs-lookup"><span data-stu-id="e5fce-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="e5fce-137">Внутренне отмечайте потока свойство как объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5fce-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="e5fce-138">Вызов **IStorageFromStream** для создания объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5fce-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="e5fce-139">Возвращает указатель на объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5fce-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="e5fce-140">Если реализовать дополнительные интерфейсы, использующие объекта хранилища, создайте объект, который является оболочкой объекта хранилища и реализуйте метод [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="e5fce-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="e5fce-141">Не разрешать свойство так, чтобы открыть с помощью интерфейса **IStream** , если он был создан **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="e5fce-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="e5fce-142">С другой стороны не разрешать свойство так, чтобы открыть с помощью интерфейса **IStorage** , если он был создан **IStream**.</span><span class="sxs-lookup"><span data-stu-id="e5fce-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="e5fce-143">Одно исключение допускается использование интерфейса **IStreamDocfile** для потоковой передачи объект хранилища из одного контейнера в другой, но идентификатор интерфейса IID_IStreamDocfile должен быть передан в **OpenProperty** метода _lpInterface _параметр.</span><span class="sxs-lookup"><span data-stu-id="e5fce-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5fce-144">См. также</span><span class="sxs-lookup"><span data-stu-id="e5fce-144">See also</span></span>



[<span data-ttu-id="e5fce-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="e5fce-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="e5fce-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5fce-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

