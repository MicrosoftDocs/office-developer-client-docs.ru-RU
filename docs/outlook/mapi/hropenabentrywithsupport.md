---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808706"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="d582e-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="d582e-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="d582e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d582e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d582e-105">Эта функция не используется.</span><span class="sxs-lookup"><span data-stu-id="d582e-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d582e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d582e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d582e-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="d582e-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d582e-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d582e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d582e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d582e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d582e-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d582e-110">Called by:</span></span>  <br/> |<span data-ttu-id="d582e-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="d582e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="d582e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d582e-112">Parameters</span></span>

 <span data-ttu-id="d582e-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="d582e-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="d582e-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d582e-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="d582e-115">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d582e-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d582e-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d582e-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="d582e-117">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="d582e-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="d582e-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d582e-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="d582e-119">[in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который будет использоваться для доступа к открытой операцией.</span><span class="sxs-lookup"><span data-stu-id="d582e-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="d582e-120">Передача NULL Возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="d582e-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="d582e-121">Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="d582e-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="d582e-122">Для списков рассылки — это [IDistList: IMAPIContainer](idistlistimapicontainer.md), и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="d582e-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="d582e-123">Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="d582e-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="d582e-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d582e-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d582e-125">[in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="d582e-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="d582e-126">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="d582e-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="d582e-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="d582e-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="d582e-128">Указывает, что сведения о возвращает TRUE, если фактически изменений на адрес; в противном случае сведения о возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="d582e-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="d582e-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d582e-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="d582e-130">Отображает модальное версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="d582e-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="d582e-131">Этот флаг является взаимоисключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="d582e-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="d582e-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="d582e-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="d582e-133">Отображает безрежимным версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="d582e-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="d582e-134">Этот флаг является взаимоисключающим с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="d582e-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="d582e-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d582e-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d582e-136">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="d582e-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d582e-137">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d582e-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d582e-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="d582e-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="d582e-139">[out] Указатель на тип открыт записи.</span><span class="sxs-lookup"><span data-stu-id="d582e-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="d582e-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="d582e-140">_lppUnk_</span></span>
  
> <span data-ttu-id="d582e-141">[out] Указатель на указатель открыт записи.</span><span class="sxs-lookup"><span data-stu-id="d582e-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

