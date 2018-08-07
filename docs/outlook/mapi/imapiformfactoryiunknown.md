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
ms.openlocfilehash: 651ef6a7c1af70c75a85e13414c4fd7632d30290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808923"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="bdec6-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdec6-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="bdec6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bdec6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bdec6-105">Поддерживает использование настраиваемых форм во время выполнения в распределенных средах сетей.</span><span class="sxs-lookup"><span data-stu-id="bdec6-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bdec6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bdec6-106">Header file:</span></span>  <br/> |<span data-ttu-id="bdec6-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="bdec6-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bdec6-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="bdec6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bdec6-109">Объекты фабрики формы</span><span class="sxs-lookup"><span data-stu-id="bdec6-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="bdec6-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="bdec6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bdec6-111">Серверы формы</span><span class="sxs-lookup"><span data-stu-id="bdec6-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="bdec6-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="bdec6-112">Called by:</span></span>  <br/> |<span data-ttu-id="bdec6-113">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="bdec6-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="bdec6-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="bdec6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bdec6-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="bdec6-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="bdec6-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="bdec6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bdec6-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="bdec6-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bdec6-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="bdec6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bdec6-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="bdec6-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="bdec6-120">Возвращает объект фабрики класса для формы.</span><span class="sxs-lookup"><span data-stu-id="bdec6-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="bdec6-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="bdec6-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="bdec6-122">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущей появление объекта фабрики формы.</span><span class="sxs-lookup"><span data-stu-id="bdec6-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="bdec6-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="bdec6-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="bdec6-124">Сохраняет это сервер открытой формы в памяти.</span><span class="sxs-lookup"><span data-stu-id="bdec6-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdec6-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="bdec6-125">Remarks</span></span>

<span data-ttu-id="bdec6-126">Интерфейс **IMAPIFormFactory** основано на интерфейс [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) и объекты, которые реализуют **IMAPIFormFactory** также должен наследовать от **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="bdec6-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="bdec6-127">**IMAPIFormFactory** — это интерфейс, который средства просмотра формы используется для создания новых объектов формы, если сервер формы поддерживает несколько классов сообщений (то есть несколько учетных записей введите объекта формы).</span><span class="sxs-lookup"><span data-stu-id="bdec6-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bdec6-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bdec6-128">See also</span></span>



[<span data-ttu-id="bdec6-129">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="bdec6-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

