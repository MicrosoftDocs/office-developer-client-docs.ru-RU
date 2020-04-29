---
title: Неинициализированное состояние
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425563"
---
# <a name="uninitialized-state"></a><span data-ttu-id="08ee5-103">Неинициализированное состояние</span><span class="sxs-lookup"><span data-stu-id="08ee5-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="08ee5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08ee5-105">Неинициализированное состояние — это начальные объекты формы состояния, которые должны находиться в момент создания.</span><span class="sxs-lookup"><span data-stu-id="08ee5-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="08ee5-106">Объекты Form инициализируются данными сообщений, когда клиентское приложение вызывает метод [иперсистмессаже:: инитнев](ipersistmessage-initnew.md) или [Иперсистмессаже:: Load](ipersistmessage-load.md) объекта Form.</span><span class="sxs-lookup"><span data-stu-id="08ee5-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="08ee5-107">В следующей таблице описаны допустимые переходы из состояния Унитиализед.</span><span class="sxs-lookup"><span data-stu-id="08ee5-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="08ee5-108">**Метод Иперсистмессаже**</span><span class="sxs-lookup"><span data-stu-id="08ee5-108">**IPersistMessage method**</span></span>|<span data-ttu-id="08ee5-109">**Действие**</span><span class="sxs-lookup"><span data-stu-id="08ee5-109">**Action**</span></span>|<span data-ttu-id="08ee5-110">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="08ee5-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08ee5-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="08ee5-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="08ee5-112">Загрузка объекта Form с данными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08ee5-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="08ee5-113">Normal</span><span class="sxs-lookup"><span data-stu-id="08ee5-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="08ee5-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="08ee5-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="08ee5-115">Загрузка объекта Form с данными из целевого сообщения.</span><span class="sxs-lookup"><span data-stu-id="08ee5-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="08ee5-116">Normal</span><span class="sxs-lookup"><span data-stu-id="08ee5-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="08ee5-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="08ee5-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="08ee5-118">Возвратите сообщение об успешном выполнении или присвойте последней ошибке и возвратите E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="08ee5-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="08ee5-119">Неинициализированное</span><span class="sxs-lookup"><span data-stu-id="08ee5-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="08ee5-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="08ee5-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="08ee5-121">Возврат последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="08ee5-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="08ee5-122">Неинициализированное</span><span class="sxs-lookup"><span data-stu-id="08ee5-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="08ee5-123">Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="08ee5-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="08ee5-124">Установка последней ошибки и возврат E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="08ee5-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="08ee5-125">Неинициализированное</span><span class="sxs-lookup"><span data-stu-id="08ee5-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08ee5-126">См. также</span><span class="sxs-lookup"><span data-stu-id="08ee5-126">See also</span></span>



[<span data-ttu-id="08ee5-127">Нормальное состояние</span><span class="sxs-lookup"><span data-stu-id="08ee5-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="08ee5-128">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="08ee5-128">Form States</span></span>](form-states.md)

