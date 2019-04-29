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
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="52a3e-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="52a3e-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="52a3e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52a3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52a3e-105">Выполняет ту же функцию, что и функция [хропенабентривиспровидеруид](hropenabentrywithprovideruid.md) , за исключением того, что функция **хропенабентривиспровидеруидсуппорт** открывает запись, используя указанный объект поддержки, а не сеанс и адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="52a3e-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52a3e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="52a3e-106">Header file:</span></span>  <br/> |<span data-ttu-id="52a3e-107">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="52a3e-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="52a3e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="52a3e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="52a3e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="52a3e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="52a3e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="52a3e-110">Called by:</span></span>  <br/> |<span data-ttu-id="52a3e-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="52a3e-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="52a3e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="52a3e-112">Parameters</span></span>

 <span data-ttu-id="52a3e-113">_Пемсабпуид_</span><span class="sxs-lookup"><span data-stu-id="52a3e-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="52a3e-114">возврата Указатель на параметр _емсабпуид_ , определяющий поставщика адресных книг Exchange, который должна использовать эта функция для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="52a3e-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="52a3e-115">Если входящий идентификатор записи не является идентификатором записи поставщика адресных книг Exchange, этот параметр игнорируется, а вызов функции выполняется точно так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="52a3e-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="52a3e-116">Если этот параметр имеет значение NULL или нулевой МАПИУИД, эта функция также работает точно так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="52a3e-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="52a3e-117">_Лпсуп_</span><span class="sxs-lookup"><span data-stu-id="52a3e-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="52a3e-118">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="52a3e-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="52a3e-119">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="52a3e-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="52a3e-120">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="52a3e-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="52a3e-121">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="52a3e-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="52a3e-122">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="52a3e-122">_lpInterface_</span></span>
  
> <span data-ttu-id="52a3e-123">возврата Указатель на идентификатор интерфейса (IID) интерфейса, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="52a3e-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="52a3e-124">При передаче значения NULL возвращается стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="52a3e-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="52a3e-125">Для пользователей обмена сообщениями стандартный интерфейс — [имаилусер: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="52a3e-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="52a3e-126">Для списков рассылки это [идистлист: IMAPIContainer](idistlistimapicontainer.md), а для контейнеров — [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="52a3e-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="52a3e-127">Вызывающие абоненты могут установить _лпинтерфаце_ в соответствии со стандартным интерфейсом или интерфейсом в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="52a3e-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="52a3e-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52a3e-128">_ulFlags_</span></span>
  
> <span data-ttu-id="52a3e-129">возврата Битовая маска флагов, определяющая тип текста для параметра _лпсзбуттонтекст_ .</span><span class="sxs-lookup"><span data-stu-id="52a3e-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="52a3e-130">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="52a3e-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="52a3e-131">АБ_ТЕЛЛ_ДЕТАИЛС_ЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="52a3e-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="52a3e-132">Указывает, что Details возвращает TRUE, если изменения фактически вносятся в адрес; в противном случае сведения возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="52a3e-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="52a3e-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="52a3e-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="52a3e-134">Отображает модальную версию диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="52a3e-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="52a3e-135">Этот флаг является взаимно исключающим с ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="52a3e-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="52a3e-136">ДИАЛОГ_СДИ</span><span class="sxs-lookup"><span data-stu-id="52a3e-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="52a3e-137">Отображает немодальную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="52a3e-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="52a3e-138">Этот флаг является взаимно исключающим с ДИАЛОГ_МОДАЛ.</span><span class="sxs-lookup"><span data-stu-id="52a3e-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="52a3e-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="52a3e-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="52a3e-140">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="52a3e-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="52a3e-141">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="52a3e-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="52a3e-142">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="52a3e-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="52a3e-143">вышли Указатель на тип открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="52a3e-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="52a3e-144">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="52a3e-144">_lppUnk_</span></span>
  
> <span data-ttu-id="52a3e-145">вышли Указатель на указатель открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="52a3e-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

