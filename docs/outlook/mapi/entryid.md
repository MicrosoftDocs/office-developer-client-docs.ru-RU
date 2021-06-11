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
# <a name="entryid"></a><span data-ttu-id="b92d1-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b92d1-103">ENTRYID</span></span>

  
  
<span data-ttu-id="b92d1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b92d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b92d1-105">Содержит идентификатор входа для объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="b92d1-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b92d1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b92d1-106">Header file:</span></span>  <br/> |<span data-ttu-id="b92d1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b92d1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b92d1-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="b92d1-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b92d1-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="b92d1-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="b92d1-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="b92d1-110">Members</span></span>

 <span data-ttu-id="b92d1-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="b92d1-111">**abFlags**</span></span>
  
> <span data-ttu-id="b92d1-112">Bitmask флагов, которые предоставляют информацию, которая описывает объект.</span><span class="sxs-lookup"><span data-stu-id="b92d1-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="b92d1-113">Поставщик может установить только первый набор **флагов, abFlags[0];** остальные три зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="b92d1-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="b92d1-114">Эти флаги не должны устанавливаться для идентификаторов постоянных записей; они устанавливаются только для краткосрочных идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="b92d1-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="b92d1-115">Для клиентов эта структура является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b92d1-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="b92d1-116">Следующие флаги можно установить в **abFlags[0]**:</span><span class="sxs-lookup"><span data-stu-id="b92d1-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="b92d1-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="b92d1-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="b92d1-118">Идентификатор записи не может использоваться в качестве получателя в сообщении.</span><span class="sxs-lookup"><span data-stu-id="b92d1-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="b92d1-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="b92d1-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="b92d1-120">Другие пользователи не могут получить доступ к идентификатору записи.</span><span class="sxs-lookup"><span data-stu-id="b92d1-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="b92d1-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="b92d1-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="b92d1-122">Идентификатор записи не может использоваться в другое время.</span><span class="sxs-lookup"><span data-stu-id="b92d1-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="b92d1-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="b92d1-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="b92d1-124">Идентификатор записи является краткосрочным.</span><span class="sxs-lookup"><span data-stu-id="b92d1-124">The entry identifier is short-term.</span></span> <span data-ttu-id="b92d1-125">Все другие значения в этом byte должны быть заданной, если не включено другое использование идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="b92d1-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="b92d1-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="b92d1-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="b92d1-127">Идентификатор записи нельзя использовать на других сеансах.</span><span class="sxs-lookup"><span data-stu-id="b92d1-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="b92d1-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="b92d1-128">**ab**</span></span>
  
> <span data-ttu-id="b92d1-129">Указывает массив двоичных данных, используемых поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="b92d1-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="b92d1-130">Клиентские приложения не могут использовать этот массив.</span><span class="sxs-lookup"><span data-stu-id="b92d1-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b92d1-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="b92d1-131">Remarks</span></span>

<span data-ttu-id="b92d1-132">Структура **ENTRYID** используется поставщиками сообщений и адресных книг для создания уникальных идентификаторов для своих объектов.</span><span class="sxs-lookup"><span data-stu-id="b92d1-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="b92d1-133">Идентификаторы записей используются для определения следующих типов объектов:</span><span class="sxs-lookup"><span data-stu-id="b92d1-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="b92d1-134">Хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="b92d1-134">Message stores</span></span>
    
- <span data-ttu-id="b92d1-135">Folders</span><span class="sxs-lookup"><span data-stu-id="b92d1-135">Folders</span></span>
    
- <span data-ttu-id="b92d1-136">Сообщения</span><span class="sxs-lookup"><span data-stu-id="b92d1-136">Messages</span></span>
    
- <span data-ttu-id="b92d1-137">Контейнеры адресной книги</span><span class="sxs-lookup"><span data-stu-id="b92d1-137">Address book containers</span></span>
    
- <span data-ttu-id="b92d1-138">Списки рассылки</span><span class="sxs-lookup"><span data-stu-id="b92d1-138">Distribution lists</span></span>
    
- <span data-ttu-id="b92d1-139">Пользователи обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="b92d1-139">Messaging users</span></span>
    
- <span data-ttu-id="b92d1-140">Объекты состояний</span><span class="sxs-lookup"><span data-stu-id="b92d1-140">Status objects</span></span>
    
- <span data-ttu-id="b92d1-141">Разделы профилей</span><span class="sxs-lookup"><span data-stu-id="b92d1-141">Profile sections</span></span>
    
<span data-ttu-id="b92d1-142">Каждый поставщик использует формат **структуры ENTRYID,** который имеет смысл для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="b92d1-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="b92d1-143">Идентификаторы записи нельзя сравнивать напрямую, так как один объект может быть представлен двумя разными двоичными значениями.</span><span class="sxs-lookup"><span data-stu-id="b92d1-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="b92d1-144">Чтобы определить, представляют ли два идентификатора записи один и тот же объект, позвоните по методу [IMAPISession::CompareEntryIDs.](imapisession-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="b92d1-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="b92d1-145">Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) объекта для получения его идентификатора входа, объект возвращает самую постоянную форму идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="b92d1-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="b92d1-146">Клиент может убедиться, что идентификатор записи является долгосрочным, проверяя, что ни один из флагов не установлен в первой части **участника abFlags.**</span><span class="sxs-lookup"><span data-stu-id="b92d1-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="b92d1-147">Если клиент получает доступ к идентификатору записи через столбец в таблице, скорее всего, этот идентификатор записи является краткосрочным, а не долгосрочным.</span><span class="sxs-lookup"><span data-stu-id="b92d1-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="b92d1-148">Краткосрочные идентификаторы записи можно использовать для открытия соответствующих объектов только в текущем сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="b92d1-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="b92d1-149">Клиент может убедиться, что идентификатор записи является краткосрочным, проверяя, что все флаги задают в первой части **участника abFlags.**</span><span class="sxs-lookup"><span data-stu-id="b92d1-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="b92d1-150">Некоторые идентификаторы записей являются краткосрочными, но имеют долгосрочное использование.</span><span class="sxs-lookup"><span data-stu-id="b92d1-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="b92d1-151">Такой идентификатор записи будет иметь один или несколько соответствующих флагов, установленных в первом byte своего **члена abFlags.**</span><span class="sxs-lookup"><span data-stu-id="b92d1-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="b92d1-152">Структура **ENTRYID** напоминает структуру [FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="b92d1-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="b92d1-153">Однако существуют некоторые различия:</span><span class="sxs-lookup"><span data-stu-id="b92d1-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="b92d1-154">Структура **ENTRYID** не сохраняет размер идентификатора записи; структура **FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="b92d1-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="b92d1-155">Структура **ENTRYID** хранит данные флага и остальные идентификаторы входа отдельно; структура **FLATENTRY** хранит данные флага с остальным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="b92d1-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="b92d1-156">Структура **ENTRYID** передается в качестве параметра методам интерфейса [IMAPIProp](imapipropiunknown.md) и следующим методам **OpenEntry:** [IABLogon::OpenEntry,](iablogon-openentry.md) [IAddrBook::OpenEntry,](iaddrbook-openentry.md) [IMAPIContainer::OpenEntry,](imapicontainer-openentry.md) [IMAPISession::OpenEntry,](imapisession-openentry.md) [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon:OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="b92d1-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="b92d1-157">Структура **ENTRYID** используется для хранения идентификатора записи на диске.</span><span class="sxs-lookup"><span data-stu-id="b92d1-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="b92d1-158">Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке bytes.</span><span class="sxs-lookup"><span data-stu-id="b92d1-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="b92d1-159">Клиенты всегда должны проходить в естественно выровненных идентификаторах записей.</span><span class="sxs-lookup"><span data-stu-id="b92d1-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="b92d1-160">Хотя поставщики должны обрабатывать произвольно выровненные идентификаторы записей, клиенты не должны ожидать такого поведения.</span><span class="sxs-lookup"><span data-stu-id="b92d1-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="b92d1-161">Невыполнение правильного идентификатора входа в метод может привести к сбою выравнивания на процессорах RISC.</span><span class="sxs-lookup"><span data-stu-id="b92d1-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="b92d1-162">Естественный коэффициент выравнивания, обычно 8 bytes, это самый большой тип данных, поддерживаемый ЦП, и, как правило, тот же фактор выравнивания, используемый в системе памяти.</span><span class="sxs-lookup"><span data-stu-id="b92d1-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="b92d1-163">Естественно выровненный адрес памяти позволяет ЦП получать доступ к любому типу данных, который он поддерживает по этому адресу, без создания ошибки выравнивания.</span><span class="sxs-lookup"><span data-stu-id="b92d1-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="b92d1-164">Для ЦП RISC тип данных размером N-bytes обычно должен выравниваться по даже нескольким N-bytes, при этом адрес является даже нескольким N.</span><span class="sxs-lookup"><span data-stu-id="b92d1-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="b92d1-165">Дополнительные сведения см. в [документе Entry Identifiers](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b92d1-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b92d1-166">См. также</span><span class="sxs-lookup"><span data-stu-id="b92d1-166">See also</span></span>



[<span data-ttu-id="b92d1-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="b92d1-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="b92d1-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="b92d1-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="b92d1-169">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="b92d1-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="b92d1-170">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b92d1-170">MAPI Structures</span></span>](mapi-structures.md)

