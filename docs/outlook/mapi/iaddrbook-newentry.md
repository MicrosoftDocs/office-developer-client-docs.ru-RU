---
title: Иаддрбукневентри
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336717"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="45b66-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="45b66-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="45b66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45b66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45b66-105">Добавляет нового получателя в контейнер адресной книги или в список получателей исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="45b66-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a><span data-ttu-id="45b66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45b66-106">Parameters</span></span>

 <span data-ttu-id="45b66-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="45b66-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="45b66-108">возврата Дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="45b66-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="45b66-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45b66-109">_ulFlags_</span></span>
  
> <span data-ttu-id="45b66-110">возврата Битовая маска флагов, определяющая тип используемого текста.</span><span class="sxs-lookup"><span data-stu-id="45b66-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="45b66-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="45b66-111">The following flag can be set:</span></span>
    
<span data-ttu-id="45b66-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45b66-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="45b66-113">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="45b66-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="45b66-114">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="45b66-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="45b66-115">_Кбеидконтаинер_</span><span class="sxs-lookup"><span data-stu-id="45b66-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="45b66-116">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпеидконтаинер_ .</span><span class="sxs-lookup"><span data-stu-id="45b66-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="45b66-117">_Лпеидконтаинер_</span><span class="sxs-lookup"><span data-stu-id="45b66-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="45b66-118">возврата Указатель на идентификатор элемента контейнера, в который нужно добавить нового получателя.</span><span class="sxs-lookup"><span data-stu-id="45b66-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="45b66-119">Если значение параметра _кбеидконтаинер_ равно нулю, метод **невентри** возвращает идентификатор записи получателя и список шаблонов, как если бы вызывался метод [IAddrBook:: креатеонеофф](iaddrbook-createoneoff.md) .</span><span class="sxs-lookup"><span data-stu-id="45b66-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="45b66-120">_Кбеидневентритпл_</span><span class="sxs-lookup"><span data-stu-id="45b66-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="45b66-121">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпеидневентритпл_ .</span><span class="sxs-lookup"><span data-stu-id="45b66-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="45b66-122">_Лпеидневентритпл_</span><span class="sxs-lookup"><span data-stu-id="45b66-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="45b66-123">возврата Указатель на одноразовый шаблон, который будет использоваться для создания нового получателя.</span><span class="sxs-lookup"><span data-stu-id="45b66-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="45b66-124">Если _кбеидневентритпл_ имеет значение 0, а _ЛПЕИДНЕВЕНТРИТПЛ_ имеет значение null, **невентри** отображает диалоговое окно, с помощью которого пользователь может выбрать из списка шаблонов для добавления новых записей.</span><span class="sxs-lookup"><span data-stu-id="45b66-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="45b66-125">_Лпкбеидневентри_</span><span class="sxs-lookup"><span data-stu-id="45b66-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="45b66-126">вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппеидневентри_ .</span><span class="sxs-lookup"><span data-stu-id="45b66-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="45b66-127">_Лппеидневентри_</span><span class="sxs-lookup"><span data-stu-id="45b66-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="45b66-128">вышли Указатель на указатель на указатель на идентификатор записи нового получателя.</span><span class="sxs-lookup"><span data-stu-id="45b66-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45b66-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45b66-129">Return value</span></span>

<span data-ttu-id="45b66-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="45b66-130">S_OK</span></span> 
  
> <span data-ttu-id="45b66-131">Новая запись адресной книги успешно создана.</span><span class="sxs-lookup"><span data-stu-id="45b66-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45b66-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45b66-132">Remarks</span></span>

<span data-ttu-id="45b66-133">Метод **невентри** создает новую запись адресной книги, которая будет добавляться непосредственно в контейнер или использоваться для адресации исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="45b66-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="45b66-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="45b66-134">Notes to callers</span></span>

<span data-ttu-id="45b66-135">Если вы хотите добавить новую запись в определенный контейнер, задайте для параметра _лпеидконтаинер_ идентификатор записи контейнера и _кбеидконтаинер_ в качестве значения счетчика байтов в идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="45b66-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="45b66-136">Если вы хотите добавить новую запись в список получателей исходящего сообщения, установите для параметра _ЛПЕИДКОНТАИНЕР_ значение NULL и _кбеидконтаинер_ в ноль.</span><span class="sxs-lookup"><span data-stu-id="45b66-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="45b66-137">Если вы хотите разрешить пользователю клиентского приложения выбирать тип создаваемой записи, передайте ноль в _кбеидневентритпл_ и значение NULL в _лпеидневентритпл_.</span><span class="sxs-lookup"><span data-stu-id="45b66-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="45b66-138">Метод **невентри** отображает одноадресную таблицу MAPI, список шаблонов, поддерживаемых MAPI, и каждого поставщика адресных книг в сеансе.</span><span class="sxs-lookup"><span data-stu-id="45b66-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="45b66-139">Каждый шаблон может создать запись получателя для одного или нескольких типов адресов.</span><span class="sxs-lookup"><span data-stu-id="45b66-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="45b66-140">Если необходимо сохранить идентификатор записи новой записи, передайте допустимые указатели в параметрах _лпкбеидневентри_ и _лппеидневентри_ .</span><span class="sxs-lookup"><span data-stu-id="45b66-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="45b66-141">Вы несете ответственность за освобождение этого идентификатора записи при завершении работы с ним, вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="45b66-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="45b66-142">Чтобы использовать определенный шаблон для добавления новой записи в изменяемый контейнер, выполните следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="45b66-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="45b66-143">ВыЗовите метод [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть целевой контейнер, и присвойте параметру _лпентрид_ идентификатор элемента контейнера.</span><span class="sxs-lookup"><span data-stu-id="45b66-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="45b66-144">ВыЗовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) конечного контейнера и задайте для параметра _улпроптаг_ значение **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) и для параметра _лпиид_ значение иид_имапитабле.</span><span class="sxs-lookup"><span data-stu-id="45b66-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="45b66-145">Контейнер вернет одноразовую таблицу, в которой перечислены все шаблоны, которые она поддерживает для создания новых записей.</span><span class="sxs-lookup"><span data-stu-id="45b66-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="45b66-146">Получите строку, представляющую шаблон для определенного типа записи, которую вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="45b66-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="45b66-147">В столбце **пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) указывается тип адреса, поддерживаемый шаблоном.</span><span class="sxs-lookup"><span data-stu-id="45b66-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="45b66-148">ВыЗовите метод **невентри** и задайте _лпеидневентритпл_ в качестве идентификатора записи выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="45b66-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="45b66-149">Идентификатором записи будет столбец **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из строки шаблона в таблице одноразовый.</span><span class="sxs-lookup"><span data-stu-id="45b66-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="45b66-150">В _кбеидконтаинер_ передается ноль, а в _лпеидконтаинер_— null.</span><span class="sxs-lookup"><span data-stu-id="45b66-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="45b66-151">Если требуется сохранить идентификатор записи нового элемента, переДается допустимый указатель в параметре _лппеидневентри_ .</span><span class="sxs-lookup"><span data-stu-id="45b66-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="45b66-152">См. также</span><span class="sxs-lookup"><span data-stu-id="45b66-152">See also</span></span>



[<span data-ttu-id="45b66-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="45b66-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="45b66-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="45b66-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="45b66-155">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="45b66-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="45b66-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="45b66-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

