---
title: Имслогонопенентри
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317285"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="7ad8c-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7ad8c-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="7ad8c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ad8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ad8c-105">Открывает папку или объект Message и возвращает указатель на объект, предоставляющий дополнительный доступ.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="7ad8c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ad8c-106">Parameters</span></span>

 <span data-ttu-id="7ad8c-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="7ad8c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7ad8c-108">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="7ad8c-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7ad8c-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="7ad8c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7ad8c-110">возврата Указатель на адрес идентификатора записи открываемой папки или объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="7ad8c-111">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="7ad8c-111">_lpInterface_</span></span>
  
> <span data-ttu-id="7ad8c-112">возврата Указатель на идентификатор интерфейса (IID) для объекта.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="7ad8c-113">Передача значения NULL указывает на то, что объект приводится к стандартному интерфейсу для такого объекта.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="7ad8c-114">Для параметра _лпинтерфаце_ также можно задать идентификатор для соответствующего интерфейса для объекта.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="7ad8c-115">_Улопенфлагс_</span><span class="sxs-lookup"><span data-stu-id="7ad8c-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="7ad8c-116">возврата Битовая маска флагов, определяющих способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="7ad8c-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7ad8c-117">The following flags can be set:</span></span>
    
<span data-ttu-id="7ad8c-118">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="7ad8c-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="7ad8c-119">Объект должен быть открыт с максимальными разрешениями, разрешенными для пользователя и максимальными разрешениями клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="7ad8c-120">Например, если у клиента есть разрешение на чтение и запись, объект открывается с разрешением на чтение и запись; Если клиент имеет разрешение только на чтение, объект открывается с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="7ad8c-121">Клиент может получить уровень разрешений, получив свойство **пр_акцесс_левел** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7ad8c-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="7ad8c-122">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="7ad8c-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7ad8c-123">Вызов может быть выполнен, даже если базовый объект недоступен для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="7ad8c-124">Если объект недоступен, последующий вызов объекта может вернуть ошибку.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="7ad8c-125">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="7ad8c-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7ad8c-126">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-126">Requests read/write permission.</span></span> <span data-ttu-id="7ad8c-127">По умолчанию объекты создаются с разрешением только для чтения, и клиенты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="7ad8c-128">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="7ad8c-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="7ad8c-129">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="7ad8c-130">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="7ad8c-130">_lppUnk_</span></span>
  
> <span data-ttu-id="7ad8c-131">вышли Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ad8c-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ad8c-132">Return value</span></span>

<span data-ttu-id="7ad8c-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ad8c-133">S_OK</span></span> 
  
> <span data-ttu-id="7ad8c-134">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ad8c-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ad8c-135">Remarks</span></span>

<span data-ttu-id="7ad8c-136">MAPI вызывает метод **имслогон:: OpenEntry** для открытия папки или сообщения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="7ad8c-137">MAPI передает идентификатор записи объекта, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="7ad8c-138">Поставщик хранилища сообщений должен возвратить указатель, который обеспечивает дальнейший доступ к объекту, указанному в параметре _лппунк_ .</span><span class="sxs-lookup"><span data-stu-id="7ad8c-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="7ad8c-139">Перед вызовом MAPI **имслогон:: OpenEntry**, он сначала определяет, что указанный идентификатор записи сообщения или папки соответствует одному из зарегистрированных поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="7ad8c-140">Дополнительные сведения о том, как поставщики хранилищ регистрируют идентификаторы записей, можно найти в статье [имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="7ad8c-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="7ad8c-141">**Имслогон:: OpenEntry** идентичен методу [IMsgStore:: OpenEntry](imsgstore-openentry.md) объекта хранилища сообщений, за исключением того, что клиент не вызывает **имслогон:: OpenEntry**; MAPI вызывает **имслогон:: OpenEntry** при обработке метода **IMAPISession:: OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="7ad8c-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="7ad8c-142">Объекты, открытые с помощью **имслогон:: OpenEntry** должны обрабатываться точно так же, как объекты, открытые с помощью объекта хранилища сообщений; в частности, объекты, открытые с помощью этого вызова, следует сделать недействительными при отпускании объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ad8c-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ad8c-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7ad8c-143">See also</span></span>



[<span data-ttu-id="7ad8c-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="7ad8c-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="7ad8c-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7ad8c-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="7ad8c-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ad8c-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

