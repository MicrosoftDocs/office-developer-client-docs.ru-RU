---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415273"
---
# <a name="entryid"></a><span data-ttu-id="2da98-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2da98-103">ENTRYID</span></span>

  
  
<span data-ttu-id="2da98-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2da98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2da98-105">Содержит идентификатор записи для объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="2da98-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2da98-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2da98-106">Header file:</span></span>  <br/> |<span data-ttu-id="2da98-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2da98-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2da98-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="2da98-108">Related macros:</span></span>  <br/> |<span data-ttu-id="2da98-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="2da98-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="2da98-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="2da98-110">Members</span></span>

 <span data-ttu-id="2da98-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="2da98-111">**abFlags**</span></span>
  
> <span data-ttu-id="2da98-112">Битоваяmas флагов, которые предоставляют сведения, описывая объект.</span><span class="sxs-lookup"><span data-stu-id="2da98-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="2da98-113">Поставщик может установить только первый byte из флагов, **abFlags[0]**; остальные три зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="2da98-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="2da98-114">Эти флаги не должны устанавливаться для постоянных идентификаторов записей; они устанавливаются только для краткосрочных идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="2da98-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="2da98-115">Для клиентов эта структура является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2da98-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="2da98-116">Следующие флаги можно установить в **abFlags[0]**:</span><span class="sxs-lookup"><span data-stu-id="2da98-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="2da98-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="2da98-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="2da98-118">Идентификатор записи нельзя использовать в качестве получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="2da98-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="2da98-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="2da98-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="2da98-120">Другие пользователи не могут получить доступ к идентификатору записи.</span><span class="sxs-lookup"><span data-stu-id="2da98-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="2da98-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="2da98-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="2da98-122">Идентификатор записи нельзя использовать в другое время.</span><span class="sxs-lookup"><span data-stu-id="2da98-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="2da98-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="2da98-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="2da98-124">Идентификатор записи является краткосрочным.</span><span class="sxs-lookup"><span data-stu-id="2da98-124">The entry identifier is short-term.</span></span> <span data-ttu-id="2da98-125">Все остальные значения в этом byte необходимо устанавливать, если не включено другое использование идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="2da98-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="2da98-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="2da98-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="2da98-127">Идентификатор записи нельзя использовать в других сеансах.</span><span class="sxs-lookup"><span data-stu-id="2da98-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="2da98-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="2da98-128">**ab**</span></span>
  
> <span data-ttu-id="2da98-129">Указывает массив двоичных данных, используемый поставщиками служб.</span><span class="sxs-lookup"><span data-stu-id="2da98-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="2da98-130">Клиентские приложения не могут использовать этот массив.</span><span class="sxs-lookup"><span data-stu-id="2da98-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2da98-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="2da98-131">Remarks</span></span>

<span data-ttu-id="2da98-132">Структура **ENTRYID** используется поставщиками хранения сообщений и адресных книг для создания уникальных идентификаторов объектов.</span><span class="sxs-lookup"><span data-stu-id="2da98-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="2da98-133">Идентификаторы записей используются для идентификации следующих типов объектов:</span><span class="sxs-lookup"><span data-stu-id="2da98-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="2da98-134">Хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="2da98-134">Message stores</span></span>
    
- <span data-ttu-id="2da98-135">Folders</span><span class="sxs-lookup"><span data-stu-id="2da98-135">Folders</span></span>
    
- <span data-ttu-id="2da98-136">Сообщения</span><span class="sxs-lookup"><span data-stu-id="2da98-136">Messages</span></span>
    
- <span data-ttu-id="2da98-137">Контейнеры адресной книги</span><span class="sxs-lookup"><span data-stu-id="2da98-137">Address book containers</span></span>
    
- <span data-ttu-id="2da98-138">Списки рассылки</span><span class="sxs-lookup"><span data-stu-id="2da98-138">Distribution lists</span></span>
    
- <span data-ttu-id="2da98-139">Пользователи сообщений</span><span class="sxs-lookup"><span data-stu-id="2da98-139">Messaging users</span></span>
    
- <span data-ttu-id="2da98-140">Объекты состояний</span><span class="sxs-lookup"><span data-stu-id="2da98-140">Status objects</span></span>
    
- <span data-ttu-id="2da98-141">Разделы профиля</span><span class="sxs-lookup"><span data-stu-id="2da98-141">Profile sections</span></span>
    
<span data-ttu-id="2da98-142">Каждый поставщик использует формат структуры **ENTRYID,** который имеет смысл для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="2da98-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="2da98-143">Идентификаторы записей нельзя сравнить напрямую, так как один объект может быть представлен двумя разными двоичными значениями.</span><span class="sxs-lookup"><span data-stu-id="2da98-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="2da98-144">Чтобы определить, представляют ли два идентификатора записи один и тот же объект, вызовите метод [IMAPISession::CompareEntryIDs.](imapisession-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="2da98-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="2da98-145">Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) объекта для получения его идентификатора записи, объект возвращает самую постоянную форму идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="2da98-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="2da98-146">Клиент может проверить, является ли идентификатор записи долгосрочным, проверив, что ни один из флагов не установлен в первом byte члена **abFlags.**</span><span class="sxs-lookup"><span data-stu-id="2da98-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="2da98-147">Когда клиент получает доступ к идентификатору записи через столбец в таблице, скорее всего, этот идентификатор записи является краткосрочным, а не долгосрочным.</span><span class="sxs-lookup"><span data-stu-id="2da98-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="2da98-148">Краткосрочные идентификаторы записей можно использовать для открытия соответствующих объектов только в текущем сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="2da98-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="2da98-149">Клиент может проверить, является ли идентификатор записи краткосрочным, проверив, установлены ли все флаги в первом byte члена **abFlags.**</span><span class="sxs-lookup"><span data-stu-id="2da98-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="2da98-150">Некоторые идентификаторы записей являются краткосрочными, но используются в долгосрочной перспективе.</span><span class="sxs-lookup"><span data-stu-id="2da98-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="2da98-151">Такой идентификатор записи будет иметь один или несколько из соответствующих флагов, установленных в первом byte члена **abFlags.**</span><span class="sxs-lookup"><span data-stu-id="2da98-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="2da98-152">Структура **ENTRYID** напоминает [структуру FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="2da98-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="2da98-153">Однако существуют некоторые различия:</span><span class="sxs-lookup"><span data-stu-id="2da98-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="2da98-154">В **структуре ENTRYID** не хранится размер идентификатора записи; Структура **FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="2da98-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="2da98-155">В **структуре ENTRYID** данные флага и остальные идентификаторы записей хранится отдельно; Структура **FLATENTRY** хранит данные флага с остальным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="2da98-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="2da98-156">Структура **ENTRYID** передается в качестве параметра в методы интерфейса [IMAPIProp](imapipropiunknown.md) и следующие методы **OpenEntry:** [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="2da98-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="2da98-157">Структура **ENTRYID** используется для хранения идентификатора записи на диске.</span><span class="sxs-lookup"><span data-stu-id="2da98-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="2da98-158">Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке данных.</span><span class="sxs-lookup"><span data-stu-id="2da98-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="2da98-159">Клиенты должны всегда передавать идентификаторы записей, выровненные по естественному.</span><span class="sxs-lookup"><span data-stu-id="2da98-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="2da98-160">Хотя поставщики должны обрабатывать произвольно выровненные идентификаторы записей, клиенты не должны ожидать такого поведения.</span><span class="sxs-lookup"><span data-stu-id="2da98-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="2da98-161">Если не передать методу правильно выровненный идентификатор записи, это может привести к сбою выравнивания процессоров RISC.</span><span class="sxs-lookup"><span data-stu-id="2da98-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="2da98-162">Коэффициент естественного выравнивания( обычно 8 т) — это самый большой тип данных, поддерживаемый ЦП, и обычно это тот же коэффициент выравнивания, который используется в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="2da98-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="2da98-163">Естественно выровненный адрес памяти позволяет ЦП получать доступ к любому типу данных, который он поддерживает по этому адресу, без сбоя выравнивания.</span><span class="sxs-lookup"><span data-stu-id="2da98-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="2da98-164">Для ЦП RISC тип данных размера N обычно должен быть выровнен по четным кратным размерам N, при этом адрес может быть даже кратным N.</span><span class="sxs-lookup"><span data-stu-id="2da98-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="2da98-165">Дополнительные сведения [см. в документе "Идентификаторы записей".](mapi-entry-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2da98-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2da98-166">См. также</span><span class="sxs-lookup"><span data-stu-id="2da98-166">See also</span></span>



[<span data-ttu-id="2da98-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="2da98-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="2da98-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2da98-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="2da98-169">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="2da98-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="2da98-170">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="2da98-170">MAPI Structures</span></span>](mapi-structures.md)

