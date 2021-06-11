---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409547"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="a7a7d-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="a7a7d-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="a7a7d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7a7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7a7d-105">Выполняет ту же функцию, что и функция [HrOpenABEntryWithProviderUID,](hropenabentrywithprovideruid.md) за исключением того, что функция **HrOpenABEntryWithProviderUIDSupport** открывает запись с помощью данного объекта поддержки вместо сеанса и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7a7d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a7a7d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a7a7d-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="a7a7d-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a7a7d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a7a7d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a7a7d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a7a7d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a7a7d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a7a7d-110">Called by:</span></span>  <br/> |<span data-ttu-id="a7a7d-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a7a7d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="a7a7d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a7a7d-112">Parameters</span></span>

 <span data-ttu-id="a7a7d-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="a7a7d-114">[in] Указатель на параметр _emsabpUID,_ который определяет поставщика адресной книги Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="a7a7d-115">Если идентификатор входной записи не является идентификатором записи поставщика Exchange адресной книги, этот параметр игнорируется, и вызов функции действует точно так же, как [iAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a7a7d-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="a7a7d-116">Если этот параметр является NULL или нулевой MAPIUID, эта функция также действует точно так же, как [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a7a7d-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="a7a7d-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="a7a7d-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="a7a7d-119">[in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a7a7d-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="a7a7d-121">[in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="a7a7d-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-122">_lpInterface_</span></span>
  
> <span data-ttu-id="a7a7d-123">[in] Указатель на идентификатор интерфейса (IID) интерфейса, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="a7a7d-124">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a7a7d-125">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a7a7d-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a7a7d-126">Для списков рассылки это [IDistList: IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров [— IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a7a7d-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a7a7d-127">Звонители могут настроить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a7a7d-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-128">_ulFlags_</span></span>
  
> <span data-ttu-id="a7a7d-129">[in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="a7a7d-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="a7a7d-130">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a7a7d-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="a7a7d-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a7a7d-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="a7a7d-132">Указывает, что Details возвращает TRUE, если на самом деле в адрес внесены изменения; в противном случае Details возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="a7a7d-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="a7a7d-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="a7a7d-134">Отображает модную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="a7a7d-135">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="a7a7d-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="a7a7d-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="a7a7d-137">Отображает бес режимную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="a7a7d-138">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="a7a7d-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a7a7d-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="a7a7d-140">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a7a7d-141">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a7a7d-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="a7a7d-143">[вышел] Указатель на тип открываемой записи.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a7a7d-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a7a7d-144">_lppUnk_</span></span>
  
> <span data-ttu-id="a7a7d-145">[вышел] Указатель на указатель открываемой записи.</span><span class="sxs-lookup"><span data-stu-id="a7a7d-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

