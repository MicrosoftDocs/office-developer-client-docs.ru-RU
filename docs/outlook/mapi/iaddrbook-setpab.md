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
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424618"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="e9b80-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="e9b80-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="e9b80-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9b80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9b80-105">Назначает определенный контейнер в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="e9b80-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e9b80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9b80-106">Parameters</span></span>

 <span data-ttu-id="e9b80-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e9b80-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e9b80-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="e9b80-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e9b80-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e9b80-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e9b80-110">[in] Указатель на идентификатор записи контейнера, который должен быть назначен в качестве PAB.</span><span class="sxs-lookup"><span data-stu-id="e9b80-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="e9b80-111">Параметр  _lpEntryID_ не может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="e9b80-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e9b80-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9b80-112">Return value</span></span>

<span data-ttu-id="e9b80-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9b80-113">S_OK</span></span> 
  
> <span data-ttu-id="e9b80-114">Указанный контейнер установлен в качестве PAB.</span><span class="sxs-lookup"><span data-stu-id="e9b80-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9b80-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9b80-115">Remarks</span></span>

<span data-ttu-id="e9b80-116">Клиенты и поставщики услуг **звонят методу SetPAB,** чтобы назначить определенный контейнер в качестве PAB.</span><span class="sxs-lookup"><span data-stu-id="e9b80-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="e9b80-117">PAB — это контейнер, состоящий из записей, скопированные из других контейнеров, а также новых записей.</span><span class="sxs-lookup"><span data-stu-id="e9b80-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="e9b80-118">Вызов **SetPAB** устанавливает контейнер в качестве PAB, пока этот контейнер не станет недоступным или новый контейнер не станет PAB посредством последующего вызова **SetPAB.**</span><span class="sxs-lookup"><span data-stu-id="e9b80-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="e9b80-119">Клиентам и поставщикам не нужно вызывать метод [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) чтобы изменить PAB без изменений.</span><span class="sxs-lookup"><span data-stu-id="e9b80-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e9b80-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e9b80-120">MFCMAPI reference</span></span>

<span data-ttu-id="e9b80-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e9b80-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e9b80-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e9b80-122">**File**</span></span>|<span data-ttu-id="e9b80-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e9b80-123">**Function**</span></span>|<span data-ttu-id="e9b80-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e9b80-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e9b80-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e9b80-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="e9b80-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="e9b80-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="e9b80-127">MFCMAPI использует метод **SetPAB,** чтобы сделать указанный контейнер PAB.</span><span class="sxs-lookup"><span data-stu-id="e9b80-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9b80-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e9b80-128">See also</span></span>



[<span data-ttu-id="e9b80-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="e9b80-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="e9b80-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="e9b80-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="e9b80-131">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="e9b80-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="e9b80-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e9b80-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="e9b80-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e9b80-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

