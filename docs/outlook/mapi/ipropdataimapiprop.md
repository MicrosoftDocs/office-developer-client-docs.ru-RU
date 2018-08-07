---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809524"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="da8c0-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="da8c0-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="da8c0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da8c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da8c0-105">Предоставляет возможность извлекать и изменять уровень доступа для свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="da8c0-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da8c0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="da8c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="da8c0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="da8c0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="da8c0-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="da8c0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="da8c0-109">Объект данных свойств</span><span class="sxs-lookup"><span data-stu-id="da8c0-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="da8c0-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="da8c0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="da8c0-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="da8c0-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="da8c0-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="da8c0-112">Called by:</span></span>  <br/> |<span data-ttu-id="da8c0-113">Поставщиков услуг и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="da8c0-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="da8c0-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="da8c0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="da8c0-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="da8c0-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="da8c0-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="da8c0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="da8c0-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="da8c0-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="da8c0-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="da8c0-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="da8c0-119">Не входящих в транзакции</span><span class="sxs-lookup"><span data-stu-id="da8c0-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="da8c0-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="da8c0-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="da8c0-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="da8c0-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="da8c0-122">Задает уровень доступа для объекта.</span><span class="sxs-lookup"><span data-stu-id="da8c0-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="da8c0-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="da8c0-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="da8c0-124">Задает уровень доступа и состояние для одной или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="da8c0-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="da8c0-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="da8c0-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="da8c0-126">Получает уровень доступа и состояние для одной или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="da8c0-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="da8c0-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="da8c0-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="da8c0-128">Добавление одного или нескольких свойств типа PT_OBJECT объект.</span><span class="sxs-lookup"><span data-stu-id="da8c0-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da8c0-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="da8c0-129">Remarks</span></span>

<span data-ttu-id="da8c0-130">Интерфейс **IPropData::IMAPIProp** реализован MAPI и используется в первую очередь поставщиками услуг, обращающихся к этой реализации путем вызова функции [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="da8c0-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="da8c0-131">Дополнительные сведения о уровни доступа для объектов и свойств содержатся в разделе [разрешения для объектов и свойств](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="da8c0-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da8c0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="da8c0-132">See also</span></span>



[<span data-ttu-id="da8c0-133">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="da8c0-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

