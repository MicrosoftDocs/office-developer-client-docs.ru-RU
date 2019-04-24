---
title: Имаписуппортисторажефромстреам
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
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="3ee18-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="3ee18-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="3ee18-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ee18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ee18-105">Реализует объект Storage для доступа к потоку.</span><span class="sxs-lookup"><span data-stu-id="3ee18-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="3ee18-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ee18-106">Parameters</span></span>

 <span data-ttu-id="3ee18-107">_Лпункин_</span><span class="sxs-lookup"><span data-stu-id="3ee18-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="3ee18-108">возврата Указатель на объект Stream.</span><span class="sxs-lookup"><span data-stu-id="3ee18-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="3ee18-109">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="3ee18-109">_lpInterface_</span></span>
  
> <span data-ttu-id="3ee18-110">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к потоку, на который указывает _лпункин_.</span><span class="sxs-lookup"><span data-stu-id="3ee18-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="3ee18-111">Допустимы следующие значения: Иид_истреам, Иид_илоккбитес или **null**, что указывает на то, что для доступа к потоку должен использоваться интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3ee18-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="3ee18-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ee18-112">_ulFlags_</span></span>
  
> <span data-ttu-id="3ee18-113">возврата Битовая маска флагов, которые управляют способом создания объекта хранилища относительно объекта Stream.</span><span class="sxs-lookup"><span data-stu-id="3ee18-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="3ee18-114">По умолчанию хранилище создается с доступом только для чтения, а поток начинается с нулевой позиции в хранилище.</span><span class="sxs-lookup"><span data-stu-id="3ee18-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="3ee18-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="3ee18-115">The following flags can be set:</span></span>
    
<span data-ttu-id="3ee18-116">СТГСТРМ_КРЕАТЕ</span><span class="sxs-lookup"><span data-stu-id="3ee18-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="3ee18-117">Для объекта Stream необходимо создать новый объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ee18-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="3ee18-118">СТГСТРМ_КУРРЕНТ</span><span class="sxs-lookup"><span data-stu-id="3ee18-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="3ee18-119">Объект Storage должен начинаться с текущей позиции в потоке.</span><span class="sxs-lookup"><span data-stu-id="3ee18-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="3ee18-120">СТГСТРМ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="3ee18-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="3ee18-121">Вызывающий абонент должен иметь разрешение на чтение и запись возвращенного объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ee18-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="3ee18-122">СТГСТРМ_РЕСЕТ</span><span class="sxs-lookup"><span data-stu-id="3ee18-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="3ee18-123">Объект Storage должен начинаться с позиции 0.</span><span class="sxs-lookup"><span data-stu-id="3ee18-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="3ee18-124">_Лппсторажеаут_</span><span class="sxs-lookup"><span data-stu-id="3ee18-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="3ee18-125">вышли Указатель на указатель на объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ee18-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ee18-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ee18-126">Return value</span></span>

<span data-ttu-id="3ee18-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ee18-127">S_OK</span></span> 
  
> <span data-ttu-id="3ee18-128">Объект хранилища успешно создан.</span><span class="sxs-lookup"><span data-stu-id="3ee18-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ee18-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="3ee18-129">Remarks</span></span>

<span data-ttu-id="3ee18-130">Метод **имаписуппорт:: исторажефромстреам** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="3ee18-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="3ee18-131">Поставщики услуг вызывают **исторажефромстреам** , чтобы создать объект хранилища, который будет использоваться для открытия определенных свойств.</span><span class="sxs-lookup"><span data-stu-id="3ee18-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="3ee18-132">Поставщики услуг, у которых есть собственная реализация интерфейса [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) , не обязаны вызывать **исторажефромстреам**.</span><span class="sxs-lookup"><span data-stu-id="3ee18-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="3ee18-133">Объект хранилища, созданный с помощью **исторажефромстреам** , вызывает метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для увеличения счетчика ссылок, а затем уменьшает значение счетчика при отпускании хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ee18-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ee18-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3ee18-134">Notes to callers</span></span>

<span data-ttu-id="3ee18-135">При вызове метода [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) одного из объектов, чтобы открыть свойство с интерфейсом **IStorage** , выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="3ee18-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="3ee18-136">Откройте объект Stream с разрешениями на чтение и запись для свойства.</span><span class="sxs-lookup"><span data-stu-id="3ee18-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="3ee18-137">Помечает поток свойств как объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ee18-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="3ee18-138">Call **исторажефромстреам** для создания объекта Storage.</span><span class="sxs-lookup"><span data-stu-id="3ee18-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="3ee18-139">Возвращает указатель на этот объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ee18-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="3ee18-140">При реализации дополнительных интерфейсов, использующих объект Storage, создайте объект, который упаковывает объект Storage и реализует метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) более высокого уровня::.</span><span class="sxs-lookup"><span data-stu-id="3ee18-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="3ee18-141">Не разрешать открытие свойства с помощью интерфейса **IStream** , если он был создан с помощью **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="3ee18-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="3ee18-142">И наоборот, не разрешать открытие свойства с помощью интерфейса **IStorage** , если он был создан с помощью **IStream**.</span><span class="sxs-lookup"><span data-stu-id="3ee18-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="3ee18-143">С одним исключением можно использовать интерфейс **помощью istreamdocfile** для потоковой передачи объекта хранилища из одного контейнера в другой, но идентификатор интерфейса иид_истреамдокфиле должен быть передан в методе **опенпроперти** _лпинтерфаце _параметр.</span><span class="sxs-lookup"><span data-stu-id="3ee18-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ee18-144">См. также</span><span class="sxs-lookup"><span data-stu-id="3ee18-144">See also</span></span>



[<span data-ttu-id="3ee18-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="3ee18-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="3ee18-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ee18-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

