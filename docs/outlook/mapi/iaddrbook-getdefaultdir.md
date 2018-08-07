---
title: IAddrBookGetDefaultDir
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
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808760"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="f75af-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="f75af-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="f75af-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f75af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f75af-105">Возвращает идентификатор записи для контейнер начальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f75af-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="f75af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f75af-106">Parameters</span></span>

 <span data-ttu-id="f75af-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f75af-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="f75af-108">[out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f75af-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f75af-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="f75af-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="f75af-110">[out] Указатель на указатель на запись идентификатор контейнера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f75af-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f75af-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="f75af-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f75af-112">S_OK</span></span> 
  
> <span data-ttu-id="f75af-113">Идентификатор записи по умолчанию контейнера успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="f75af-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f75af-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f75af-114">Remarks</span></span>

<span data-ttu-id="f75af-115">Клиентские приложения и поставщиков услуг вызовите метод **GetDefaultDir** для получения идентификатора запись контейнер адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f75af-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="f75af-116">Контейнер по умолчанию является то, что на экране пользователя отображается отображаются в адресной книге, при первом открытии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f75af-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="f75af-117">Если контейнер по умолчанию с помощью вызова метода [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) не задано, MAPI, назначает как контейнер по умолчанию первого контейнера с именами, который не является личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="f75af-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="f75af-118">Если не удается найти такие контейнер, личной адресной книги становится контейнера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f75af-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="f75af-119">По умолчанию каталог, клиента или поставщика вызывается метод **SetDefaultDir** .</span><span class="sxs-lookup"><span data-stu-id="f75af-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="f75af-120">Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; так как изменения в адресной книге не выполняются, изменения сразу же становятся постоянными.</span><span class="sxs-lookup"><span data-stu-id="f75af-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f75af-121">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="f75af-121">MFCMAPI reference</span></span>

<span data-ttu-id="f75af-122">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="f75af-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f75af-123">**����**</span><span class="sxs-lookup"><span data-stu-id="f75af-123">**File**</span></span>|<span data-ttu-id="f75af-124">**�������**</span><span class="sxs-lookup"><span data-stu-id="f75af-124">**Function**</span></span>|<span data-ttu-id="f75af-125">**�����������**</span><span class="sxs-lookup"><span data-stu-id="f75af-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f75af-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f75af-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="f75af-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="f75af-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="f75af-128">Mfcmapi (en) использует метод **GetDefaultDir** , чтобы получить идентификатор контейнер адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f75af-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f75af-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f75af-129">See also</span></span>



[<span data-ttu-id="f75af-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="f75af-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="f75af-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f75af-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="f75af-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f75af-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f75af-133">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="f75af-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="f75af-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f75af-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="f75af-135">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f75af-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

