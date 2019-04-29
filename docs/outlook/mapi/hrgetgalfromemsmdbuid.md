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
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="ee8fa-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="ee8fa-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="ee8fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee8fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee8fa-105">Возвращает идентификатор глобальной адресной книги для службы Exchange, идентифицируемой _пемсмдбуид_.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="ee8fa-106">Возвращенный идентификатор элемента должен быть освобожден с помощью [мапифрибуффер](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ee8fa-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee8fa-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ee8fa-107">Header file:</span></span>  <br/> |<span data-ttu-id="ee8fa-108">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="ee8fa-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="ee8fa-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ee8fa-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee8fa-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee8fa-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee8fa-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ee8fa-111">Called by:</span></span>  <br/> |<span data-ttu-id="ee8fa-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ee8fa-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="ee8fa-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee8fa-113">Parameters</span></span>

 <span data-ttu-id="ee8fa-114">_Псесс_</span><span class="sxs-lookup"><span data-stu-id="ee8fa-114">_pSess_</span></span>
  
> <span data-ttu-id="ee8fa-115">возврата Вошедший в систему IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="ee8fa-116">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ee8fa-117">_Паддрбук_</span><span class="sxs-lookup"><span data-stu-id="ee8fa-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="ee8fa-118">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="ee8fa-119">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ee8fa-120">_Пемсмдбуид_</span><span class="sxs-lookup"><span data-stu-id="ee8fa-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="ee8fa-121">возврата Указатель на **емсмдбуид** , ОПРЕДЕЛЯЮЩий глобальную коллекцию адресов, которую необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="ee8fa-122">Если _пемсмдбуид_ имеет значение null или нулевой UID, эта функция получает глобальный список адресов (GAL) устаревшей службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="ee8fa-123">_лпкбеид_</span><span class="sxs-lookup"><span data-stu-id="ee8fa-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="ee8fa-124">вышли Указатель на число байтов идентификатора записи глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="ee8fa-125">_лппеид_</span><span class="sxs-lookup"><span data-stu-id="ee8fa-125">_lppeid_</span></span>
  
> <span data-ttu-id="ee8fa-126">вышли Указатель на идентификатор элемента глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="ee8fa-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="ee8fa-127">Его следует освободить с помощью [мапифрибуффер](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ee8fa-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

