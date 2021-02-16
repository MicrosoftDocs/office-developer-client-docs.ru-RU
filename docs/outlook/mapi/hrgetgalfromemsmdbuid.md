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
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439109"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="27666-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="27666-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="27666-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27666-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27666-105">Возвращает идентификатор записи глобальной адресной книги для службы Exchange, определяемой _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="27666-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="27666-106">Возвращаемого идентификатора записи следует освободить с помощью [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="27666-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27666-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="27666-107">Header file:</span></span>  <br/> |<span data-ttu-id="27666-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="27666-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="27666-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="27666-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="27666-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="27666-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="27666-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="27666-111">Called by:</span></span>  <br/> |<span data-ttu-id="27666-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="27666-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="27666-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="27666-113">Parameters</span></span>

 <span data-ttu-id="27666-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="27666-114">_pSess_</span></span>
  
> <span data-ttu-id="27666-115">[in] Во время входа в систему IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="27666-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="27666-116">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="27666-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="27666-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="27666-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="27666-118">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="27666-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="27666-119">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="27666-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="27666-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="27666-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="27666-121">[in] Указатель на **emsmdbUID,** который определяет gal извлекаемой службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="27666-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="27666-122">Если  _pEmsmdbUID_ имеет значение NULL или нулевое значение UID, эта функция получает устаревший gal службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="27666-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="27666-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="27666-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="27666-124">[out] Указатель на количество byte идентификатора записи глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="27666-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="27666-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="27666-125">_lppeid_</span></span>
  
> <span data-ttu-id="27666-126">[out] Указатель на идентификатор записи глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="27666-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="27666-127">Его следует освободить с помощью [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="27666-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

