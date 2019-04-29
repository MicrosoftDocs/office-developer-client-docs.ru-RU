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
# <a name="creating-a-distribution-list"></a><span data-ttu-id="b39f2-103">Создание списка рассылки</span><span class="sxs-lookup"><span data-stu-id="b39f2-103">Creating a distribution list</span></span>

<span data-ttu-id="b39f2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b39f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b39f2-105">Клиенты могут создавать списки рассылки непосредственно в изменяемом контейнере, например в личной адресной книге (PAB).</span><span class="sxs-lookup"><span data-stu-id="b39f2-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="b39f2-106">**Создание списка рассылки в личной АДРЕСНОЙ книге**</span><span class="sxs-lookup"><span data-stu-id="b39f2-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="b39f2-107">Создайте массив тегов свойств с одним тегом свойства, **пр_деф_креате_дл** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b39f2-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="b39f2-108">Call [IAddrBook:: жетпаб](iaddrbook-getpab.md) для получения идентификатора записи личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b39f2-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="b39f2-109">Если возникает ошибка или **жетпаб** возвращает ноль или null, не продолжайте.</span><span class="sxs-lookup"><span data-stu-id="b39f2-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="b39f2-110">Call [IAddrBook:: OpenEntry](iaddrbook-openentry.md) для открытия личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b39f2-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="b39f2-111">Параметру OUTPUT _улобжтипе_ должно быть присвоено значение мапи_абконт.</span><span class="sxs-lookup"><span data-stu-id="b39f2-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="b39f2-112">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) /PROPS PAB PAB, чтобы получить свойство пр_деф_креате_дл, шаблон, который используется для создания списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="b39f2-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="b39f2-113">Если \*\*\*\* не удается выполнить команду PROPS:</span><span class="sxs-lookup"><span data-stu-id="b39f2-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="b39f2-114">ВыЗовите метод [IMAPIProp:: ОПЕНПРОПЕРТИ](imapiprop-openproperty.md) личной адресной книги, чтобы открыть свойство **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с помощью интерфейса **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="b39f2-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="b39f2-115">Создайте ограничение свойства для поиска строки со столбцом **пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)), равным "мапипдл".</span><span class="sxs-lookup"><span data-stu-id="b39f2-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="b39f2-116">Call [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения этой строки.</span><span class="sxs-lookup"><span data-stu-id="b39f2-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="b39f2-117">Сохраните идентификатор записи, возвращенный с \*\*\*\* помощью метода/Props, или метода **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="b39f2-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="b39f2-118">ВыЗовите метод [иабконтаинер:: КРЕАТИНТРИ](iabcontainer-createentry.md) PAB, чтобы создать новую запись, используя шаблон, представленный сохраненным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="b39f2-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="b39f2-119">Не следует предполагать, что возвращаемый объект будет списком рассылки, а не пользователем обмена сообщениями при удаленном вызове.</span><span class="sxs-lookup"><span data-stu-id="b39f2-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="b39f2-120">Обратите внимание на то, что в параметре _ulFlags_ передается флаг креате_чекк_дуп, чтобы не допустить Добавление записи дважды.</span><span class="sxs-lookup"><span data-stu-id="b39f2-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="b39f2-121">ВыЗовите метод **IUnknown:: QueryInterface** новой записи, передав иид_идистлист в качестве идентификатора интерфейса, чтобы определить, является ли запись списком рассылки, и поддерживает ли она интерфейс [идистлист: IMAPIContainer](idistlistimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="b39f2-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="b39f2-122">Так как **креатинтри** возвращает указатель **IMAPIProp** , а не более конкретный указатель **имаилусер** или **идистлист** , убедитесь, что был создан объект списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="b39f2-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="b39f2-123">Если **QueryInterface** завершается успешно, вы можете убедиться, что вы создали список рассылки, а не пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b39f2-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="b39f2-124">ВыЗовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) списка рассылки, чтобы задать отображаемое имя и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="b39f2-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="b39f2-125">ВыЗовите метод [иабконтаинер:: креатинтри](iabcontainer-createentry.md) списка рассылки, чтобы добавить одного или нескольких пользователей системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b39f2-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="b39f2-126">ВыЗовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) списка рассылки, когда будете готовы сохранить его.</span><span class="sxs-lookup"><span data-stu-id="b39f2-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="b39f2-127">Чтобы получить идентификатор записи сохраненного списка рассылки, установите флаг КИП_ОПЕН_РЕАДВРИТЕ и затем вызовите [IMAPIProp::](imapiprop-getprops.md) -Props, запрашивающие свойство **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b39f2-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="b39f2-128">Освободите новый список рассылки и личную личную книгу, вызвав их методы выПусков: **: Release** .</span><span class="sxs-lookup"><span data-stu-id="b39f2-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="b39f2-129">ВыЗовите [мапифрибуффер](mapifreebuffer.md) , чтобы освободить память для идентификатора записи для массива тегов свойств PAB и Letter.</span><span class="sxs-lookup"><span data-stu-id="b39f2-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

