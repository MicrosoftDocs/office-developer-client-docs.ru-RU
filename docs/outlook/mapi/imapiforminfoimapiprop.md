---
title: IMAPIFormInfo IMAPIProp
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417366"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="50833-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="50833-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="50833-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50833-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50833-105">Предоставляет клиентские приложения доступ к свойствам, которые являются особыми для определения формы.</span><span class="sxs-lookup"><span data-stu-id="50833-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="50833-106">Сохраняя сведения о форме в отдельном объекте, поставщик библиотеки форм может описать форму клиенту без активации формы.</span><span class="sxs-lookup"><span data-stu-id="50833-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50833-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="50833-107">Header file:</span></span>  <br/> |<span data-ttu-id="50833-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="50833-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="50833-109">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="50833-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="50833-110">Форма информационных объектов</span><span class="sxs-lookup"><span data-stu-id="50833-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="50833-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="50833-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="50833-112">Поставщики библиотек форм</span><span class="sxs-lookup"><span data-stu-id="50833-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="50833-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="50833-113">Called by:</span></span>  <br/> |<span data-ttu-id="50833-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="50833-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="50833-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="50833-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="50833-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="50833-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="50833-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="50833-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="50833-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="50833-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="50833-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="50833-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="50833-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="50833-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="50833-121">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="50833-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="50833-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="50833-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="50833-123">Возвращает указатель к полному набору свойств, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="50833-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="50833-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="50833-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="50833-125">Возвращает указатель к полному набору глаголов, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="50833-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="50833-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="50833-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="50833-127">Создает значок из свойства значка формы.</span><span class="sxs-lookup"><span data-stu-id="50833-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="50833-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="50833-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="50833-129">Сохраняет описание определенной формы в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="50833-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="50833-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="50833-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="50833-131">Возвращает указатель в контейнер формы, в котором установлена определенная форма.</span><span class="sxs-lookup"><span data-stu-id="50833-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50833-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="50833-132">Remarks</span></span>

<span data-ttu-id="50833-133">В отличие от большинства интерфейсов, определенных в заглавном файле MapiForm.h, **IMAPIFormInfo** наследует интерфейс [IMAPIProp,](imapipropiunknown.md) так как он экспортирует большую часть сведений о форме с помощью вызовов метода [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="50833-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50833-134">См. также</span><span class="sxs-lookup"><span data-stu-id="50833-134">See also</span></span>



[<span data-ttu-id="50833-135">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="50833-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

