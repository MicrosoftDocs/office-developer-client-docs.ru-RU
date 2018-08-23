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
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578250"
---
# <a name="uninitialized-state"></a><span data-ttu-id="a7ad9-103">Неинициализированное состояние</span><span class="sxs-lookup"><span data-stu-id="a7ad9-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="a7ad9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7ad9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7ad9-105">Неинициализированная переменная состояние — исходное состояние формы, в которой должны быть объекты при первом создании.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="a7ad9-106">Объекты формы становятся инициализирован с данными сообщения при клиентского приложения вызывается метод [IPersistMessage::InitNew](ipersistmessage-initnew.md) или [IPersistMessage::Load](ipersistmessage-load.md) объекта формы.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="a7ad9-107">В следующей таблице описываются допустимые переходы из состояния Unitialized.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="a7ad9-108">**Метод IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="a7ad9-108">**IPersistMessage method**</span></span>|<span data-ttu-id="a7ad9-109">**Действие**</span><span class="sxs-lookup"><span data-stu-id="a7ad9-109">**Action**</span></span>|<span data-ttu-id="a7ad9-110">**Новое состояние**</span><span class="sxs-lookup"><span data-stu-id="a7ad9-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a7ad9-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="a7ad9-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="a7ad9-112">Загрузите объект формы с данными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="a7ad9-113">Normal</span><span class="sxs-lookup"><span data-stu-id="a7ad9-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="a7ad9-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="a7ad9-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="a7ad9-115">Загрузите объект формы с данными из целевого сообщения.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="a7ad9-116">Normal</span><span class="sxs-lookup"><span data-stu-id="a7ad9-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="a7ad9-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="a7ad9-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="a7ad9-118">Возвращает успешно, или значение последней ошибки и возвратить значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="a7ad9-119">Неинициализированная переменная</span><span class="sxs-lookup"><span data-stu-id="a7ad9-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="a7ad9-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a7ad9-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="a7ad9-121">Возвращает последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="a7ad9-122">Неинициализированная переменная</span><span class="sxs-lookup"><span data-stu-id="a7ad9-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="a7ad9-123">Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов</span><span class="sxs-lookup"><span data-stu-id="a7ad9-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="a7ad9-124">Значение последней ошибки и возвратить значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="a7ad9-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="a7ad9-125">Неинициализированная переменная</span><span class="sxs-lookup"><span data-stu-id="a7ad9-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7ad9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a7ad9-126">See also</span></span>



[<span data-ttu-id="a7ad9-127">Обычное состояние</span><span class="sxs-lookup"><span data-stu-id="a7ad9-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="a7ad9-128">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="a7ad9-128">Form States</span></span>](form-states.md)

