---
title: Создание списка рассылки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f0a6b7af196073d52ce98037b443569dcd1f41e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582548"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="d7705-103">Создание списка рассылки</span><span class="sxs-lookup"><span data-stu-id="d7705-103">Creating a distribution list</span></span>

<span data-ttu-id="d7705-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7705-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7705-105">Клиенты могут создавать список рассылки непосредственно в можно изменить контейнер, такие как личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="d7705-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="d7705-106">**Чтобы создать список рассылки в личной адресной книги**</span><span class="sxs-lookup"><span data-stu-id="d7705-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="d7705-107">Создание массива тег размера свойства с тегом одно свойство, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7705-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="d7705-108">Вызовите [IAddrBook::GetPAB](iaddrbook-getpab.md) , чтобы получить идентификатор записи личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d7705-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="d7705-109">Если возникает ошибка или **GetPAB** возвращает ноль или значение NULL, не продолжайте.</span><span class="sxs-lookup"><span data-stu-id="d7705-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="d7705-110">Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) , чтобы открыть личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d7705-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="d7705-111">Выходной параметр _ulObjType_ должен иметь значение MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="d7705-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="d7705-112">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) адресной книги для получения свойства PR_DEF_CREATE_DL шаблон, который используется для создания списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="d7705-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="d7705-113">Если не удается выполнить **GetProps** :</span><span class="sxs-lookup"><span data-stu-id="d7705-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="d7705-114">Вызов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) адресной книги для открытия свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с помощью интерфейса **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="d7705-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="d7705-115">Создание ограничение свойства для поиска строк со столбцом **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)), равное «MAPIPDL».</span><span class="sxs-lookup"><span data-stu-id="d7705-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="d7705-116">Вызовите [IMAPITable::FindRow](imapitable-findrow.md) , чтобы найти этой строки.</span><span class="sxs-lookup"><span data-stu-id="d7705-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="d7705-117">Сохраните идентификатор записи, возвращенный **GetProps** или **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="d7705-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="d7705-118">Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) адресной книги для создания записи с помощью шаблона, представленное идентификатор сохраненного записи.</span><span class="sxs-lookup"><span data-stu-id="d7705-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="d7705-119">Не предполагается, что объект, возвращенный можно считать список рассылки, а не для обмена сообщениями пользователя, когда этот вызов является удаленным.</span><span class="sxs-lookup"><span data-stu-id="d7705-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="d7705-120">Обратите внимание на то, что флаг CREATE_CHECK_DUP передается в параметре _ulFlags_ для предотвращения дважды добавления записи.</span><span class="sxs-lookup"><span data-stu-id="d7705-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="d7705-121">Вызовите метод **IUnknown::QueryInterface** новую запись, передав IID_IDistList идентификатор интерфейса, чтобы определить, если операция — это список рассылки и поддерживает [IDistList: IMAPIContainer](idistlistimapicontainer.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d7705-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="d7705-122">Так как **CreateEntry** возвращает указатель **IMAPIProp** , а не более конкретные указатель **IMailUser** или **IDistList** , проверьте, что объект списка рассылки был создан.</span><span class="sxs-lookup"><span data-stu-id="d7705-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="d7705-123">При успешном **QueryInterface** , можно убедиться, что вы создали в список рассылки, а не для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="d7705-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="d7705-124">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) списка рассылки, чтобы задать его отображаемого имени и других свойств.</span><span class="sxs-lookup"><span data-stu-id="d7705-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="d7705-125">Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) списка рассылки, чтобы добавить одного или нескольких пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d7705-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="d7705-126">Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) список рассылки, когда вы будете готовы для его сохранения.</span><span class="sxs-lookup"><span data-stu-id="d7705-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="d7705-127">Чтобы получить идентификатор записи из списка сохраненных рассылки, установить флаг KEEP_OPEN_READWRITE, а затем вызвать [IMAPIProp::GetProps](imapiprop-getprops.md) разрешения на запрос свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7705-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="d7705-128">Освобождение список рассылки и личной адресной книги, вызвав их **функции IUnknown::Release** методы.</span><span class="sxs-lookup"><span data-stu-id="d7705-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="d7705-129">Вызовите [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить память для идентификатора записи адресной книги и массива тег размера свойства.</span><span class="sxs-lookup"><span data-stu-id="d7705-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

