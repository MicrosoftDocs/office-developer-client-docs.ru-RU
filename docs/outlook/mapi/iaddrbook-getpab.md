---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808766"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="ddc34-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="ddc34-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="ddc34-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddc34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddc34-105">Возвращает идентификатор записи контейнера, который используется в качестве Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="ddc34-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ddc34-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddc34-106">Parameters</span></span>

 <span data-ttu-id="ddc34-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ddc34-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="ddc34-108">[out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="ddc34-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ddc34-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="ddc34-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="ddc34-110">[out] Указатель на указатель на идентификатор записи личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ddc34-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="ddc34-111">Параметр _lppEntryID_ содержит нулевое значение, если контейнер не был определен как личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ddc34-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ddc34-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ddc34-112">Return value</span></span>

<span data-ttu-id="ddc34-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ddc34-113">S_OK</span></span> 
  
> <span data-ttu-id="ddc34-114">Идентификатор записи адресной книги успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="ddc34-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ddc34-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="ddc34-115">Remarks</span></span>

<span data-ttu-id="ddc34-116">Клиенты вызовите метод **GetPAB** для извлечения идентификатор записи контейнера обозначены как личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ddc34-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="ddc34-117">Если не было установлено в профиле адресной книги, MAPI выбирает в качестве личной адресной книги первого контейнера в иерархии адресной книги, обеспечивающий изменения.</span><span class="sxs-lookup"><span data-stu-id="ddc34-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ddc34-118">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="ddc34-118">MFCMAPI reference</span></span>

<span data-ttu-id="ddc34-119">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="ddc34-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ddc34-120">**����**</span><span class="sxs-lookup"><span data-stu-id="ddc34-120">**File**</span></span>|<span data-ttu-id="ddc34-121">**�������**</span><span class="sxs-lookup"><span data-stu-id="ddc34-121">**Function**</span></span>|<span data-ttu-id="ddc34-122">**�����������**</span><span class="sxs-lookup"><span data-stu-id="ddc34-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ddc34-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ddc34-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="ddc34-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="ddc34-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="ddc34-125">Mfcmapi (en) использует метод **GetPAB** для получения идентификатора для пользователя Личная адресная книга.</span><span class="sxs-lookup"><span data-stu-id="ddc34-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddc34-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ddc34-126">See also</span></span>



[<span data-ttu-id="ddc34-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ddc34-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ddc34-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ddc34-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ddc34-129">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="ddc34-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="ddc34-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ddc34-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ddc34-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ddc34-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

