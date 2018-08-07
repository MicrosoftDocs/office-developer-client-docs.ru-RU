---
title: IMSLogonOpenEntry
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
ms.openlocfilehash: e9d9ca56a877c0106c76242fe97ce43321e62e08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809427"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="91a2c-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="91a2c-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="91a2c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91a2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91a2c-105">Открывает папку или объект сообщения и возвращает указатель на объект для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="91a2c-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="91a2c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91a2c-106">Parameters</span></span>

 <span data-ttu-id="91a2c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="91a2c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="91a2c-108">[in] Размер в байтах, идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="91a2c-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="91a2c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="91a2c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="91a2c-110">[in] Указатель на адрес идентификатор записи объекта папки или сообщения, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="91a2c-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="91a2c-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="91a2c-111">_lpInterface_</span></span>
  
> <span data-ttu-id="91a2c-112">[in] Указатель на интерфейс идентификатор (ИД интерфейса) для объекта.</span><span class="sxs-lookup"><span data-stu-id="91a2c-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="91a2c-113">Передача NULL означает, что объект приводится стандартный интерфейс для таких объектов.</span><span class="sxs-lookup"><span data-stu-id="91a2c-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="91a2c-114">Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="91a2c-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="91a2c-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="91a2c-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="91a2c-116">[in] Битовая маска флаги, который определяет способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="91a2c-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="91a2c-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="91a2c-117">The following flags can be set:</span></span>
    
<span data-ttu-id="91a2c-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="91a2c-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="91a2c-119">Объект должен быть открыт максимального разрешения для пользователя и разрешения максимальное клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="91a2c-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="91a2c-120">Например если клиент имеет разрешение на чтение и запись, объект открывается с разрешение на чтение и запись. Если клиент имеет разрешение только на чтение, объект открыт с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91a2c-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="91a2c-121">Уровень разрешений можно получить путем получения свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91a2c-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="91a2c-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="91a2c-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="91a2c-123">Разрешено для успешного выполнения даже в том случае, если базовый объект недоступен вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="91a2c-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="91a2c-124">Если объект недоступен, следующий вызов объекта может возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="91a2c-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="91a2c-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="91a2c-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="91a2c-126">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="91a2c-126">Requests read/write permission.</span></span> <span data-ttu-id="91a2c-127">По умолчанию объекты создаются с разрешением только для чтения, и клиенты не должны работать предполагается, что чтение и запись, назначено разрешение.</span><span class="sxs-lookup"><span data-stu-id="91a2c-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="91a2c-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="91a2c-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="91a2c-129">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="91a2c-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="91a2c-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="91a2c-130">_lppUnk_</span></span>
  
> <span data-ttu-id="91a2c-131">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="91a2c-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91a2c-132">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="91a2c-132">Return value</span></span>

<span data-ttu-id="91a2c-133">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="91a2c-133">S_OK</span></span> 
  
> <span data-ttu-id="91a2c-134">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="91a2c-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91a2c-135">���������</span><span class="sxs-lookup"><span data-stu-id="91a2c-135">Remarks</span></span>

<span data-ttu-id="91a2c-136">MAPI вызывает метод **IMSLogon::OpenEntry** , чтобы открыть папку или сообщение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="91a2c-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="91a2c-137">Идентификатор записи объекта, чтобы открыть передает MAPI.</span><span class="sxs-lookup"><span data-stu-id="91a2c-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="91a2c-138">Поставщик хранения сообщений должен возвращать указатель, который позволяет дальнейший доступ к объекту, указанный в параметре _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="91a2c-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="91a2c-139">Прежде чем MAPI вызывает **IMSLogon::OpenEntry**, сначала определяет, что данное сообщение или идентификатор записи папки соответствует одной зарегистрированные этим поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="91a2c-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="91a2c-140">Дополнительные сведения о как зарегистрировать поставщиков хранилища идентификаторы записей можно [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="91a2c-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="91a2c-141">**IMSLogon::OpenEntry** идентичен методу [IMsgStore::OpenEntry](imsgstore-openentry.md) объекта хранилища сообщений, за исключением того, что клиент не вызывает **IMSLogon::OpenEntry**; MAPI вызывает **IMSLogon::OpenEntry** при обработке методом **IMAPISession::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="91a2c-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="91a2c-142">Будет открыто с помощью **IMSLogon::OpenEntry** объекты обрабатываются точно так же, как объекты открыто с помощью сообщения хранилищ объекта; в частности объектов открыто с помощью этого вызова должна недействительным после выхода объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="91a2c-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91a2c-143">См. также</span><span class="sxs-lookup"><span data-stu-id="91a2c-143">See also</span></span>



[<span data-ttu-id="91a2c-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="91a2c-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="91a2c-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="91a2c-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="91a2c-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91a2c-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

