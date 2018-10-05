---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384768"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="853dc-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="853dc-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="853dc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="853dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="853dc-105">Поддерживает использование настраиваемых форм во время выполнения в распределенных средах сетей.</span><span class="sxs-lookup"><span data-stu-id="853dc-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="853dc-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="853dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="853dc-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="853dc-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="853dc-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="853dc-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="853dc-109">Объекты фабрики формы</span><span class="sxs-lookup"><span data-stu-id="853dc-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="853dc-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="853dc-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="853dc-111">Серверы формы</span><span class="sxs-lookup"><span data-stu-id="853dc-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="853dc-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="853dc-112">Called by:</span></span>  <br/> |<span data-ttu-id="853dc-113">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="853dc-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="853dc-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="853dc-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="853dc-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="853dc-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="853dc-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="853dc-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="853dc-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="853dc-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="853dc-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="853dc-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="853dc-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="853dc-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="853dc-120">Возвращает объект фабрики класса для формы.</span><span class="sxs-lookup"><span data-stu-id="853dc-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="853dc-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="853dc-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="853dc-122">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущей появление объекта фабрики формы.</span><span class="sxs-lookup"><span data-stu-id="853dc-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="853dc-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="853dc-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="853dc-124">Сохраняет это сервер открытой формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="853dc-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="853dc-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="853dc-125">Remarks</span></span>

<span data-ttu-id="853dc-126">Интерфейс **IMAPIFormFactory** основано на интерфейс [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) и объекты, которые реализуют **IMAPIFormFactory** также должен наследовать от **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="853dc-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="853dc-127">**IMAPIFormFactory** — это интерфейс, который средства просмотра формы используется для создания новых объектов формы, если сервер формы поддерживает несколько классов сообщений (то есть несколько учетных записей введите объекта формы).</span><span class="sxs-lookup"><span data-stu-id="853dc-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="853dc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="853dc-128">See also</span></span>



[<span data-ttu-id="853dc-129">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="853dc-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

