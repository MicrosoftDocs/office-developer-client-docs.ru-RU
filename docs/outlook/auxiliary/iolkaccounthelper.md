---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322157"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="e68c0-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="e68c0-102">IOlkAccountHelper</span></span>

<span data-ttu-id="e68c0-103">Предоставляет вспомогательные функциональные возможности в текущем сеансе MAPI для управления учетными записями.</span><span class="sxs-lookup"><span data-stu-id="e68c0-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e68c0-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e68c0-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e68c0-105">Наследование от:</span><span class="sxs-lookup"><span data-stu-id="e68c0-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="e68c0-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e68c0-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e68c0-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="e68c0-107">Provided by:</span></span>  <br/> |<span data-ttu-id="e68c0-108">Client</span><span class="sxs-lookup"><span data-stu-id="e68c0-108">Client</span></span>  <br/> |
|<span data-ttu-id="e68c0-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e68c0-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e68c0-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="e68c0-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e68c0-111">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="e68c0-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e68c0-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="e68c0-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="e68c0-113">*Этот элемент является заполнителем и не поддерживается.*</span><span class="sxs-lookup"><span data-stu-id="e68c0-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="e68c0-114">Идентификация по длинности</span><span class="sxs-lookup"><span data-stu-id="e68c0-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="e68c0-115">Получает имя профиля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e68c0-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="e68c0-116">жетмаписессион</span><span class="sxs-lookup"><span data-stu-id="e68c0-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="e68c0-117">Открывает сеанс MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e68c0-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="e68c0-118">хандсоффсессион</span><span class="sxs-lookup"><span data-stu-id="e68c0-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="e68c0-119">Освобождает объект сеанса MAPI, возвращенный функцией [иолкаккаунселпер:: жетмаписессион](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="e68c0-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e68c0-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e68c0-120">Remarks</span></span>

<span data-ttu-id="e68c0-121">Этот интерфейс передается в [иолкаккаунтманажер:: init](iolkaccountmanager-init.md) при инициализации диспетчера учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e68c0-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e68c0-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e68c0-122">See also</span></span>

- [<span data-ttu-id="e68c0-123">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="e68c0-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="e68c0-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="e68c0-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

