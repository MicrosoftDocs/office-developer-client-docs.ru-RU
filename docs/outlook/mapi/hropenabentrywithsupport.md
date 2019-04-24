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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347763"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="12857-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="12857-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="12857-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12857-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12857-105">Не используйте эту функцию.</span><span class="sxs-lookup"><span data-stu-id="12857-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12857-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="12857-106">Header file:</span></span>  <br/> |<span data-ttu-id="12857-107">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="12857-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="12857-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="12857-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="12857-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="12857-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="12857-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="12857-110">Called by:</span></span>  <br/> |<span data-ttu-id="12857-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="12857-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="12857-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="12857-112">Parameters</span></span>

 <span data-ttu-id="12857-113">_Лпсуп_</span><span class="sxs-lookup"><span data-stu-id="12857-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="12857-114">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="12857-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="12857-115">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="12857-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="12857-116">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="12857-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="12857-117">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="12857-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="12857-118">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="12857-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="12857-119">возврата Указатель на идентификатор интерфейса (IID) интерфейса, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="12857-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="12857-120">При передаче значения NULL возвращается стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="12857-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="12857-121">Для пользователей обмена сообщениями стандартный интерфейс — [имаилусер: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="12857-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="12857-122">Для списков рассылки это [идистлист: IMAPIContainer](idistlistimapicontainer.md), а для контейнеров — [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="12857-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="12857-123">Вызывающие абоненты могут установить _лпинтерфаце_ в соответствии со стандартным интерфейсом или интерфейсом в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="12857-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="12857-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="12857-124">_ulFlags_</span></span>
  
> <span data-ttu-id="12857-125">возврата Битовая маска флагов, определяющая тип текста для параметра _лпсзбуттонтекст_ .</span><span class="sxs-lookup"><span data-stu-id="12857-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="12857-126">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="12857-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="12857-127">АБ_ТЕЛЛ_ДЕТАИЛС_ЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="12857-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="12857-128">Указывает, что Details возвращает TRUE, если изменения фактически вносятся в адрес; в противном случае сведения возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="12857-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="12857-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="12857-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="12857-130">Отображает модальную версию диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="12857-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="12857-131">Этот флаг является взаимно исключающим с ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="12857-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="12857-132">ДИАЛОГ_СДИ</span><span class="sxs-lookup"><span data-stu-id="12857-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="12857-133">Отображает немодальную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="12857-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="12857-134">Этот флаг является взаимно исключающим с ДИАЛОГ_МОДАЛ.</span><span class="sxs-lookup"><span data-stu-id="12857-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="12857-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="12857-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="12857-136">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="12857-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="12857-137">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="12857-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="12857-138">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="12857-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="12857-139">вышли Указатель на тип открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="12857-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="12857-140">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="12857-140">_lppUnk_</span></span>
  
> <span data-ttu-id="12857-141">вышли Указатель на указатель открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="12857-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

