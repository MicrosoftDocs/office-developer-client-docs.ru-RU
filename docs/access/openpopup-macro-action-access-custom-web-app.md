---
title: Макрокоманда Опенпопуп (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Открывает указанное представление во всплывающем окне.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427390"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="755b9-103">Макрокоманда Опенпопуп (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="755b9-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="755b9-104">Открывает указанное представление во всплывающем окне.</span><span class="sxs-lookup"><span data-stu-id="755b9-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="755b9-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="755b9-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="755b9-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="755b9-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="755b9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="755b9-107">Syntax</span></span>

 <span data-ttu-id="755b9-108">**Опенпопуп** (*Представление*, *где =*, *ORDER BY*)</span><span class="sxs-lookup"><span data-stu-id="755b9-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="755b9-109">Действие **опенпопуп** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="755b9-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="755b9-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="755b9-110">**Argument name**</span></span>|<span data-ttu-id="755b9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="755b9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="755b9-112">*View*</span><span class="sxs-lookup"><span data-stu-id="755b9-112">*View*</span></span>  <br/> |<span data-ttu-id="755b9-113">Имя представления, которое требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="755b9-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="755b9-114">*Где =*</span><span class="sxs-lookup"><span data-stu-id="755b9-114">*Where=*</span></span>  <br/> |<span data-ttu-id="755b9-115">Допустимое предложение WHERE SQL (без слова WHERE), которое позволяет ограничить записи в представлении.</span><span class="sxs-lookup"><span data-stu-id="755b9-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="755b9-116">*ORDER BY*</span><span class="sxs-lookup"><span data-stu-id="755b9-116">*Order By*</span></span>  <br/> |<span data-ttu-id="755b9-117">Строковое выражение, включающее имя поля или полей, по которым сортируются записи, а также необязательные ключевые слова ASC и DESC.</span><span class="sxs-lookup"><span data-stu-id="755b9-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="755b9-118">По умолчанию этот аргумент не задан.</span><span class="sxs-lookup"><span data-stu-id="755b9-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="755b9-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="755b9-119">Remarks</span></span>

<span data-ttu-id="755b9-120">После обработки действия **опенпопуп** текущий макрос завершается.</span><span class="sxs-lookup"><span data-stu-id="755b9-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="755b9-121">При вызове действия **опенпопуп** удаляется любая сортировка или фильтрация, примененные пользователем.</span><span class="sxs-lookup"><span data-stu-id="755b9-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="755b9-122">Аргумент *OrderBy* — это имя поля или полей, для которых требуется отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="755b9-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="755b9-123">При использовании нескольких имен полей разделяйте их запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="755b9-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="755b9-124">При задании аргумента *OrderBy* записи сортируются по умолчанию в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="755b9-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

