---
title: OpenPopup Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Открывает указанное представление во всплывающее окно.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427390"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="62775-103">OpenPopup Macro Action (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="62775-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="62775-104">Открывает указанное представление во всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="62775-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="62775-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="62775-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="62775-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="62775-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="62775-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62775-107">Syntax</span></span>

 <span data-ttu-id="62775-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span><span class="sxs-lookup"><span data-stu-id="62775-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="62775-109">Действие **OpenPopup** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="62775-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="62775-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="62775-110">**Argument name**</span></span>|<span data-ttu-id="62775-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62775-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="62775-112">*View*</span><span class="sxs-lookup"><span data-stu-id="62775-112">*View*</span></span>  <br/> |<span data-ttu-id="62775-113">Имя открываемого представления.</span><span class="sxs-lookup"><span data-stu-id="62775-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="62775-114">*Where=*</span><span class="sxs-lookup"><span data-stu-id="62775-114">*Where=*</span></span>  <br/> |<span data-ttu-id="62775-115">Допустимый SQL WHERE (без слова WHERE), ограничивающий записи в представлении.</span><span class="sxs-lookup"><span data-stu-id="62775-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="62775-116">*Order By*</span><span class="sxs-lookup"><span data-stu-id="62775-116">*Order By*</span></span>  <br/> |<span data-ttu-id="62775-117">Строка выражения, которая включает имя поля или полей, по которым необходимо сортировать записи, и необязательные ключевые слова ASC или DESC.</span><span class="sxs-lookup"><span data-stu-id="62775-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="62775-118">По умолчанию этот аргумент пустой.</span><span class="sxs-lookup"><span data-stu-id="62775-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62775-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="62775-119">Remarks</span></span>

<span data-ttu-id="62775-120">Текущий макрос завершается после обработки действия **OpenPopup.**</span><span class="sxs-lookup"><span data-stu-id="62775-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="62775-121">При наступлении действия **OpenPopup** любая сортировка или фильтрация, применяемая пользователем, очищается.</span><span class="sxs-lookup"><span data-stu-id="62775-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="62775-122">Аргумент  *OrderBy*  — это имя поля или полей, по которым необходимо отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="62775-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="62775-123">При использовании более одного имени поля разделять их запятой (,).</span><span class="sxs-lookup"><span data-stu-id="62775-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="62775-124">При наборе  *аргумента OrderBy*  записи сортироваться по умолчанию в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="62775-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

