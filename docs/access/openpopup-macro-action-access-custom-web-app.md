---
title: Макро-действие OpenPopup (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Открывает указанное представление в всплывающее окно.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427390"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="a0e52-103">Макро-действие OpenPopup (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="a0e52-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="a0e52-104">Открывает указанное представление в всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="a0e52-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a0e52-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a0e52-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a0e52-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="a0e52-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0e52-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0e52-107">Syntax</span></span>

 <span data-ttu-id="a0e52-108">**OpenPopup** *(View*, *Where=*, *Order By)*</span><span class="sxs-lookup"><span data-stu-id="a0e52-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="a0e52-109">Действие **OpenPopup** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a0e52-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="a0e52-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="a0e52-110">**Argument name**</span></span>|<span data-ttu-id="a0e52-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0e52-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a0e52-112">*View*</span><span class="sxs-lookup"><span data-stu-id="a0e52-112">*View*</span></span>  <br/> |<span data-ttu-id="a0e52-113">Имя открываемого представления.</span><span class="sxs-lookup"><span data-stu-id="a0e52-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="a0e52-114">*Where=*</span><span class="sxs-lookup"><span data-stu-id="a0e52-114">*Where=*</span></span>  <br/> |<span data-ttu-id="a0e52-115">Допустимый SQL where (без слова WHERE), ограничивающий записи в представлении.</span><span class="sxs-lookup"><span data-stu-id="a0e52-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="a0e52-116">*Order By*</span><span class="sxs-lookup"><span data-stu-id="a0e52-116">*Order By*</span></span>  <br/> |<span data-ttu-id="a0e52-117">Строковая фраза, включаемая имя поля или полей для сортировки записей, а также необязательные ключевые слова ASC или DESC.</span><span class="sxs-lookup"><span data-stu-id="a0e52-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="a0e52-118">По умолчанию этот аргумент является пустым.</span><span class="sxs-lookup"><span data-stu-id="a0e52-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0e52-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0e52-119">Remarks</span></span>

<span data-ttu-id="a0e52-120">Текущий макрос завершается после обработки действия **OpenPopup.**</span><span class="sxs-lookup"><span data-stu-id="a0e52-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="a0e52-121">Любая сортировка или фильтрация, применяемая пользователем, очищается при наступлении **действия OpenPopup.**</span><span class="sxs-lookup"><span data-stu-id="a0e52-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="a0e52-122">Аргумент  *OrderBy*  — это имя поля или полей, на которых необходимо сортировать записи.</span><span class="sxs-lookup"><span data-stu-id="a0e52-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="a0e52-123">При использовании более чем одного имени поля разделять имена с запятой (,).</span><span class="sxs-lookup"><span data-stu-id="a0e52-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="a0e52-124">При наборе  *аргумента OrderBy*  записи сортироваться по умолчанию в порядке восходящей.</span><span class="sxs-lookup"><span data-stu-id="a0e52-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

