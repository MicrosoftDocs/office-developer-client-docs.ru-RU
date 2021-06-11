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
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316590"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="d6420-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="d6420-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="d6420-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6420-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6420-105">Реализует объект хранения для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="d6420-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="d6420-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6420-106">Parameters</span></span>

 <span data-ttu-id="d6420-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="d6420-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="d6420-108">[in] Указатель на объект потока.</span><span class="sxs-lookup"><span data-stu-id="d6420-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="d6420-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d6420-109">_lpInterface_</span></span>
  
> <span data-ttu-id="d6420-110">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к потоку, на который указывает _lpUnkIn._</span><span class="sxs-lookup"><span data-stu-id="d6420-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="d6420-111">Любое из следующих значений допустимо: IID_IStream, IID_ILockBytes или **null,** что указывает на то, что интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) должен использоваться для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="d6420-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="d6420-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6420-112">_ulFlags_</span></span>
  
> <span data-ttu-id="d6420-113">[in] Немного флагов, которые контролируют, как должен создаваться объект хранилища по отношению к объекту потока.</span><span class="sxs-lookup"><span data-stu-id="d6420-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="d6420-114">По умолчанию хранилище создается с доступом только для чтения, а поток начинается с нуля в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d6420-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="d6420-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d6420-115">The following flags can be set:</span></span>
    
<span data-ttu-id="d6420-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="d6420-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="d6420-117">Для объекта потока необходимо создать новый объект хранения.</span><span class="sxs-lookup"><span data-stu-id="d6420-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="d6420-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="d6420-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="d6420-119">Объект хранилища должен начинаться с текущего положения потока.</span><span class="sxs-lookup"><span data-stu-id="d6420-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="d6420-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d6420-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="d6420-121">Вызываемая должна иметь разрешение на чтение и записи возвращаемого объекта хранения.</span><span class="sxs-lookup"><span data-stu-id="d6420-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="d6420-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="d6420-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="d6420-123">Объект хранилища должен начинаться с нуля.</span><span class="sxs-lookup"><span data-stu-id="d6420-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="d6420-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="d6420-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="d6420-125">[вышел] Указатель на указатель на объект хранения.</span><span class="sxs-lookup"><span data-stu-id="d6420-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6420-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6420-126">Return value</span></span>

<span data-ttu-id="d6420-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6420-127">S_OK</span></span> 
  
> <span data-ttu-id="d6420-128">Объект хранения был успешно создан.</span><span class="sxs-lookup"><span data-stu-id="d6420-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6420-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6420-129">Remarks</span></span>

<span data-ttu-id="d6420-130">Метод **IMAPISupport::IStorageFromStream** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d6420-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d6420-131">Поставщики услуг называют **IStorageFromStream** для создания объекта хранения, который будет использовать для открытия определенных свойств.</span><span class="sxs-lookup"><span data-stu-id="d6420-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="d6420-132">Поставщикам услуг, которые имеют собственную реализацию интерфейса [IStorage,](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) не нужно вызывать **IStorageFromStream.**</span><span class="sxs-lookup"><span data-stu-id="d6420-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="d6420-133">Объект хранения, созданный **IStorageFromStream,** вызывает метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) чтобы прибавить количество ссылок, а затем приумножает количество, когда хранилище будет выпущено.</span><span class="sxs-lookup"><span data-stu-id="d6420-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d6420-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d6420-134">Notes to callers</span></span>

<span data-ttu-id="d6420-135">Когда [метод IMAPIProp::OpenProperty](imapiprop-openproperty.md) одного из объектов вызван для открытия свойства с интерфейсом **IStorage,** выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="d6420-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="d6420-136">Откройте объект потока с разрешением чтения и записи для свойства.</span><span class="sxs-lookup"><span data-stu-id="d6420-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="d6420-137">Внутренне пометить поток свойств как объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="d6420-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="d6420-138">Вызов **IStorageFromStream для** создания объекта хранения.</span><span class="sxs-lookup"><span data-stu-id="d6420-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="d6420-139">Верни указатель этому объекту хранения.</span><span class="sxs-lookup"><span data-stu-id="d6420-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="d6420-140">Если вы реализуете дополнительные интерфейсы, которые используют объект хранения, создайте объект, который заворачивает объект хранилища, и реализуйте метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="d6420-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="d6420-141">Не разрешайте открывать свойство с интерфейсом **IStream,** если оно создано **с помощью IStorage.**</span><span class="sxs-lookup"><span data-stu-id="d6420-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="d6420-142">И наоборот, не разрешайте открывать свойство с интерфейсом **IStorage,** если оно создано **с помощью IStream.**</span><span class="sxs-lookup"><span data-stu-id="d6420-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="d6420-143">За одним исключением можно использовать интерфейс **IStreamDocfile** для потоковой передачи объекта хранения из одного контейнера в другой, но идентификатор интерфейса IID_IStreamDocfile должен быть передан в _параметре lpInterface_ метода **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="d6420-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6420-144">См. также</span><span class="sxs-lookup"><span data-stu-id="d6420-144">See also</span></span>



[<span data-ttu-id="d6420-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="d6420-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="d6420-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6420-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

