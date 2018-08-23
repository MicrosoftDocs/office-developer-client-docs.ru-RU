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
ms.openlocfilehash: d6f5a0bd5da851c5107b8d3d40d683a7e3c1b26b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586013"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="fbd83-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="fbd83-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="fbd83-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbd83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbd83-105">Выполняет те же функции, что функцию [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) , за исключением того, что функция **HrOpenABEntryWithProviderUIDSupport** открывает запись, с помощью объекта заданного поддержки вместо использования сеанса и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="fbd83-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbd83-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fbd83-106">Header file:</span></span>  <br/> |<span data-ttu-id="fbd83-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="fbd83-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="fbd83-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="fbd83-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fbd83-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fbd83-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fbd83-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="fbd83-110">Called by:</span></span>  <br/> |<span data-ttu-id="fbd83-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="fbd83-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="fbd83-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbd83-112">Parameters</span></span>

 <span data-ttu-id="fbd83-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="fbd83-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="fbd83-114">[in] Указатель на параметр _emsabpUID_ , который определяет поставщик адресной книги Exchange, который следует использовать эту функцию для отображения сведений на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="fbd83-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="fbd83-115">Если входящий идентификатор записи не идентификатор записи адресной книги Exchange поставщика, этот параметр игнорируется и действует вызова функции аналогично [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="fbd83-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="fbd83-116">Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция также работает так же, как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="fbd83-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="fbd83-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="fbd83-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="fbd83-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fbd83-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="fbd83-119">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fbd83-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="fbd83-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fbd83-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="fbd83-121">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="fbd83-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="fbd83-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fbd83-122">_lpInterface_</span></span>
  
> <span data-ttu-id="fbd83-123">[in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который будет использоваться для доступа к открытой операцией.</span><span class="sxs-lookup"><span data-stu-id="fbd83-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="fbd83-124">Передача NULL Возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="fbd83-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="fbd83-125">Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fbd83-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="fbd83-126">Для списков рассылки, он является [IDistList: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="fbd83-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="fbd83-127">Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="fbd83-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="fbd83-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fbd83-128">_ulFlags_</span></span>
  
> <span data-ttu-id="fbd83-129">[in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="fbd83-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="fbd83-130">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="fbd83-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="fbd83-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="fbd83-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="fbd83-132">Указывает, что сведения о возвращает TRUE, если фактически изменений на адрес; в противном случае сведения о возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="fbd83-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="fbd83-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="fbd83-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="fbd83-134">Отображает модальное версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="fbd83-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="fbd83-135">Этот флаг является взаимоисключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="fbd83-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="fbd83-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="fbd83-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="fbd83-137">Отображает безрежимным версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="fbd83-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="fbd83-138">Этот флаг является взаимоисключающим с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="fbd83-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="fbd83-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fbd83-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="fbd83-140">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="fbd83-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="fbd83-141">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="fbd83-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="fbd83-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="fbd83-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="fbd83-143">[out] Указатель на тип открыт записи.</span><span class="sxs-lookup"><span data-stu-id="fbd83-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="fbd83-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="fbd83-144">_lppUnk_</span></span>
  
> <span data-ttu-id="fbd83-145">[out] Указатель на указатель открыт записи.</span><span class="sxs-lookup"><span data-stu-id="fbd83-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

