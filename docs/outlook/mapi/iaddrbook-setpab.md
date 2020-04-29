---
title: иаддрбуксетпаб
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424618"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="9086d-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="9086d-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="9086d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9086d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9086d-105">Назначает определенный контейнер в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="9086d-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="9086d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9086d-106">Parameters</span></span>

 <span data-ttu-id="9086d-107">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="9086d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="9086d-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="9086d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9086d-109">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="9086d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="9086d-110">возврата Указатель на идентификатор записи контейнера, который необходимо назначить в качестве личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9086d-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="9086d-111">Параметр _лпентрид_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="9086d-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9086d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9086d-112">Return value</span></span>

<span data-ttu-id="9086d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9086d-113">S_OK</span></span> 
  
> <span data-ttu-id="9086d-114">Указанный контейнер был установлен в качестве личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9086d-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9086d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="9086d-115">Remarks</span></span>

<span data-ttu-id="9086d-116">Клиенты и поставщики услуг вызывают метод **сетпаб** , чтобы назначить конкретный контейнер в качестве личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9086d-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="9086d-117">PAB — это контейнер, который содержит записи, скопированные из других контейнеров, а также новые записи.</span><span class="sxs-lookup"><span data-stu-id="9086d-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="9086d-118">При вызове **сетпаб** создается контейнер в качестве личной адресной книги, пока он не станет недоступен или новый контейнер становится личной адресной книгой при последующих вызовах **сетпаб**.</span><span class="sxs-lookup"><span data-stu-id="9086d-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="9086d-119">Клиентам и поставщикам не нужно вызывать метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , чтобы сделать изменение личной адресной книги постоянным.</span><span class="sxs-lookup"><span data-stu-id="9086d-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9086d-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9086d-120">MFCMAPI reference</span></span>

<span data-ttu-id="9086d-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9086d-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9086d-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9086d-122">**File**</span></span>|<span data-ttu-id="9086d-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9086d-123">**Function**</span></span>|<span data-ttu-id="9086d-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9086d-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9086d-125">Абконтдлг. cpp</span><span class="sxs-lookup"><span data-stu-id="9086d-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="9086d-126">Кабконтдлг:: Онсетпаб</span><span class="sxs-lookup"><span data-stu-id="9086d-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="9086d-127">MFCMAPI использует метод **сетпаб** , чтобы сделать указанный контейнер личной адресной книгой.</span><span class="sxs-lookup"><span data-stu-id="9086d-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9086d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9086d-128">See also</span></span>



[<span data-ttu-id="9086d-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="9086d-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="9086d-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="9086d-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="9086d-131">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="9086d-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="9086d-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9086d-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="9086d-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9086d-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

