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
ms.openlocfilehash: fa439d0a6fa59bac787f09c3f894a750948a0a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808918"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="2cde3-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2cde3-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="2cde3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cde3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cde3-105">Предоставляет клиентских приложений доступ к свойства для определения формы.</span><span class="sxs-lookup"><span data-stu-id="2cde3-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="2cde3-106">Хранение сведений о форме в отдельном объекте, поставщика библиотеки форм можно ввести описание формы в клиент без активации формы.</span><span class="sxs-lookup"><span data-stu-id="2cde3-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2cde3-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2cde3-107">Header file:</span></span>  <br/> |<span data-ttu-id="2cde3-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="2cde3-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="2cde3-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="2cde3-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2cde3-110">Объекты формы</span><span class="sxs-lookup"><span data-stu-id="2cde3-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="2cde3-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="2cde3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2cde3-112">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="2cde3-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="2cde3-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="2cde3-113">Called by:</span></span>  <br/> |<span data-ttu-id="2cde3-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="2cde3-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="2cde3-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="2cde3-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2cde3-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="2cde3-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="2cde3-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="2cde3-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2cde3-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="2cde3-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="2cde3-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="2cde3-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="2cde3-120">Не входящих в транзакции</span><span class="sxs-lookup"><span data-stu-id="2cde3-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2cde3-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="2cde3-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2cde3-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="2cde3-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="2cde3-123">Возвращает указатель на полный набор свойств, используемых в форме.</span><span class="sxs-lookup"><span data-stu-id="2cde3-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="2cde3-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="2cde3-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="2cde3-125">Возвращает указатель на полный набор команд, которые использует формы.</span><span class="sxs-lookup"><span data-stu-id="2cde3-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="2cde3-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="2cde3-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="2cde3-127">Создает значок из свойства значок формы.</span><span class="sxs-lookup"><span data-stu-id="2cde3-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="2cde3-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="2cde3-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="2cde3-129">Сохраняет описание определенной формы в файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2cde3-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="2cde3-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="2cde3-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="2cde3-131">Возвращает указатель на контейнер формы, в которой установлен определенной формы.</span><span class="sxs-lookup"><span data-stu-id="2cde3-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cde3-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="2cde3-132">Remarks</span></span>

<span data-ttu-id="2cde3-133">В отличие от большинства интерфейсы, определенные в файле заголовка MapiForm.h **IMAPIFormInfo** наследует от интерфейса [IMAPIProp](imapipropiunknown.md) , так как экспортирует большинство сведений о форме посредством вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="2cde3-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2cde3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2cde3-134">See also</span></span>



[<span data-ttu-id="2cde3-135">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="2cde3-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

