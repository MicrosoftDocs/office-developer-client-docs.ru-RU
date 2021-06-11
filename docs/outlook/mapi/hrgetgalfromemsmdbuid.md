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
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="5141b-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="5141b-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="5141b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5141b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5141b-105">Возвращает идентификатор записи глобальной адресной книги для Exchange службы _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="5141b-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="5141b-106">Идентификатор возвращаемой записи должен быть освобожден с помощью [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="5141b-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5141b-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5141b-107">Header file:</span></span>  <br/> |<span data-ttu-id="5141b-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="5141b-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="5141b-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5141b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5141b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5141b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5141b-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5141b-111">Called by:</span></span>  <br/> |<span data-ttu-id="5141b-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="5141b-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="5141b-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="5141b-113">Parameters</span></span>

 <span data-ttu-id="5141b-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="5141b-114">_pSess_</span></span>
  
> <span data-ttu-id="5141b-115">[in] Вход в систему IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="5141b-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="5141b-116">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="5141b-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5141b-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="5141b-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="5141b-118">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="5141b-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="5141b-119">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="5141b-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5141b-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="5141b-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="5141b-121">[in] Указатель на **emsmdbUID,** который определяет gal службы Exchange, которая должна быть извлечена.</span><span class="sxs-lookup"><span data-stu-id="5141b-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="5141b-122">Если _pEmsmdbUID_ является NULL или нулевой UID, эта функция получает устаревшую ГАЛ службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="5141b-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="5141b-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="5141b-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="5141b-124">[вышел] Указатель на количество byte идентификатора входа глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="5141b-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="5141b-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="5141b-125">_lppeid_</span></span>
  
> <span data-ttu-id="5141b-126">[вышел] Указатель на идентификатор записи глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="5141b-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="5141b-127">Это должно быть освобождено с [помощью MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="5141b-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

