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
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="1b7b4-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="1b7b4-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="1b7b4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b7b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b7b4-105">Реализует объект хранилища для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="1b7b4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b7b4-106">Parameters</span></span>

 <span data-ttu-id="1b7b4-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="1b7b4-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="1b7b4-108">[in] Указатель на объект stream.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="1b7b4-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1b7b4-109">_lpInterface_</span></span>
  
> <span data-ttu-id="1b7b4-110">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к потоку, на который указывает _lpUnkIn._</span><span class="sxs-lookup"><span data-stu-id="1b7b4-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="1b7b4-111">Допустимы любые из следующих значений: IID_IStream, IID_ILockBytes **или null,** что означает, что интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) должен использоваться для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="1b7b4-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b7b4-112">_ulFlags_</span></span>
  
> <span data-ttu-id="1b7b4-113">[in] Битоваяmas флагов, которая управляет тем, как создается объект хранилища относительно объекта stream.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="1b7b4-114">По умолчанию хранилище создается с доступом только для чтения, а поток начинается с нуля в хранилище.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="1b7b4-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="1b7b4-115">The following flags can be set:</span></span>
    
<span data-ttu-id="1b7b4-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="1b7b4-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="1b7b4-117">Для объекта stream необходимо создать новый объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="1b7b4-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="1b7b4-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="1b7b4-119">Объект хранилища должен начинаться с текущего положения потока.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="1b7b4-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1b7b4-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="1b7b4-121">Вызываемая должна иметь разрешение на чтение и записи для возвращенного объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="1b7b4-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="1b7b4-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="1b7b4-123">Объект хранилища должен начинаться с нуля.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="1b7b4-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="1b7b4-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="1b7b4-125">[out] Указатель на указатель на объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b7b4-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b7b4-126">Return value</span></span>

<span data-ttu-id="1b7b4-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b7b4-127">S_OK</span></span> 
  
> <span data-ttu-id="1b7b4-128">Объект хранилища успешно создан.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b7b4-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b7b4-129">Remarks</span></span>

<span data-ttu-id="1b7b4-130">Метод **IMAPISupport::IStorageFromStream** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="1b7b4-131">Поставщики услуг вызовите **IStorageFromStream,** чтобы создать объект хранилища, который будет применяться для открытия определенных свойств.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="1b7b4-132">Поставщикам услуг, которые имеют собственную реализацию [интерфейса IStorage,](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) не требуется вызывать **IStorageFromStream.**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="1b7b4-133">Объект хранилища, созданный **IStorageFromStream,** вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) потока для инкрементного подсчета ссылок, а затем при отпущении хранилища понижается.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b7b4-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1b7b4-134">Notes to callers</span></span>

<span data-ttu-id="1b7b4-135">При [выполнении метода IMAPIProp::OpenProperty](imapiprop-openproperty.md) одного из ваших объектов для открытия свойства с помощью интерфейса **IStorage** выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="1b7b4-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="1b7b4-136">Откройте объект stream с разрешением на чтение и записи для свойства.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="1b7b4-137">Внутренне пометить поток свойств как объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="1b7b4-138">Вызовите **IStorageFromStream для** создания объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="1b7b4-139">Возвращает указатель на этот объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="1b7b4-140">При реализации дополнительных интерфейсов, которые используют объект хранилища, создайте объект, который будет обтекать объект хранилища, и реализуйте метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="1b7b4-141">Не разрешайте открывать свойство с помощью **интерфейса IStream,** если оно было создано с помощью **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="1b7b4-142">И наоборот, не разрешайте открывать свойство с помощью **интерфейса IStorage,** если оно было создано с **помощью IStream.**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="1b7b4-143">За одним исключением, можно использовать интерфейс **IStreamDocfile** для потоковой передачи объекта хранилища из одного контейнера в другой, но идентификатор интерфейса IID_IStreamDocfile должен быть передан в _параметре lpInterface_ метода **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b7b4-144">См. также</span><span class="sxs-lookup"><span data-stu-id="1b7b4-144">See also</span></span>



[<span data-ttu-id="1b7b4-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="1b7b4-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="1b7b4-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b7b4-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

