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
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419900"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="41a98-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="41a98-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="41a98-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41a98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41a98-105">Возвращает идентификатор входа контейнера, назначенного в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="41a98-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="41a98-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="41a98-106">Parameters</span></span>

 <span data-ttu-id="41a98-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="41a98-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="41a98-108">[вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="41a98-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="41a98-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="41a98-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="41a98-110">[вышел] Указатель на указатель на идентификатор записи PAB.</span><span class="sxs-lookup"><span data-stu-id="41a98-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="41a98-111">Параметр  _lppEntryID содержит_ ноль, если контейнер не назначен как PAB.</span><span class="sxs-lookup"><span data-stu-id="41a98-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41a98-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41a98-112">Return value</span></span>

<span data-ttu-id="41a98-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="41a98-113">S_OK</span></span> 
  
> <span data-ttu-id="41a98-114">Идентификатор записи PAB был успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="41a98-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41a98-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="41a98-115">Remarks</span></span>

<span data-ttu-id="41a98-116">Клиенты звонят **методу GetPAB,** чтобы получить идентификатор входа контейнера, назначенного как PAB.</span><span class="sxs-lookup"><span data-stu-id="41a98-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="41a98-117">Если PAB не установлен в профиле, MAPI выбирает в качестве PAB первый контейнер в иерархии адресной книги, который позволяет вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="41a98-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41a98-118">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="41a98-118">MFCMAPI reference</span></span>

<span data-ttu-id="41a98-119">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="41a98-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41a98-120">**Файл**</span><span class="sxs-lookup"><span data-stu-id="41a98-120">**File**</span></span>|<span data-ttu-id="41a98-121">**Функция**</span><span class="sxs-lookup"><span data-stu-id="41a98-121">**Function**</span></span>|<span data-ttu-id="41a98-122">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="41a98-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41a98-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="41a98-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="41a98-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="41a98-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="41a98-125">MFCMAPI использует **метод GetPAB** для получения ID для личной адресной книги пользователя.</span><span class="sxs-lookup"><span data-stu-id="41a98-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41a98-126">См. также</span><span class="sxs-lookup"><span data-stu-id="41a98-126">See also</span></span>



[<span data-ttu-id="41a98-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="41a98-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="41a98-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="41a98-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="41a98-129">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="41a98-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="41a98-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="41a98-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="41a98-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="41a98-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

