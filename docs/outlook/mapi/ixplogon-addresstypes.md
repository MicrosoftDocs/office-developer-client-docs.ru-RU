---
title: Иксплогонаддресстипес
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
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435378"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="65c84-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="65c84-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="65c84-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65c84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65c84-105">Возвращает типы получателей, которые обрабатывает поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="65c84-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="65c84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="65c84-106">Parameters</span></span>

 <span data-ttu-id="65c84-107">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="65c84-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="65c84-108">вышли Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="65c84-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="65c84-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="65c84-109">The following flag can be set:</span></span>
    
<span data-ttu-id="65c84-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="65c84-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="65c84-111">Возвращаемые строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="65c84-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="65c84-112">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="65c84-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="65c84-113">_Лпкадртипе_</span><span class="sxs-lookup"><span data-stu-id="65c84-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="65c84-114">вышли Указатель на число записей в массиве, на которое указывает параметр _лпппсзадртипеаррай_ .</span><span class="sxs-lookup"><span data-stu-id="65c84-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="65c84-115">_Лпппсзадртипеаррай_</span><span class="sxs-lookup"><span data-stu-id="65c84-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="65c84-116">вышли Указатель на указатель на массив строк, который определяет типы получателей.</span><span class="sxs-lookup"><span data-stu-id="65c84-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="65c84-117">_Лпкмапиуид_</span><span class="sxs-lookup"><span data-stu-id="65c84-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="65c84-118">вышли Указатель на число записей в массиве, на которое указывает параметр _лпппуидаррай_ .</span><span class="sxs-lookup"><span data-stu-id="65c84-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="65c84-119">_Лпппуидаррай_</span><span class="sxs-lookup"><span data-stu-id="65c84-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="65c84-120">вышли Указатель на указатель на массив указателей на структуры [мапиуид](mapiuid.md) , которые определяют типы получателей.</span><span class="sxs-lookup"><span data-stu-id="65c84-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="65c84-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65c84-121">Return value</span></span>

<span data-ttu-id="65c84-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="65c84-122">S_OK</span></span> 
  
> <span data-ttu-id="65c84-123">Поставщик транспорта успешно указал типы получателей, которые он может обработать.</span><span class="sxs-lookup"><span data-stu-id="65c84-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="65c84-124">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="65c84-124">Notes to implementers</span></span>

<span data-ttu-id="65c84-125">Диспетчер очереди MAPI вызывает метод **иксплогон:: аддресстипес** сразу после того, как поставщик транспорта возвращает вызов метода [Иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) , чтобы поставщик транспорта мог указать, какие типы получателей он обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="65c84-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="65c84-126">Чтобы обозначить это, поставщик транспорта должен передать параметру _лпппсзадртипеаррай_ указатель на массив указателей на строки или передать обратно в параметре _лпппуидаррай_ указатель на массив указателей на **мапиуид** структуры или передавать значения в обоих параметрах.</span><span class="sxs-lookup"><span data-stu-id="65c84-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="65c84-127">Эти два массива используются для различных процессов идентификации.</span><span class="sxs-lookup"><span data-stu-id="65c84-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="65c84-128">MAPI и Диспетчер очереди MAPI используют структуры [мапиуид](mapiuid.md) в массиве _лпппуидаррай_ , чтобы определить идентификаторы записей получателей, которые непосредственно обрабатываются поставщиком транспорта или системой обмена сообщениями, к которой подключается поставщик транспорта. .</span><span class="sxs-lookup"><span data-stu-id="65c84-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="65c84-129">Ни MAPI, ни Диспетчер очереди MAPI не разворачивает адреса с помощью идентификаторов записей, которые хранятся в любой из этих структур **мапиуид** ; Эти структуры используются только для идентификации типа получателя.</span><span class="sxs-lookup"><span data-stu-id="65c84-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="65c84-130">При выборе поставщика транспорта, который должен обрабатывать получателей исходящих сообщений, диспетчер очереди MAPI использует каждую строку параметра _лпппсзадртипеаррай_ для проверки сравнения.</span><span class="sxs-lookup"><span data-stu-id="65c84-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="65c84-131">Если свойство **пр_аддртипе** получателя сообщения ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) точно совпадает со строкой, определяющей один из типов адресов обмена сообщениями, предоставленных поставщиком транспорта, поставщик может доставить сообщение этому получателю.</span><span class="sxs-lookup"><span data-stu-id="65c84-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="65c84-132">Если несколько поставщиков транспорта могут обрабатывать один и тот же тип получателя, MAPI выбирает поставщика транспорта на основе заказа приоритета транспорта, указанного в профиле клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="65c84-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="65c84-133">Чтобы определить, какой поставщик транспорта будет использоваться, диспетчер очереди MAPI сканирует все зависящие от поставщика структуры **мапиуид** в порядке приоритета, а затем все значения типа адреса, заданные поставщиком, в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="65c84-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="65c84-134">Первый поставщик транспорта, соответствующий определенному получателю в данном сканировании, получает первую возможность для обработки этого получателя.</span><span class="sxs-lookup"><span data-stu-id="65c84-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="65c84-135">Если этот поставщик не обрабатывает получателя, диспетчер очереди MAPI продолжает сканирование, чтобы найти поставщика транспорта, который еще не обработан.</span><span class="sxs-lookup"><span data-stu-id="65c84-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="65c84-136">Сканирование продолжается до тех пор, пока не будут найдены никакие совпадения, и при этом создается отчет о недоставке для всех получателей, которые не были обработаны.</span><span class="sxs-lookup"><span data-stu-id="65c84-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="65c84-137">Если поставщик всегда поддерживает определенный набор типов получателей, тип адреса и массивы **мапиуид** , передаваемые поставщиком транспорта, могут быть статическими.</span><span class="sxs-lookup"><span data-stu-id="65c84-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="65c84-138">Если поставщик транспорта динамически создает эти массивы, он может выделить память с помощью объекта поддержки, который ранее был передан в вызове **транспортлогон**, хотя это необязательно.</span><span class="sxs-lookup"><span data-stu-id="65c84-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="65c84-139">Память, используемая для массивов типа адреса и **мапиуид** , должна быть выделена до последнего вызова метода [Иксплогон:: транспортлогофф](ixplogon-transportlogoff.md) , когда поставщик транспорта может освободить память, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="65c84-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="65c84-140">Поставщик транспорта не должен изменять содержимое этих массивов после его возврата из вызова **транспортлогофф** .</span><span class="sxs-lookup"><span data-stu-id="65c84-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="65c84-141">Поставщик транспорта, который может обрабатывать любой тип получателя, может возвращать значение NULL в параметре _лпппсзадртипеаррай_ .</span><span class="sxs-lookup"><span data-stu-id="65c84-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="65c84-142">Поставщики транспорта для систем обмена сообщениями на основе ЛВС, использующих центральный сервер для доставки исходящих сообщений в различные системы инородных сообщений, обычно это выполняется.</span><span class="sxs-lookup"><span data-stu-id="65c84-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="65c84-143">Этот тип поставщика транспорта должен быть установлен последним в порядке приоритетов диспетчера очереди MAPI и MAPI в профиле.</span><span class="sxs-lookup"><span data-stu-id="65c84-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="65c84-144">Поставщик транспорта, который не поддерживает исходящие сообщения, отправленные в него на основе типа адреса, должен возвращать одну строку нулевой длины в _лпппсзадртипеаррай_.</span><span class="sxs-lookup"><span data-stu-id="65c84-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="65c84-145">Если поставщик транспорта не поддерживает типы получателей, он должен передать значение NULL для структуры **мапиуид** и пустую строку для типа адреса.</span><span class="sxs-lookup"><span data-stu-id="65c84-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="65c84-146">Поставщики транспорта этого типа чаще всего используются для установки препроцессора сообщений.</span><span class="sxs-lookup"><span data-stu-id="65c84-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65c84-147">См. также</span><span class="sxs-lookup"><span data-stu-id="65c84-147">See also</span></span>



[<span data-ttu-id="65c84-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="65c84-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="65c84-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="65c84-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="65c84-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="65c84-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="65c84-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65c84-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

