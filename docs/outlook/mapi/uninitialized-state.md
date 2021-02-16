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
# <a name="uninitialized-state"></a><span data-ttu-id="237f1-103">Неинициализированное состояние</span><span class="sxs-lookup"><span data-stu-id="237f1-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="237f1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="237f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="237f1-105">Неинициализированное состояние — это объекты формы начального состояния, которые должны быть созданы при их первом создания.</span><span class="sxs-lookup"><span data-stu-id="237f1-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="237f1-106">Объекты форм инициализируются с данными сообщения при вызове клиентского приложения [методом IPersistMessage::InitNew](ipersistmessage-initnew.md) или [IPersistMessage::Load](ipersistmessage-load.md) в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="237f1-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="237f1-107">В следующей таблице описаны разрешенные переходы из состояния "Unitialized".</span><span class="sxs-lookup"><span data-stu-id="237f1-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="237f1-108">**Метод IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="237f1-108">**IPersistMessage method**</span></span>|<span data-ttu-id="237f1-109">**Действие**</span><span class="sxs-lookup"><span data-stu-id="237f1-109">**Action**</span></span>|<span data-ttu-id="237f1-110">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="237f1-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="237f1-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="237f1-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="237f1-112">Загрузка объекта формы с данными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="237f1-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="237f1-113">Normal</span><span class="sxs-lookup"><span data-stu-id="237f1-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="237f1-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="237f1-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="237f1-115">Загрузка объекта формы с данными из целевого сообщения.</span><span class="sxs-lookup"><span data-stu-id="237f1-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="237f1-116">Normal</span><span class="sxs-lookup"><span data-stu-id="237f1-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="237f1-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="237f1-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="237f1-118">Возврат успеха или настройка последней ошибки и возврат E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="237f1-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="237f1-119">Неинициализировано</span><span class="sxs-lookup"><span data-stu-id="237f1-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="237f1-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="237f1-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="237f1-121">Возвращает последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="237f1-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="237f1-122">Неинициализировано</span><span class="sxs-lookup"><span data-stu-id="237f1-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="237f1-123">Другие [методы IPersistMessage : методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="237f1-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="237f1-124">Установите последнюю ошибку и E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="237f1-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="237f1-125">Неинициализировано</span><span class="sxs-lookup"><span data-stu-id="237f1-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="237f1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="237f1-126">See also</span></span>



[<span data-ttu-id="237f1-127">Нормальное состояние</span><span class="sxs-lookup"><span data-stu-id="237f1-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="237f1-128">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="237f1-128">Form States</span></span>](form-states.md)

