---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 65d633f0c2b0ce56793eaa55a417b5d6a816d449
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589849"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="d8b0b-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="d8b0b-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="d8b0b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8b0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8b0b-105">Возвращает типы получателей, которые обрабатывают поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="d8b0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8b0b-106">Parameters</span></span>

 <span data-ttu-id="d8b0b-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8b0b-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="d8b0b-108">[out] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d8b0b-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d8b0b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d8b0b-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8b0b-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d8b0b-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="d8b0b-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d8b0b-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="d8b0b-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="d8b0b-114">[out] Указатель на число записей в массиве указывает параметр _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="d8b0b-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="d8b0b-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="d8b0b-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="d8b0b-116">[out] Указатель на указатель на массив строк, чтобы указать типы получателей.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="d8b0b-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="d8b0b-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="d8b0b-118">[out] Указатель на число записей в массиве указывает параметр _lpppUIDArray_ .</span><span class="sxs-lookup"><span data-stu-id="d8b0b-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="d8b0b-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="d8b0b-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="d8b0b-120">[out] Указатель на указатель на массив указатели на [MAPIUID](mapiuid.md) структуры, чтобы указать типы получателей.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8b0b-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d8b0b-121">Return value</span></span>

<span data-ttu-id="d8b0b-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d8b0b-122">S_OK</span></span> 
  
> <span data-ttu-id="d8b0b-123">Поставщика транспорта успешно Указывает типы получателей, которые можно обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="d8b0b-124">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d8b0b-124">Notes to implementers</span></span>

<span data-ttu-id="d8b0b-125">Диспетчер очереди MAPI вызывает метод **IXPLogon::AddressTypes** сразу же после возвращает поставщика транспорта в вызове метода [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) , поставщика транспорта можно указать, какие типы получателей обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="d8b0b-126">Чтобы указать это, поставщика транспорта следует передать обратно в параметре _lpppszAdrTypeArray_ указатель на массив указатели на строки или передайте в параметре _lpppUIDArray_ указатель массив указатели на **MAPIUID** структуры или передавать значения в оба параметра.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="d8b0b-127">Эти два массива используются для идентификации различных процессов.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="d8b0b-128">MAPI и диспетчер очереди MAPI структур [MAPIUID](mapiuid.md) в массиве _lpppUIDArray_ для определения используют эти идентификаторы получателей записей, которые обрабатываются непосредственно с поставщика транспорта или системы обмена сообщениями, к которому подключается поставщика транспорта .</span><span class="sxs-lookup"><span data-stu-id="d8b0b-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="d8b0b-129">Диспетчер очереди MAPI ни MAPI расширяет адреса с помощью идентификаторы записей, содержащихся в любой из этих структур **MAPIUID** ; Эти структуры используются только для определения типа получателя.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="d8b0b-130">Диспетчер очереди MAPI использует каждый из строки с помощью параметра _lpppszAdrTypeArray_ для тестирования сравнения при определяет, какие поставщика транспорта должен обрабатывать получателей для исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="d8b0b-131">Если свойство **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) получателя сообщения в точности соответствует строка, определяющая один из системы обмена сообщениями типов адресов, которые предоставляет поставщика транспорта, поставщик можно доставить сообщение для получателя.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="d8b0b-132">Если несколько поставщиков транспорта может обрабатывать тот же тип получателя, MAPI выбирает поставщика транспорта в порядке приоритета транспорта указано в профиле клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="d8b0b-133">Чтобы определить, используемого поставщика транспорта, диспетчер очереди MAPI сканирование всех указан поставщик структур **MAPIUID** в порядке приоритета и затем все адреса указанного поставщика тип значения в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="d8b0b-134">Первый поставщика транспорта в соответствии с определенного получателя в для этого сканирования получает возможность первым обработать данному получателю.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="d8b0b-135">Если этого поставщика не обрабатывает получателя, диспетчер очереди MAPI по-прежнему производится сканирование для поиска поставщика транспорта для получателя, еще не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="d8b0b-136">Сканирование продолжается, пока не дальнейший дал, после чего для какого-либо получателя, которое не было обработано создается отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="d8b0b-137">Если поставщик поддерживает всегда определенный набор типов получателей, тип адреса и массивов **MAPIUID** , которые переданы поставщика транспорта может быть static.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="d8b0b-138">Если поставщик транспорта динамически создает эти массивы, его выделения памяти с помощью объекта поддержки, который ранее был передан в вызове **TransportLogon**, хотя это не требуется.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="d8b0b-139">Объем памяти, используемый для типа адреса и массивов **MAPIUID** должны оставаться выделенный до окончательного вызова метода [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) , в этот момент поставщика транспорта можно освободить память, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="d8b0b-140">Поставщика транспорта не следует изменить содержимое этих массивов после возврата из вызова **TransportLogoff** .</span><span class="sxs-lookup"><span data-stu-id="d8b0b-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="d8b0b-141">Поставщик транспорта, который может обрабатывать любой тип получателя может возвращать NULL в параметре _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="d8b0b-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="d8b0b-142">Поставщики транспорта для локальных систем обмена сообщениями, использующих центральный сервер для передачи исходящих сообщений на различных систем внешнего сообщения часто это сделать.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="d8b0b-143">Этот тип поставщика транспорта должны быть установлены последние в MAPI и MAPI приоритетности очереди транспорта поставщиков в профиле.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="d8b0b-144">Поставщик транспорта, не поддерживает исходящих сообщений, отправляемых на него на основе типа адреса должна вернуть одну строку нулевой длины в _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="d8b0b-145">Если поставщик транспорта поддерживает не типы получателей, ему следует передать значение NULL для структуры **MAPIUID** и пустая строка для типа адреса.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="d8b0b-146">Поставщики транспорта этого типа чаще всего используются для установки препроцессор сообщения.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8b0b-147">См. также</span><span class="sxs-lookup"><span data-stu-id="d8b0b-147">See also</span></span>



[<span data-ttu-id="d8b0b-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="d8b0b-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="d8b0b-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="d8b0b-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="d8b0b-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d8b0b-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d8b0b-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8b0b-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

