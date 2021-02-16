---
title: ChangeView Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Действие ChangeView можно использовать для перемещения между представлениями на месте.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425360"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="4f835-103">ChangeView Macro Action (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="4f835-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="4f835-104">Действие **ChangeView** можно использовать для перемещения между представлениями на месте.</span><span class="sxs-lookup"><span data-stu-id="4f835-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4f835-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4f835-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="4f835-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="4f835-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="4f835-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="4f835-107">Setting</span></span>

<span data-ttu-id="4f835-108">Действие **ChangeView** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="4f835-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="4f835-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="4f835-109">**Action argument**</span></span>|<span data-ttu-id="4f835-110">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4f835-110">**Required**</span></span>|<span data-ttu-id="4f835-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f835-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f835-112">Table</span><span class="sxs-lookup"><span data-stu-id="4f835-112">Table</span></span>  <br/> |<span data-ttu-id="4f835-113">Да</span><span class="sxs-lookup"><span data-stu-id="4f835-113">Yes</span></span>  <br/> |<span data-ttu-id="4f835-114">Имя открытой таблицы.</span><span class="sxs-lookup"><span data-stu-id="4f835-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="4f835-115">Просмотр</span><span class="sxs-lookup"><span data-stu-id="4f835-115">View</span></span>  <br/> |<span data-ttu-id="4f835-116">Да</span><span class="sxs-lookup"><span data-stu-id="4f835-116">Yes</span></span>  <br/> |<span data-ttu-id="4f835-117">Имя открываемого представления.</span><span class="sxs-lookup"><span data-stu-id="4f835-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="4f835-118">Где</span><span class="sxs-lookup"><span data-stu-id="4f835-118">Where</span></span>  <br/> |<span data-ttu-id="4f835-119">Нет</span><span class="sxs-lookup"><span data-stu-id="4f835-119">No</span></span>  <br/> |<span data-ttu-id="4f835-120">Если этот код задан, заменяет условие Where источника записи объекта.</span><span class="sxs-lookup"><span data-stu-id="4f835-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="4f835-121">Order By</span><span class="sxs-lookup"><span data-stu-id="4f835-121">Order By</span></span>  <br/> |<span data-ttu-id="4f835-122">Нет</span><span class="sxs-lookup"><span data-stu-id="4f835-122">No</span></span>  <br/> |<span data-ttu-id="4f835-123">Строка выражения, включаемая имя поля или полей, по которым необходимо сортировать записи, и необязательные ключевые слова ASC или DESC.</span><span class="sxs-lookup"><span data-stu-id="4f835-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="4f835-124">По умолчанию этот аргумент пустой.</span><span class="sxs-lookup"><span data-stu-id="4f835-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f835-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f835-125">Remarks</span></span>

<span data-ttu-id="4f835-126">Любая сортировка или фильтрация, применяемая пользователем, очищается при вызвании **действия ChangeView.**</span><span class="sxs-lookup"><span data-stu-id="4f835-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="4f835-127">Аргумент  *OrderBy*  — это имя поля или полей, по которым необходимо отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="4f835-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="4f835-128">При использовании более одного имени поля разделять их запятой (,).</span><span class="sxs-lookup"><span data-stu-id="4f835-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="4f835-129">При наборе  *аргумента OrderBy*  записи сортироваться по умолчанию в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="4f835-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

