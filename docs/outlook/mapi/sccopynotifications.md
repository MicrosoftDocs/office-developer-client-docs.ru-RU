---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435924"
---
# <a name="sccopynotifications"></a><span data-ttu-id="de4d7-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="de4d7-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="de4d7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de4d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de4d7-105">Копирует группу уведомлений о событиях в один блок памяти.</span><span class="sxs-lookup"><span data-stu-id="de4d7-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de4d7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="de4d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="de4d7-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="de4d7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="de4d7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="de4d7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="de4d7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="de4d7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="de4d7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="de4d7-110">Called by:</span></span>  <br/> |<span data-ttu-id="de4d7-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="de4d7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="de4d7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="de4d7-112">Parameters</span></span>

 <span data-ttu-id="de4d7-113">_кнтф_</span><span class="sxs-lookup"><span data-stu-id="de4d7-113">_cntf_</span></span>
  
> <span data-ttu-id="de4d7-114">возврата Количество структур [уведомлений](notification.md) в массиве, указанном с помощью параметра _ргнтф_ .</span><span class="sxs-lookup"><span data-stu-id="de4d7-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="de4d7-115">_ргнтф_</span><span class="sxs-lookup"><span data-stu-id="de4d7-115">_rgntf_</span></span>
  
> <span data-ttu-id="de4d7-116">возврата Указатель на массив структуры **уведомлений** , определяющий копируемые уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="de4d7-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="de4d7-117">_пвдст_</span><span class="sxs-lookup"><span data-stu-id="de4d7-117">_pvDst_</span></span>
  
> <span data-ttu-id="de4d7-118">вышли Указатель на возвращенные уведомления.</span><span class="sxs-lookup"><span data-stu-id="de4d7-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="de4d7-119">_пкб_</span><span class="sxs-lookup"><span data-stu-id="de4d7-119">_pcb_</span></span>
  
> <span data-ttu-id="de4d7-120">вышли Необязательный указатель на переменную, в которой хранится размер массива (в байтах), на который указывает параметр _ргнтф_ .</span><span class="sxs-lookup"><span data-stu-id="de4d7-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="de4d7-121">Если значение не равно NULL, параметр _ПКБ_ имеет значение, равное числу байтов, хранящихся в параметре _пвдст_ .</span><span class="sxs-lookup"><span data-stu-id="de4d7-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="de4d7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de4d7-122">Return value</span></span>

<span data-ttu-id="de4d7-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="de4d7-123">S_OK</span></span>
  
> <span data-ttu-id="de4d7-124">Уведомления о событиях успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="de4d7-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="de4d7-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="de4d7-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="de4d7-126">Обнаружено недопустимое уведомление.</span><span class="sxs-lookup"><span data-stu-id="de4d7-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de4d7-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="de4d7-127">Remarks</span></span>

<span data-ttu-id="de4d7-128">Если в параметре _ПКБ_ передается значение null, копирование не выполняется; Если в _ПКБ_передается значение, отличное от NULL, функция **сккопинотификатионс** копирует размер массива и самого массива в один блок памяти.</span><span class="sxs-lookup"><span data-stu-id="de4d7-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="de4d7-129">Если _ПКБ_ не равно null, для него задается число байтов, хранящихся в параметре _пвдст_ .</span><span class="sxs-lookup"><span data-stu-id="de4d7-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="de4d7-130">Параметр _пвдст_ должен быть достаточно большим, чтобы вместить весь массив.</span><span class="sxs-lookup"><span data-stu-id="de4d7-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

