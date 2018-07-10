---
title: Действия макроса ChangeView (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Действие ChangeView можно использовать для перехода между режимами на месте.
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806962"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="d2340-103">Действия макроса ChangeView (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="d2340-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d2340-104">Действие **ChangeView** можно использовать для перехода между режимами на месте.</span><span class="sxs-lookup"><span data-stu-id="d2340-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d2340-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d2340-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="d2340-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="d2340-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d2340-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="d2340-107">Setting</span></span>

<span data-ttu-id="d2340-108">Действие **ChangeView** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="d2340-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="d2340-109">**Аргумент действия**</span><span class="sxs-lookup"><span data-stu-id="d2340-109">**Action argument**</span></span>|<span data-ttu-id="d2340-110">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="d2340-110">**Required**</span></span>|<span data-ttu-id="d2340-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d2340-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2340-112">Таблица</span><span class="sxs-lookup"><span data-stu-id="d2340-112">Table</span></span>  <br/> |<span data-ttu-id="d2340-113">Да</span><span class="sxs-lookup"><span data-stu-id="d2340-113">Yes</span></span>  <br/> |<span data-ttu-id="d2340-114">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="d2340-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="d2340-115">Представление</span><span class="sxs-lookup"><span data-stu-id="d2340-115">View</span></span>  <br/> |<span data-ttu-id="d2340-116">Да</span><span class="sxs-lookup"><span data-stu-id="d2340-116">Yes</span></span>  <br/> |<span data-ttu-id="d2340-117">Имя представления, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="d2340-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="d2340-118">Где</span><span class="sxs-lookup"><span data-stu-id="d2340-118">Where</span></span>  <br/> |<span data-ttu-id="d2340-119">Нет</span><span class="sxs-lookup"><span data-stu-id="d2340-119">No</span></span>  <br/> |<span data-ttu-id="d2340-120">Если указано, заменяет условие источника записей объекта.</span><span class="sxs-lookup"><span data-stu-id="d2340-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="d2340-121">Order By</span><span class="sxs-lookup"><span data-stu-id="d2340-121">Order By</span></span>  <br/> |<span data-ttu-id="d2340-122">Нет</span><span class="sxs-lookup"><span data-stu-id="d2340-122">No</span></span>  <br/> |<span data-ttu-id="d2340-123">Строковое выражение, которое включает в себя имя поля или полей, по которому выполняется сортировка записей и необязательные ASC или DESC ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="d2340-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="d2340-124">По умолчанию этот аргумент не задан.</span><span class="sxs-lookup"><span data-stu-id="d2340-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2340-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="d2340-125">Remarks</span></span>

<span data-ttu-id="d2340-126">При вызове действие **ChangeView** сортировки или фильтрации применяется пользователем снят.</span><span class="sxs-lookup"><span data-stu-id="d2340-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="d2340-127">Аргумент *OrderBy* — это имя в поле или поля, в которых используется для сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="d2340-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="d2340-128">При использовании более одного имени поля, разделяйте имена запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="d2340-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="d2340-129">Если значение аргумента *OrderBy* , записи сортируются в порядке возрастания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2340-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

