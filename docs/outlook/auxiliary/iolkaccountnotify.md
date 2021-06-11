---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412501"
---
# <a name="iolkaccountnotify"></a><span data-ttu-id="7686f-102">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="7686f-102">IOlkAccountNotify</span></span>

<span data-ttu-id="7686f-103">Предоставляет клиенту вызов для изменения учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7686f-103">Provides a callback to the client for changes to an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7686f-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7686f-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7686f-105">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="7686f-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="7686f-106">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="7686f-106">IOlkErrorUnknown</span></span>](iolkerrorunknown.md) <br/> |
|<span data-ttu-id="7686f-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="7686f-107">Provided by:</span></span>  <br/> | <span data-ttu-id="7686f-108">Клиент</span><span class="sxs-lookup"><span data-stu-id="7686f-108">Client</span></span>  <br/> |
|<span data-ttu-id="7686f-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="7686f-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7686f-110">IID_IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="7686f-110">IID_IOlkAccountNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7686f-111">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="7686f-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7686f-112">Уведомить</span><span class="sxs-lookup"><span data-stu-id="7686f-112">Notify</span></span>](iolkaccountnotify-notify.md) <br/> |<span data-ttu-id="7686f-113">Сообщает клиенту об изменениях указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7686f-113">Notifies the client of changes to the specified account.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7686f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7686f-114">Remarks</span></span>

<span data-ttu-id="7686f-115">Этот интерфейс передается [в IOlkAccountManager::Advise](iolkaccountmanager-advise.md) при настройке уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7686f-115">This interface is passed to [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) when setting up notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7686f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7686f-116">See also</span></span>

- [<span data-ttu-id="7686f-117">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="7686f-117">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="7686f-118">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="7686f-118">Constants (Account management API)</span></span>](constants-account-management-api.md)

