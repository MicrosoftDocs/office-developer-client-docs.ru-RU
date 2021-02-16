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
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416302"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="ddbbc-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ddbbc-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="ddbbc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddbbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddbbc-105">Открывает папку или объект сообщения и возвращает указатель на объект для обеспечения дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="ddbbc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddbbc-106">Parameters</span></span>

 <span data-ttu-id="ddbbc-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ddbbc-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ddbbc-108">[in] Размер идентификатора записи в вайтах, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ddbbc-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ddbbc-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ddbbc-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ddbbc-110">[in] Указатель на адрес идентификатора записи открываемой папки или объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="ddbbc-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ddbbc-111">_lpInterface_</span></span>
  
> <span data-ttu-id="ddbbc-112">[in] Указатель на идентификатор интерфейса (IID) для объекта.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="ddbbc-113">Передача NULL означает, что объект передается в стандартный интерфейс для такого объекта.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="ddbbc-114">Параметр  _lpInterface_ также может быть задан в качестве идентификатора для соответствующего интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="ddbbc-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="ddbbc-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="ddbbc-116">[in] Битоваяmas флагов, которая управляет открытием объекта.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="ddbbc-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ddbbc-117">The following flags can be set:</span></span>
    
<span data-ttu-id="ddbbc-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ddbbc-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="ddbbc-119">Объект должен быть открыт с максимальным количеством разрешений, разрешенных для пользователя, и максимальным разрешением клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="ddbbc-120">Например, если у клиента есть разрешение на чтение и записи, объект открывается с разрешением на чтение и записи; если у клиента есть разрешение только для чтения, объект открывается с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="ddbbc-121">Клиент может получить уровень разрешений, получив **свойство PR_ACCESS_LEVEL** ([PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ddbbc-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="ddbbc-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ddbbc-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ddbbc-123">Вызов может быть успешным даже в том случае, если его объект недопустим для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="ddbbc-124">Если объект не доступен, последующий вызов объекта может вернуть ошибку.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="ddbbc-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ddbbc-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ddbbc-126">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-126">Requests read/write permission.</span></span> <span data-ttu-id="ddbbc-127">По умолчанию объекты создаются с разрешением только для чтения, и клиенты не должны работать при предположении, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="ddbbc-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="ddbbc-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="ddbbc-129">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="ddbbc-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="ddbbc-130">_lppUnk_</span></span>
  
> <span data-ttu-id="ddbbc-131">[out] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ddbbc-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddbbc-132">Return value</span></span>

<span data-ttu-id="ddbbc-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="ddbbc-133">S_OK</span></span> 
  
> <span data-ttu-id="ddbbc-134">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ddbbc-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="ddbbc-135">Remarks</span></span>

<span data-ttu-id="ddbbc-136">MAPI вызывает метод **IMSLogon::OpenEntry,** чтобы открыть папку или сообщение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="ddbbc-137">MAPI передает идентификатор записи объекта для открытия.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="ddbbc-138">Поставщик параметров хранения сообщений должен вернуть указатель, который обеспечивает дальнейший доступ к объекту, указанному в параметре _lppUnk._</span><span class="sxs-lookup"><span data-stu-id="ddbbc-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="ddbbc-139">Перед вызовом **СЛУЖБЫ MAPI IMSLogon::OpenEntry** сначала определяется, что заданный идентификатор записи сообщения или папки соответствует идентификатору, зарегистрированного этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="ddbbc-140">Дополнительные сведения о регистрации идентификаторов записей поставщиками магазина см. в документе [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="ddbbc-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="ddbbc-141">**IMSLogon::OpenEntry** идентичен методу [IMsgStore::OpenEntry](imsgstore-openentry.md) объекта хранилище сообщений, за исключением того, что клиент не вызвать **IMSLogon::OpenEntry;** MAPI вызывает **IMSLogon::OpenEntry** при обработке метода **IMAPISession::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="ddbbc-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="ddbbc-142">Объекты, открытые с помощью **IMSLogon::OpenEntry,** должны рассматриваться точно так же, как объекты, открытые с помощью объекта хранения сообщений; в частности, объекты, открытые с помощью этого вызова, должны быть признаны недействительными при освобождения объекта хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="ddbbc-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddbbc-143">См. также</span><span class="sxs-lookup"><span data-stu-id="ddbbc-143">See also</span></span>



[<span data-ttu-id="ddbbc-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="ddbbc-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="ddbbc-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ddbbc-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="ddbbc-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ddbbc-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

