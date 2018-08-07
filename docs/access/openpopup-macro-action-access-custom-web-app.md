---
title: Действия макроса OpenPopup (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Открывает указанное представление во всплывающем окне.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807083"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="5502f-103">Действия макроса OpenPopup (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="5502f-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="5502f-104">Открывает указанное представление во всплывающем окне.</span><span class="sxs-lookup"><span data-stu-id="5502f-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5502f-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5502f-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5502f-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5502f-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5502f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5502f-107">Syntax</span></span>

 <span data-ttu-id="5502f-108">**OpenPopup** (*Просмотр* *где =*, *Order By*)</span><span class="sxs-lookup"><span data-stu-id="5502f-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="5502f-109">Действие **OpenPopup** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5502f-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="5502f-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="5502f-110">**Argument name**</span></span>|<span data-ttu-id="5502f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5502f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5502f-112">*Просмотр*</span><span class="sxs-lookup"><span data-stu-id="5502f-112">*View*</span></span>  <br/> |<span data-ttu-id="5502f-113">Имя представления, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="5502f-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="5502f-114">*Где =*</span><span class="sxs-lookup"><span data-stu-id="5502f-114">*Where=*</span></span>  <br/> |<span data-ttu-id="5502f-115">Оператор SQL WHERE (без слова ГДЕ), который ограничивает число записей в представлении.</span><span class="sxs-lookup"><span data-stu-id="5502f-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="5502f-116">*Order By*</span><span class="sxs-lookup"><span data-stu-id="5502f-116">*Order By*</span></span>  <br/> |<span data-ttu-id="5502f-117">Строковое выражение, которое включает в себя имя поля или полей, по которому выполняется сортировка записей и необязательные ASC или DESC ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="5502f-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="5502f-118">По умолчанию этот аргумент не задан.</span><span class="sxs-lookup"><span data-stu-id="5502f-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5502f-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="5502f-119">Remarks</span></span>

<span data-ttu-id="5502f-120">Текущий макрос завершается после обработки **OpenPopup** действие.</span><span class="sxs-lookup"><span data-stu-id="5502f-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="5502f-121">При вызове действие **OpenPopup** сортировки или фильтрации применяется пользователем снят.</span><span class="sxs-lookup"><span data-stu-id="5502f-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="5502f-122">Аргумент *OrderBy* — это имя в поле или поля, в которых используется для сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="5502f-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="5502f-123">При использовании более одного имени поля, разделяйте имена запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="5502f-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="5502f-124">Если значение аргумента *OrderBy* , записи сортируются в порядке возрастания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5502f-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

