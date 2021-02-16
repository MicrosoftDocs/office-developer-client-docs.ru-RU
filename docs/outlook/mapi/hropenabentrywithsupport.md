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
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417646"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="fc4b9-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="fc4b9-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="fc4b9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc4b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc4b9-105">Не используйте эту функцию.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc4b9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fc4b9-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc4b9-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="fc4b9-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="fc4b9-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="fc4b9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc4b9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc4b9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc4b9-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="fc4b9-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc4b9-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="fc4b9-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="fc4b9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc4b9-112">Parameters</span></span>

 <span data-ttu-id="fc4b9-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="fc4b9-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="fc4b9-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fc4b9-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="fc4b9-115">[in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="fc4b9-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="fc4b9-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fc4b9-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="fc4b9-117">[in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="fc4b9-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fc4b9-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="fc4b9-119">[in] Указатель на идентификатор интерфейса, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="fc4b9-120">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="fc4b9-121">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fc4b9-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="fc4b9-122">Для списков рассылки это [IDistList : IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров это [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="fc4b9-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="fc4b9-123">Вызывающие могут установить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="fc4b9-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc4b9-124">_ulFlags_</span></span>
  
> <span data-ttu-id="fc4b9-125">[in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="fc4b9-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="fc4b9-126">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="fc4b9-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="fc4b9-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="fc4b9-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="fc4b9-128">Указывает, что details возвращает true, если фактически в адрес были внесены изменения; в противном случае details возвращает false.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="fc4b9-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="fc4b9-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="fc4b9-130">Отображает модальные версии общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="fc4b9-131">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="fc4b9-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="fc4b9-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="fc4b9-133">Отображает неавтомтную версию общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="fc4b9-134">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="fc4b9-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fc4b9-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="fc4b9-136">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="fc4b9-137">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="fc4b9-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="fc4b9-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="fc4b9-139">[out] Указатель на тип открытой записи.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="fc4b9-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="fc4b9-140">_lppUnk_</span></span>
  
> <span data-ttu-id="fc4b9-141">[out] Указатель на указатель открытой записи.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

