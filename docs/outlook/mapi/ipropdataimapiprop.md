---
title: Ипропдата IMAPIProp
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
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435147"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="260aa-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="260aa-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="260aa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="260aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="260aa-105">Предоставляет возможность извлечения и изменения доступа к свойствам объекта.</span><span class="sxs-lookup"><span data-stu-id="260aa-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="260aa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="260aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="260aa-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="260aa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="260aa-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="260aa-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="260aa-109">Объект данных свойства</span><span class="sxs-lookup"><span data-stu-id="260aa-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="260aa-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="260aa-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="260aa-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="260aa-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="260aa-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="260aa-112">Called by:</span></span>  <br/> |<span data-ttu-id="260aa-113">Поставщики услуг и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="260aa-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="260aa-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="260aa-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="260aa-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="260aa-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="260aa-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="260aa-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="260aa-117">лппропдата</span><span class="sxs-lookup"><span data-stu-id="260aa-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="260aa-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="260aa-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="260aa-119">Не transactd</span><span class="sxs-lookup"><span data-stu-id="260aa-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="260aa-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="260aa-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="260aa-121">хрсетобжакцесс</span><span class="sxs-lookup"><span data-stu-id="260aa-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="260aa-122">Задает уровень доступа для объекта.</span><span class="sxs-lookup"><span data-stu-id="260aa-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="260aa-123">хрсетпропакцесс</span><span class="sxs-lookup"><span data-stu-id="260aa-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="260aa-124">Задает уровень доступа и состояние для одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="260aa-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="260aa-125">хржетпропакцесс</span><span class="sxs-lookup"><span data-stu-id="260aa-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="260aa-126">Получает уровень доступа и состояние для одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="260aa-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="260aa-127">храддобжпропс</span><span class="sxs-lookup"><span data-stu-id="260aa-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="260aa-128">Добавляет одно или несколько свойств типа PT_OBJECT в объект.</span><span class="sxs-lookup"><span data-stu-id="260aa-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="260aa-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="260aa-129">Remarks</span></span>

<span data-ttu-id="260aa-130">Интерфейс **ипропдата:: IMAPIProp** реализуется MAPI и используется преимущественно поставщиками услуг, которые обращаются к этой реализации, вызывая функцию [креатеипроп](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="260aa-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="260aa-131">Дополнительные сведения о уровнях доступа к объектам и свойствам содержатся в разделе [разрешения для объектов и свойств](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="260aa-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="260aa-132">См. также</span><span class="sxs-lookup"><span data-stu-id="260aa-132">See also</span></span>



[<span data-ttu-id="260aa-133">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="260aa-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

