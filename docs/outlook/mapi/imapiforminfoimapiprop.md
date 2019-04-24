---
title: Имапиформинфо IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321737"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="8d089-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8d089-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="8d089-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d089-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d089-105">Предоставляет клиентским приложениям доступ к свойствам, определенным для определения формы.</span><span class="sxs-lookup"><span data-stu-id="8d089-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="8d089-106">Сохраняя сведения о форме в отдельном объекте, поставщик библиотеки форм может описать форму для клиента, не активируя форму.</span><span class="sxs-lookup"><span data-stu-id="8d089-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d089-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8d089-107">Header file:</span></span>  <br/> |<span data-ttu-id="8d089-108">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="8d089-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8d089-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="8d089-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="8d089-110">Объекты сведений о форме</span><span class="sxs-lookup"><span data-stu-id="8d089-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="8d089-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8d089-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8d089-112">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="8d089-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="8d089-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8d089-113">Called by:</span></span>  <br/> |<span data-ttu-id="8d089-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="8d089-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="8d089-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8d089-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8d089-116">Иид_имапиформинфо</span><span class="sxs-lookup"><span data-stu-id="8d089-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="8d089-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="8d089-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="8d089-118">ЛПМАПИФОРМИНФО</span><span class="sxs-lookup"><span data-stu-id="8d089-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="8d089-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="8d089-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="8d089-120">Не transactd</span><span class="sxs-lookup"><span data-stu-id="8d089-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8d089-121">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="8d089-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8d089-122">Калкформпропсет</span><span class="sxs-lookup"><span data-stu-id="8d089-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="8d089-123">Возвращает указатель на полный набор свойств, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="8d089-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="8d089-124">Калквербсет</span><span class="sxs-lookup"><span data-stu-id="8d089-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="8d089-125">Возвращает указатель на полный набор команд, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="8d089-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="8d089-126">Макеиконфромбинари</span><span class="sxs-lookup"><span data-stu-id="8d089-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="8d089-127">Создает значок на основе свойства Icon формы.</span><span class="sxs-lookup"><span data-stu-id="8d089-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="8d089-128">Савеформ</span><span class="sxs-lookup"><span data-stu-id="8d089-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="8d089-129">Сохраняет описание конкретной формы в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8d089-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="8d089-130">Опенформконтаинер</span><span class="sxs-lookup"><span data-stu-id="8d089-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="8d089-131">Возвращает указатель на контейнер формы, в котором установлена определенная форма.</span><span class="sxs-lookup"><span data-stu-id="8d089-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d089-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="8d089-132">Remarks</span></span>

<span data-ttu-id="8d089-133">В отличие от большинства интерфейсов, определенных в файле заголовка Мапиформ. h, **имапиформинфо** наследуется от интерфейса [IMAPIProp](imapipropiunknown.md) , так как он экспортирует большинство сведений о форме с помощью вызовов метода [IMAPIProp::](imapiprop-getprops.md) -PROPS.</span><span class="sxs-lookup"><span data-stu-id="8d089-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d089-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8d089-134">See also</span></span>



[<span data-ttu-id="8d089-135">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="8d089-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

