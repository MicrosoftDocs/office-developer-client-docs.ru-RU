---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808673"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="ef276-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="ef276-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="ef276-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef276-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef276-105">Возвращает идентификатор записи из глобальной адресной книги для службы Exchange, определяемую средством _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="ef276-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="ef276-106">Идентификатор записи возвращенные нужно освободить с помощью [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ef276-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef276-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ef276-107">Header file:</span></span>  <br/> |<span data-ttu-id="ef276-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="ef276-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="ef276-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="ef276-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="ef276-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="ef276-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="ef276-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="ef276-111">Called by:</span></span>  <br/> |<span data-ttu-id="ef276-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ef276-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="ef276-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef276-113">Parameters</span></span>

 <span data-ttu-id="ef276-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="ef276-114">_pSess_</span></span>
  
> <span data-ttu-id="ef276-115">[in] Система на IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="ef276-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="ef276-116">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="ef276-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ef276-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="ef276-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="ef276-118">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="ef276-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="ef276-119">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="ef276-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ef276-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="ef276-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="ef276-121">[in] Указатель на **emsmdbUID** , идентифицирующий глобального списка адресов Exchange службы нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="ef276-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="ef276-122">Если _pEmsmdbUID_ имеет значение NULL или ноль UID, эта функция возвращает прежних версий из глобального списка адресов службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef276-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="ef276-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="ef276-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="ef276-124">[out] Указатель на количество байтов идентификатор записи из глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="ef276-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="ef276-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="ef276-125">_lppeid_</span></span>
  
> <span data-ttu-id="ef276-126">[out] Указатель на идентификатор записи из глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="ef276-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="ef276-127">Это нужно освободить с помощью [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ef276-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

