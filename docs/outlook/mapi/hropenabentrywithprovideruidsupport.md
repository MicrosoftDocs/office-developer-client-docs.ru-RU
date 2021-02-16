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
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="cc921-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="cc921-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="cc921-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc921-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc921-105">Выполняет ту же функцию, что и функция [HrOpenABEntryWithProviderUID,](hropenabentrywithprovideruid.md) за исключением того, что функция **HrOpenABEntryWithProviderUIDSupport** открывает запись с использованием заданного объекта поддержки, а не сеанса и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cc921-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc921-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cc921-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc921-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="cc921-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="cc921-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cc921-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cc921-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc921-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc921-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cc921-110">Called by:</span></span>  <br/> |<span data-ttu-id="cc921-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="cc921-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="cc921-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc921-112">Parameters</span></span>

 <span data-ttu-id="cc921-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="cc921-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="cc921-114">[in] Указатель на параметр  _emsabpUID,_ который определяет поставщика адресной книги Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="cc921-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="cc921-115">Если идентификатор входной записи не является идентификатором записи поставщика адресной книги Exchange, этот параметр игнорируется, и вызов функции действует точно так же, как [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="cc921-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="cc921-116">Если этот параметр имеет значение NULL или mapIUID нулевого уровня, эта функция также действует точно так же, как [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="cc921-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="cc921-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="cc921-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="cc921-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="cc921-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="cc921-119">[in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="cc921-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="cc921-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="cc921-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="cc921-121">[in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cc921-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="cc921-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="cc921-122">_lpInterface_</span></span>
  
> <span data-ttu-id="cc921-123">[in] Указатель на идентификатор интерфейса, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="cc921-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="cc921-124">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="cc921-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="cc921-125">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="cc921-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="cc921-126">Для списков рассылки это [IDistList : IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="cc921-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="cc921-127">Вызывающие могут установить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="cc921-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="cc921-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cc921-128">_ulFlags_</span></span>
  
> <span data-ttu-id="cc921-129">[in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="cc921-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="cc921-130">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="cc921-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="cc921-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="cc921-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="cc921-132">Указывает, что details возвращает true, если фактически в адрес были внесены изменения; в противном случае details возвращает false.</span><span class="sxs-lookup"><span data-stu-id="cc921-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="cc921-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="cc921-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="cc921-134">Отображает модальной версии диалоговое окно общего адреса.</span><span class="sxs-lookup"><span data-stu-id="cc921-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="cc921-135">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="cc921-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="cc921-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="cc921-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="cc921-137">Отображает неавтомтную версию общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="cc921-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="cc921-138">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="cc921-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="cc921-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cc921-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="cc921-140">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="cc921-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="cc921-141">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="cc921-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="cc921-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="cc921-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="cc921-143">[out] Указатель на тип открытой записи.</span><span class="sxs-lookup"><span data-stu-id="cc921-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="cc921-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="cc921-144">_lppUnk_</span></span>
  
> <span data-ttu-id="cc921-145">[out] Указатель на указатель открытой записи.</span><span class="sxs-lookup"><span data-stu-id="cc921-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

