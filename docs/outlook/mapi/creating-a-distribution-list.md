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
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424177"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="713f1-103">Создание списка рассылки</span><span class="sxs-lookup"><span data-stu-id="713f1-103">Creating a distribution list</span></span>

<span data-ttu-id="713f1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="713f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="713f1-105">Клиенты могут создать список рассылки непосредственно в изменяемом контейнере, например в личной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="713f1-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="713f1-106">**Создание списка рассылки в PAB**</span><span class="sxs-lookup"><span data-stu-id="713f1-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="713f1-107">Создайте массив тегов свойств размера с одним тегом свойства **PR_DEF_CREATE_DL** ([PidTagDefCreateDl),](pidtagdefcreatedl-canonical-property.md)следующим образом:</span><span class="sxs-lookup"><span data-stu-id="713f1-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="713f1-108">Вызовите [IAddrBook::GetPAB,](iaddrbook-getpab.md) чтобы получить идентификатор записи для PAB.</span><span class="sxs-lookup"><span data-stu-id="713f1-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="713f1-109">Если произошла ошибка или **GetPAB** возвращает ноль или значение NULL, не продолжайте.</span><span class="sxs-lookup"><span data-stu-id="713f1-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="713f1-110">Вызовите [IAddrBook::OpenEntry,](iaddrbook-openentry.md) чтобы открыть PAB.</span><span class="sxs-lookup"><span data-stu-id="713f1-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="713f1-111">Выходной  _параметр ulObjType_ должен иметь MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="713f1-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="713f1-112">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) для получения свойства PR_DEF_CREATE_DL, шаблона, который используется для создания списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="713f1-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="713f1-113">Если **сбой GetProps:**</span><span class="sxs-lookup"><span data-stu-id="713f1-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="713f1-114">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для PAB, чтобы открыть **свойство PR_CREATE_TEMPLATES** ([PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)с интерфейсом **IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="713f1-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="713f1-115">Создайте ограничение свойств для поиска строки со **столбцом PR_ADDRTYPE** ([PidTagAddressType),](pidtagaddresstype-canonical-property.md)равным "MAPIPDL".</span><span class="sxs-lookup"><span data-stu-id="713f1-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="713f1-116">Вызовите [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти эту строку.</span><span class="sxs-lookup"><span data-stu-id="713f1-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="713f1-117">Сохраните идентификатор записи, возвращенный **getProps** или **FindRow.**</span><span class="sxs-lookup"><span data-stu-id="713f1-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="713f1-118">Вызовите метод [IABContainer::CreateEntry для PAB,](iabcontainer-createentry.md) чтобы создать новую запись с помощью шаблона, представленного сохраненным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="713f1-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="713f1-119">При удалении этого вызова не следует предполагать, что возвращенный объект будет списком рассылки, а не пользователем системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="713f1-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="713f1-120">Обратите внимание, CREATE_CHECK_DUP флаг передается в  _параметре ulFlags,_ чтобы запись не добавлялась дважды.</span><span class="sxs-lookup"><span data-stu-id="713f1-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="713f1-121">Вызовите метод **IUnknown::QueryInterface** новой записи, передав IID_IDistList в качестве идентификатора интерфейса, чтобы определить, является ли запись списком рассылки и поддерживает интерфейс [IDistList : IMAPIContainer.](idistlistimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="713f1-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="713f1-122">Поскольку **CreateEntry** возвращает указатель **IMAPIProp,** а не более конкретный указатель **IMailUser** или **IDistList,** убедитесь, что объект списка рассылки создан.</span><span class="sxs-lookup"><span data-stu-id="713f1-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="713f1-123">Если **queryInterface** успешно, вы можете быть уверены, что вы создали список рассылки, а не пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="713f1-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="713f1-124">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) списка рассылки, чтобы установить его отображаемую и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="713f1-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="713f1-125">Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) списка рассылки, чтобы добавить одного или несколько пользователей обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="713f1-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="713f1-126">Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) списка рассылки, когда будете готовы сохранить его.</span><span class="sxs-lookup"><span data-stu-id="713f1-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="713f1-127">Чтобы получить идентификатор записи сохраненного списка рассылки, установите флаг KEEP_OPEN_READWRITE и вызовите [IMAPIProp::GetProps,](imapiprop-getprops.md) **запрашивающий** свойство PR_ENTRYID ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="713f1-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="713f1-128">Освободите новый список рассылки и PAB, вызывая их методы **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="713f1-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="713f1-129">Вызовите [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память для идентификатора записи PAB и массива тегов свойств размера.</span><span class="sxs-lookup"><span data-stu-id="713f1-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

