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
# <a name="iolkaccounthelper"></a><span data-ttu-id="7bf9a-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="7bf9a-102">IOlkAccountHelper</span></span>

<span data-ttu-id="7bf9a-103">Предоставляет дополнительные функции в текущем сеансе MAPI для управления учетной записью.</span><span class="sxs-lookup"><span data-stu-id="7bf9a-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7bf9a-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7bf9a-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bf9a-105">Наследуется от:</span><span class="sxs-lookup"><span data-stu-id="7bf9a-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="7bf9a-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="7bf9a-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="7bf9a-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="7bf9a-107">Provided by:</span></span>  <br/> |<span data-ttu-id="7bf9a-108">Клиент</span><span class="sxs-lookup"><span data-stu-id="7bf9a-108">Client</span></span>  <br/> |
|<span data-ttu-id="7bf9a-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="7bf9a-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7bf9a-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="7bf9a-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7bf9a-111">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="7bf9a-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7bf9a-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="7bf9a-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="7bf9a-113">*Этот член является местоимящиком и не поддерживается.*</span><span class="sxs-lookup"><span data-stu-id="7bf9a-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="7bf9a-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="7bf9a-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="7bf9a-115">Получает имя профиля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7bf9a-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="7bf9a-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="7bf9a-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="7bf9a-117">Открывает сеанс MAPI и сохраняет ссылку на сеанс для диспетчера учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7bf9a-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="7bf9a-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="7bf9a-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="7bf9a-119">Освобождает объект сеанса MAPI, возвращенный [IOlkAccountHelper::GetMapiSession.](iolkaccounthelper-getmapisession.md)</span><span class="sxs-lookup"><span data-stu-id="7bf9a-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bf9a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7bf9a-120">Remarks</span></span>

<span data-ttu-id="7bf9a-121">Этот интерфейс передается в [IOlkAccountManager::Init](iolkaccountmanager-init.md) при инициализации диспетчера учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7bf9a-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7bf9a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7bf9a-122">See also</span></span>

- [<span data-ttu-id="7bf9a-123">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="7bf9a-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="7bf9a-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="7bf9a-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

