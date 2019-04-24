---
title: Имапиформфактори IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342121"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="0bb75-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bb75-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="0bb75-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bb75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bb75-105">Поддерживает использование настраиваемых форм времени выполнения в средах распределенных вычислений.</span><span class="sxs-lookup"><span data-stu-id="0bb75-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bb75-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0bb75-106">Header file:</span></span>  <br/> |<span data-ttu-id="0bb75-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="0bb75-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="0bb75-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="0bb75-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0bb75-109">Объекты фабрики форм</span><span class="sxs-lookup"><span data-stu-id="0bb75-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="0bb75-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0bb75-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0bb75-111">Серверы форм</span><span class="sxs-lookup"><span data-stu-id="0bb75-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="0bb75-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0bb75-112">Called by:</span></span>  <br/> |<span data-ttu-id="0bb75-113">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="0bb75-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="0bb75-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="0bb75-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0bb75-115">Иид_имапиформфактори</span><span class="sxs-lookup"><span data-stu-id="0bb75-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="0bb75-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="0bb75-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0bb75-117">ЛПМАПИФОРМФАКТОРИ</span><span class="sxs-lookup"><span data-stu-id="0bb75-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0bb75-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="0bb75-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0bb75-119">Креатеклассфактори</span><span class="sxs-lookup"><span data-stu-id="0bb75-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="0bb75-120">Возвращает объект фабрики класса для формы.</span><span class="sxs-lookup"><span data-stu-id="0bb75-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="0bb75-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="0bb75-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="0bb75-122">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте фабрики форм.</span><span class="sxs-lookup"><span data-stu-id="0bb75-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="0bb75-123">Локксервер</span><span class="sxs-lookup"><span data-stu-id="0bb75-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="0bb75-124">Сохраняет открытый сервер форм в памяти.</span><span class="sxs-lookup"><span data-stu-id="0bb75-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bb75-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bb75-125">Remarks</span></span>

<span data-ttu-id="0bb75-126">Интерфейс **имапиформфактори** основан на интерфейсе [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) , а объекты, реализующие **имапиформфактори** , также должны наследовать от **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="0bb75-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="0bb75-127">**Имапиформфактори** — это интерфейс, с помощью которого пользователи могут создавать новые объекты форм, когда сервер форм поддерживает несколько классов сообщений (то есть несколько типов объектов Form).</span><span class="sxs-lookup"><span data-stu-id="0bb75-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0bb75-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0bb75-128">See also</span></span>



[<span data-ttu-id="0bb75-129">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="0bb75-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

