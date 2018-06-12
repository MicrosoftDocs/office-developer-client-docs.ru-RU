---
title: ИДЕНТИФИКАТОР ЗАПИСИ
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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 1b55703c9ad12e3645e6e9cb3dcfcbdf21b90d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808385"
---
# <a name="entryid"></a><span data-ttu-id="b96e3-103">ИДЕНТИФИКАТОР ЗАПИСИ</span><span class="sxs-lookup"><span data-stu-id="b96e3-103">ENTRYID</span></span>

  
  
<span data-ttu-id="b96e3-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b96e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b96e3-105">Содержит идентификатор записи для объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="b96e3-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b96e3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b96e3-106">Header file:</span></span>  <br/> |<span data-ttu-id="b96e3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b96e3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b96e3-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="b96e3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b96e3-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="b96e3-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="b96e3-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="b96e3-110">Members</span></span>

 <span data-ttu-id="b96e3-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="b96e3-111">**abFlags**</span></span>
  
> <span data-ttu-id="b96e3-112">Битовая маска флагов, предоставляющих сведения об объекте.</span><span class="sxs-lookup"><span data-stu-id="b96e3-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="b96e3-113">Первого байта ответа флаги **abFlags [0]**, может задать поставщиком; другие три зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="b96e3-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="b96e3-114">Эти флаги не должны быть установлены для идентификаторов навсегда; они определены только для краткосрочных идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="b96e3-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="b96e3-115">Для клиентов эта структура доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b96e3-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="b96e3-116">Можно задать следующие флаги в **abFlags [0]**:</span><span class="sxs-lookup"><span data-stu-id="b96e3-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="b96e3-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="b96e3-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="b96e3-118">Идентификатор записи нельзя использовать в качестве получателей на сообщение.</span><span class="sxs-lookup"><span data-stu-id="b96e3-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="b96e3-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="b96e3-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="b96e3-120">Другие пользователи не могут получить доступ к идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="b96e3-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="b96e3-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="b96e3-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="b96e3-122">Идентификатор записи не может использоваться в других случаях.</span><span class="sxs-lookup"><span data-stu-id="b96e3-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="b96e3-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="b96e3-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="b96e3-124">Идентификатор записи краткосрочных.</span><span class="sxs-lookup"><span data-stu-id="b96e3-124">The entry identifier is short-term.</span></span> <span data-ttu-id="b96e3-125">Все значения в этом байтов должно иметь значение, если не включены другие варианты использования идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="b96e3-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="b96e3-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="b96e3-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="b96e3-127">Идентификатор записи не может использоваться в других сеансов.</span><span class="sxs-lookup"><span data-stu-id="b96e3-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="b96e3-128">**AB**</span><span class="sxs-lookup"><span data-stu-id="b96e3-128">**ab**</span></span>
  
> <span data-ttu-id="b96e3-129">Указывает массив двоичные данные, используемые поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="b96e3-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="b96e3-130">Клиентское приложение не может использовать этот массив.</span><span class="sxs-lookup"><span data-stu-id="b96e3-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b96e3-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="b96e3-131">Remarks</span></span>

<span data-ttu-id="b96e3-132">Структура **ENTRYID** используется сообщение хранения и адресной книги поставщиков для создания уникальных идентификаторов для объектов.</span><span class="sxs-lookup"><span data-stu-id="b96e3-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="b96e3-133">Идентификаторы входа используются для определения следующих типов объектов:</span><span class="sxs-lookup"><span data-stu-id="b96e3-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="b96e3-134">Хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="b96e3-134">Message stores</span></span>
    
- <span data-ttu-id="b96e3-135">Папки</span><span class="sxs-lookup"><span data-stu-id="b96e3-135">Folders</span></span>
    
- <span data-ttu-id="b96e3-136">Сообщения</span><span class="sxs-lookup"><span data-stu-id="b96e3-136">Messages</span></span>
    
- <span data-ttu-id="b96e3-137">Контейнеры адресной книги</span><span class="sxs-lookup"><span data-stu-id="b96e3-137">Address book containers</span></span>
    
- <span data-ttu-id="b96e3-138">Списки рассылки</span><span class="sxs-lookup"><span data-stu-id="b96e3-138">Distribution lists</span></span>
    
- <span data-ttu-id="b96e3-139">Пользователи системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="b96e3-139">Messaging users</span></span>
    
- <span data-ttu-id="b96e3-140">Объекты состояния</span><span class="sxs-lookup"><span data-stu-id="b96e3-140">Status objects</span></span>
    
- <span data-ttu-id="b96e3-141">Разделы профилей</span><span class="sxs-lookup"><span data-stu-id="b96e3-141">Profile sections</span></span>
    
<span data-ttu-id="b96e3-142">Каждый поставщик использует формат для структуры **ENTRYID** , который имеет смысл для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="b96e3-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="b96e3-143">Идентификаторы записей нельзя сравнивать напрямую, так как один объект могут быть представлены два двоичные значения.</span><span class="sxs-lookup"><span data-stu-id="b96e3-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="b96e3-144">Чтобы определить, представляют ли два идентификаторы записей тот же объект, вызовите метод [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="b96e3-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="b96e3-145">Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) объекта для извлечения его идентификатор записи, объект возвращает наиболее постоянное формы идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="b96e3-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="b96e3-146">Клиент может убедитесь, что идентификатор записи долгосрочного, проверьте, что ни один из флагов, заданы в первого байта ответа **abFlags** элемента.</span><span class="sxs-lookup"><span data-stu-id="b96e3-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="b96e3-147">При обращении идентификатор записи через столбца в таблице, скорее всего, этот идентификатор записи краткосрочных вместо долгосрочного.</span><span class="sxs-lookup"><span data-stu-id="b96e3-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="b96e3-148">Краткосрочные идентификаторы записей можно использовать для открытия их соответствующими объектами только во время текущего сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="b96e3-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="b96e3-149">Клиент может убедитесь, что идентификатор записи краткосрочных, проверьте, что все флажки, заданы в первого байта ответа **abFlags** элемента.</span><span class="sxs-lookup"><span data-stu-id="b96e3-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="b96e3-150">Некоторые идентификаторы записей краткосрочной, но имеют длительного использования.</span><span class="sxs-lookup"><span data-stu-id="b96e3-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="b96e3-151">Этот идентификатор записи будут иметь одно или несколько соответствующих набора флагов в первого байта ответа его **abFlags** элементом.</span><span class="sxs-lookup"><span data-stu-id="b96e3-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="b96e3-152">Структуру **ENTRYID** напоминает структуру [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="b96e3-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="b96e3-153">Тем не менее существуют некоторые отличия:</span><span class="sxs-lookup"><span data-stu-id="b96e3-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="b96e3-154">Структуру **ENTRYID** не сохраняет размер идентификатор записи; выполняет **FLATENTRY** структуры.</span><span class="sxs-lookup"><span data-stu-id="b96e3-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="b96e3-155">Структуру **ENTRYID** хранит данные флаг и rest идентификатор записи отдельно; Структура **FLATENTRY** хранит данные флаг с помощью rest идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="b96e3-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="b96e3-156">Структуру **ENTRYID** передается как параметр для методов интерфейса [IMAPIProp](imapipropiunknown.md) и следующие методы **OpenEntry** : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md) [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="b96e3-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="b96e3-157">Структура **ENTRYID** используется для хранения идентификатора записи на диск.</span><span class="sxs-lookup"><span data-stu-id="b96e3-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="b96e3-158">Структура **FLATENTRY** используется для хранения идентификатора записи в файл или передайте его в виде потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="b96e3-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="b96e3-159">Клиенты всегда должен передавать идентификаторы естественно выровненные записей.</span><span class="sxs-lookup"><span data-stu-id="b96e3-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="b96e3-160">Несмотря на то, что поставщики будут обрабатывать идентификаторы произвольно выровненные записей, клиенты не следует ожидать это поведение.</span><span class="sxs-lookup"><span data-stu-id="b96e3-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="b96e3-161">Сбой, связанный с передавать идентификатор хорошим выровненным запись в метод может привести к сбою выравнивание на процессор RISC.</span><span class="sxs-lookup"><span data-stu-id="b96e3-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="b96e3-162">Коэффициент природные выравнивание, обычно 8 байтов является большой тип данных, поддерживаемый ЦП и обычно же коэффициента выравнивание путем выделения памяти системы.</span><span class="sxs-lookup"><span data-stu-id="b96e3-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="b96e3-163">Адрес естественно выровненные памяти позволяет ЦП для доступа к любой тип данных, поддерживаемых по этому адресу без создания ошибку выравнивание.</span><span class="sxs-lookup"><span data-stu-id="b96e3-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="b96e3-164">Для ЦП RISC тип данных размером N байт должен обычно выравнивания на делится N байт с адреса, который делится N.</span><span class="sxs-lookup"><span data-stu-id="b96e3-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="b96e3-165">Для получения дополнительных сведений см [Идентификаторы записей](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b96e3-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b96e3-166">См. также</span><span class="sxs-lookup"><span data-stu-id="b96e3-166">See also</span></span>



[<span data-ttu-id="b96e3-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="b96e3-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="b96e3-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="b96e3-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="b96e3-169">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="b96e3-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="b96e3-170">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b96e3-170">MAPI Structures</span></span>](mapi-structures.md)

