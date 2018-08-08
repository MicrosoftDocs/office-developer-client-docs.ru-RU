---
title: IAddrBookSetPAB
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
ms.openlocfilehash: 3f13a4d278b85ffae33e8f44f3a15eb499fb11b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808777"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="c9803-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="c9803-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="c9803-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9803-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9803-105">Назначает конкретным контейнером Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="c9803-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="c9803-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9803-106">Parameters</span></span>

 <span data-ttu-id="c9803-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9803-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c9803-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c9803-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c9803-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9803-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c9803-110">[in] Указатель на идентификатор записи контейнера в качестве личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9803-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="c9803-111">Параметр _lpEntryID_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="c9803-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9803-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c9803-112">Return value</span></span>

<span data-ttu-id="c9803-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c9803-113">S_OK</span></span> 
  
> <span data-ttu-id="c9803-114">Указанный контейнер установлено как личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9803-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9803-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9803-115">Remarks</span></span>

<span data-ttu-id="c9803-116">Клиенты и поставщики услуг вызовите метод **SetPAB** для назначения конкретным контейнером в качестве личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9803-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="c9803-117">Личной адресной книги является контейнером, состоит из записей, скопированные из других контейнеров, а также новые записи.</span><span class="sxs-lookup"><span data-stu-id="c9803-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="c9803-118">Вызов **SetPAB** устанавливает контейнером в качестве личной адресной книги, до этого контейнера становится недоступной или новый контейнер становится адресной книги через следующий вызов **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="c9803-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="c9803-119">Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , чтобы сохранить изменение адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9803-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c9803-120">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="c9803-120">MFCMAPI reference</span></span>

<span data-ttu-id="c9803-121">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="c9803-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c9803-122">**����**</span><span class="sxs-lookup"><span data-stu-id="c9803-122">**File**</span></span>|<span data-ttu-id="c9803-123">**�������**</span><span class="sxs-lookup"><span data-stu-id="c9803-123">**Function**</span></span>|<span data-ttu-id="c9803-124">**�����������**</span><span class="sxs-lookup"><span data-stu-id="c9803-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9803-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c9803-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="c9803-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="c9803-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="c9803-127">Mfcmapi (en) использует метод **SetPAB** для внесите в указанный контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9803-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9803-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c9803-128">See also</span></span>



[<span data-ttu-id="c9803-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="c9803-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="c9803-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="c9803-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="c9803-131">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="c9803-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="c9803-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c9803-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="c9803-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c9803-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

