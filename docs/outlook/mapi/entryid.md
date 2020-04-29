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
# <a name="entryid"></a><span data-ttu-id="ec092-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ec092-103">ENTRYID</span></span>

  
  
<span data-ttu-id="ec092-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec092-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec092-105">Содержит идентификатор записи для объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="ec092-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec092-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ec092-106">Header file:</span></span>  <br/> |<span data-ttu-id="ec092-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ec092-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ec092-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="ec092-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ec092-109">[Кбневентрид](cbnewentryid.md), [сизедентрид](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="ec092-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="ec092-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="ec092-110">Members</span></span>

 <span data-ttu-id="ec092-111">**абфлагс**</span><span class="sxs-lookup"><span data-stu-id="ec092-111">**abFlags**</span></span>
  
> <span data-ttu-id="ec092-112">Битовая маска флагов, предоставляющих сведения, описывающие объект.</span><span class="sxs-lookup"><span data-stu-id="ec092-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="ec092-113">Поставщик может задать только первый байт флажков, **абфлагс [0]**. остальные три зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="ec092-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="ec092-114">Эти флаги не должны быть установлены для постоянных идентификаторов записей; они задаются только для краткосрочных идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="ec092-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="ec092-115">Для клиентов эта структура доступна только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ec092-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="ec092-116">В **абфлагс [0]** можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ec092-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="ec092-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="ec092-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="ec092-118">Невозможно использовать идентификатор записи в качестве получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="ec092-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="ec092-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="ec092-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="ec092-120">Другие пользователи не могут получить доступ к идентификатору записи.</span><span class="sxs-lookup"><span data-stu-id="ec092-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="ec092-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="ec092-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="ec092-122">Идентификатор записи нельзя использовать в другое время.</span><span class="sxs-lookup"><span data-stu-id="ec092-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="ec092-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="ec092-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="ec092-124">Идентификатор записи является коротким термином.</span><span class="sxs-lookup"><span data-stu-id="ec092-124">The entry identifier is short-term.</span></span> <span data-ttu-id="ec092-125">Все остальные значения этого байта должны быть заданы, если не включено другое использование идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="ec092-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="ec092-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="ec092-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="ec092-127">Идентификатор записи нельзя использовать в других сеансах.</span><span class="sxs-lookup"><span data-stu-id="ec092-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="ec092-128">**поисков**</span><span class="sxs-lookup"><span data-stu-id="ec092-128">**ab**</span></span>
  
> <span data-ttu-id="ec092-129">Указывает массив двоичных данных, используемый поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="ec092-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="ec092-130">Клиентское приложение не может использовать этот массив.</span><span class="sxs-lookup"><span data-stu-id="ec092-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec092-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec092-131">Remarks</span></span>

<span data-ttu-id="ec092-132">Структура кода **EntryID** используется поставщиками хранилищ сообщений и адресных книг для создания уникальных идентификаторов объектов.</span><span class="sxs-lookup"><span data-stu-id="ec092-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="ec092-133">Идентификаторы записей используются для определения следующих типов объектов:</span><span class="sxs-lookup"><span data-stu-id="ec092-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="ec092-134">Хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="ec092-134">Message stores</span></span>
    
- <span data-ttu-id="ec092-135">Folders</span><span class="sxs-lookup"><span data-stu-id="ec092-135">Folders</span></span>
    
- <span data-ttu-id="ec092-136">Сообщения</span><span class="sxs-lookup"><span data-stu-id="ec092-136">Messages</span></span>
    
- <span data-ttu-id="ec092-137">Контейнеры адресных книг</span><span class="sxs-lookup"><span data-stu-id="ec092-137">Address book containers</span></span>
    
- <span data-ttu-id="ec092-138">Списки рассылки</span><span class="sxs-lookup"><span data-stu-id="ec092-138">Distribution lists</span></span>
    
- <span data-ttu-id="ec092-139">Пользователи системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="ec092-139">Messaging users</span></span>
    
- <span data-ttu-id="ec092-140">Объекты состояний</span><span class="sxs-lookup"><span data-stu-id="ec092-140">Status objects</span></span>
    
- <span data-ttu-id="ec092-141">Разделы профиля</span><span class="sxs-lookup"><span data-stu-id="ec092-141">Profile sections</span></span>
    
<span data-ttu-id="ec092-142">Каждый поставщик использует формат для структуры **EntryID** , который имеет смысл для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="ec092-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="ec092-143">Идентификаторы записей не могут сравниваться напрямую, так как один объект может быть представлен двумя разными двоичными значениями.</span><span class="sxs-lookup"><span data-stu-id="ec092-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="ec092-144">Чтобы определить, представляют ли два идентификатора записи один и тот же объект, вызовите метод [IMAPISession:: метод compareentryids](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="ec092-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="ec092-145">Когда клиент вызывает метод объекта [IMAPIProp::/PROPS](imapiprop-getprops.md) для получения идентификатора записи, объект возвращает самую постоянную форму идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="ec092-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="ec092-146">Клиент может проверить, что идентификатор записи является долгосрочным, проверив, не установлен ли ни один из флагов в первом байте элемента **абфлагс** .</span><span class="sxs-lookup"><span data-stu-id="ec092-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="ec092-147">Когда клиент получает доступ к идентификатору записи через столбец в таблице, скорее всего, этот идентификатор записи является краткосрочным, а не длинным термином.</span><span class="sxs-lookup"><span data-stu-id="ec092-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="ec092-148">Краткосрочные идентификаторы записей можно использовать для открытия соответствующих объектов только в текущем сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="ec092-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="ec092-149">Клиент может проверить, что идентификатор записи является краткосрочным, проверив, все ли флаги установлены в первом байте элемента **абфлагс** .</span><span class="sxs-lookup"><span data-stu-id="ec092-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="ec092-150">Некоторые идентификаторы записей являются краткосрочными, но в долгосрочной перспективе используются.</span><span class="sxs-lookup"><span data-stu-id="ec092-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="ec092-151">Такой идентификатор записи будет иметь один или несколько подходящих флагов, заданные в первом байте элемента **абфлагс** .</span><span class="sxs-lookup"><span data-stu-id="ec092-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="ec092-152">Структура **EntryID** похожа на структуру [флатентри](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="ec092-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="ec092-153">Однако существуют некоторые отличия.</span><span class="sxs-lookup"><span data-stu-id="ec092-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="ec092-154">Структура **EntryID** не хранит размер идентификатора записи; Структура **флатентри** .</span><span class="sxs-lookup"><span data-stu-id="ec092-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="ec092-155">Структура **EntryID** хранит данные флага и остальной части идентификатора записи отдельно; Структура **флатентри** хранит данные флага с остальной частью идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="ec092-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="ec092-156">Структура **EntryID** передается в качестве параметра методам интерфейса [IMAPIProp](imapipropiunknown.md) и следующим методам **OpenEntry** : [иаблогон:: OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [имаписуппорт:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), [имслогон:: OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="ec092-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="ec092-157">Структура **EntryID** используется для хранения идентификатора записи на диске.</span><span class="sxs-lookup"><span data-stu-id="ec092-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="ec092-158">Структура **флатентри** используется для хранения идентификатора записи в файле или его передачи в потоке байтов.</span><span class="sxs-lookup"><span data-stu-id="ec092-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="ec092-159">Клиенты всегда должны передаваться в естественным образом выровненные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="ec092-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="ec092-160">Несмотря на то, что поставщики должны обрабатывать идентификаторы записей с произвольным выравниванием, клиенты не должны ожидать такого поведения.</span><span class="sxs-lookup"><span data-stu-id="ec092-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="ec092-161">Неудачная передача правильного идентификатора записи в метод может привести к ошибке выравнивания на процессорах RISC.</span><span class="sxs-lookup"><span data-stu-id="ec092-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="ec092-162">Натуральный фактор выравнивания обычно 8 байтов — это самый большой тип данных, поддерживаемый ЦП, и обычно тот же коэффициент выравнивания, который используется механизмом распределения системной памяти.</span><span class="sxs-lookup"><span data-stu-id="ec092-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="ec092-163">Согласованный адрес памяти позволяет ЦП получать доступ ко всем типам данных, которые он поддерживает по этому адресу без создания ошибки выравнивания.</span><span class="sxs-lookup"><span data-stu-id="ec092-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="ec092-164">Для процессоров RISC тип данных "размер N байт" обычно должен быть выровнен по четным числам, равным N байтам, с адресом, равным нескольким N.</span><span class="sxs-lookup"><span data-stu-id="ec092-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="ec092-165">Для получения дополнительных сведений см [идентификаторы записей](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="ec092-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec092-166">См. также</span><span class="sxs-lookup"><span data-stu-id="ec092-166">See also</span></span>



[<span data-ttu-id="ec092-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="ec092-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="ec092-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ec092-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="ec092-169">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="ec092-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="ec092-170">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ec092-170">MAPI Structures</span></span>](mapi-structures.md)

