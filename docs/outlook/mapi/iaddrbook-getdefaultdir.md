---
title: иаддрбукжетдефаултдир
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436876"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="6c3f9-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="6c3f9-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="6c3f9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c3f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c3f9-105">Возвращает идентификатор для исходного контейнера адресных книг.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="6c3f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c3f9-106">Parameters</span></span>

 <span data-ttu-id="6c3f9-107">_лпкбентрид_</span><span class="sxs-lookup"><span data-stu-id="6c3f9-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="6c3f9-108">вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ .</span><span class="sxs-lookup"><span data-stu-id="6c3f9-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6c3f9-109">_лппентрид_</span><span class="sxs-lookup"><span data-stu-id="6c3f9-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="6c3f9-110">вышли Указатель на указатель на идентификатор элемента контейнера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c3f9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c3f9-111">Return value</span></span>

<span data-ttu-id="6c3f9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c3f9-112">S_OK</span></span> 
  
> <span data-ttu-id="6c3f9-113">Идентификатор элемента контейнера по умолчанию успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c3f9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c3f9-114">Remarks</span></span>

<span data-ttu-id="6c3f9-115">Клиентские приложения и поставщики услуг вызывают метод **жетдефаултдир** для получения идентификатора записи контейнера адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="6c3f9-116">По умолчанию при первом открытии адресной книги пользователь видит отображаемый в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="6c3f9-117">Если контейнер по умолчанию не был задан при вызове метода [IAddrBook:: сетдефаултдир](iaddrbook-setdefaultdir.md) , то в качестве контейнера по умолчанию используется MAPI, который является первым контейнером с именами, не являющийся личной адресной книгой (PAB).</span><span class="sxs-lookup"><span data-stu-id="6c3f9-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="6c3f9-118">Если такой контейнер не удается найти, PAB становится контейнером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="6c3f9-119">Чтобы задать каталог по умолчанию, клиент или поставщик вызывает метод **сетдефаултдир** .</span><span class="sxs-lookup"><span data-stu-id="6c3f9-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="6c3f9-120">Клиентам и поставщикам не нужно вызывать метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ; так как изменения в адресной книге не являются транзакционными, изменения немедленно вносятся в окончательные.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c3f9-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6c3f9-121">MFCMAPI reference</span></span>

<span data-ttu-id="6c3f9-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c3f9-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6c3f9-123">**File**</span></span>|<span data-ttu-id="6c3f9-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6c3f9-124">**Function**</span></span>|<span data-ttu-id="6c3f9-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6c3f9-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c3f9-126">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="6c3f9-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6c3f9-127">Кмаиндлг:: Онопендефаултдир</span><span class="sxs-lookup"><span data-stu-id="6c3f9-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="6c3f9-128">MFCMAPI использует метод **жетдефаултдир** , чтобы получить идентификатор для контейнера адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c3f9-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c3f9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="6c3f9-129">See also</span></span>



[<span data-ttu-id="6c3f9-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="6c3f9-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="6c3f9-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="6c3f9-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="6c3f9-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6c3f9-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6c3f9-133">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="6c3f9-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="6c3f9-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6c3f9-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="6c3f9-135">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6c3f9-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

