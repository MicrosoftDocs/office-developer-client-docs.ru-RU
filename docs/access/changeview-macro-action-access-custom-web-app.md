---
title: Макрокоманда ChangeView (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Вы можете использовать действие ChangeView для перехода между представлениями.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425360"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="12a38-103">Макрокоманда ChangeView (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="12a38-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="12a38-104">Вы можете использовать действие **ChangeView** для перехода между представлениями.</span><span class="sxs-lookup"><span data-stu-id="12a38-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="12a38-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="12a38-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="12a38-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="12a38-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="12a38-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="12a38-107">Setting</span></span>

<span data-ttu-id="12a38-108">Макрокоманда **ChangeView** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="12a38-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="12a38-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="12a38-109">**Action argument**</span></span>|<span data-ttu-id="12a38-110">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="12a38-110">**Required**</span></span>|<span data-ttu-id="12a38-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="12a38-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="12a38-112">Table</span><span class="sxs-lookup"><span data-stu-id="12a38-112">Table</span></span>  <br/> |<span data-ttu-id="12a38-113">Да</span><span class="sxs-lookup"><span data-stu-id="12a38-113">Yes</span></span>  <br/> |<span data-ttu-id="12a38-114">Имя открываемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="12a38-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="12a38-115">View</span><span class="sxs-lookup"><span data-stu-id="12a38-115">View</span></span>  <br/> |<span data-ttu-id="12a38-116">Да</span><span class="sxs-lookup"><span data-stu-id="12a38-116">Yes</span></span>  <br/> |<span data-ttu-id="12a38-117">Имя представления, которое требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="12a38-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="12a38-118">Где</span><span class="sxs-lookup"><span data-stu-id="12a38-118">Where</span></span>  <br/> |<span data-ttu-id="12a38-119">Нет</span><span class="sxs-lookup"><span data-stu-id="12a38-119">No</span></span>  <br/> |<span data-ttu-id="12a38-120">Если этот параметр указан, заменяется условие WHERE источника записей объекта.</span><span class="sxs-lookup"><span data-stu-id="12a38-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="12a38-121">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="12a38-121">Order By</span></span>  <br/> |<span data-ttu-id="12a38-122">Нет</span><span class="sxs-lookup"><span data-stu-id="12a38-122">No</span></span>  <br/> |<span data-ttu-id="12a38-123">Строковое выражение, включающее имя поля или полей, по которым сортируются записи, а также необязательные ключевые слова ASC и DESC.</span><span class="sxs-lookup"><span data-stu-id="12a38-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="12a38-124">По умолчанию этот аргумент не задан.</span><span class="sxs-lookup"><span data-stu-id="12a38-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12a38-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="12a38-125">Remarks</span></span>

<span data-ttu-id="12a38-126">При вызове действия **ChangeView** удаляется любая сортировка или фильтрация, примененные пользователем.</span><span class="sxs-lookup"><span data-stu-id="12a38-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="12a38-127">Аргумент *OrderBy* — это имя поля или полей, для которых требуется отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="12a38-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="12a38-128">При использовании нескольких имен полей разделяйте их запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="12a38-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="12a38-129">При задании аргумента *OrderBy* записи сортируются по умолчанию в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="12a38-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

