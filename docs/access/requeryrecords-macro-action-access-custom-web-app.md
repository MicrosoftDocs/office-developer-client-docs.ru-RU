---
title: Действия макроса RequeryRecords (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Действие RequeryRecords можно использовать для обновления, сортировки и фильтрации данных в активном представлении повторным запросом источника представления.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807101"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="ea9f8-103">Действия макроса RequeryRecords (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="ea9f8-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="ea9f8-104">Действие **RequeryRecords** можно использовать для обновления, сортировки и фильтрации данных в активном представлении повторным запросом источника представления.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ea9f8-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="ea9f8-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ea9f8-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="ea9f8-107">Setting</span></span>

<span data-ttu-id="ea9f8-108">Действие **RequeryRecords** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="ea9f8-109">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="ea9f8-109">**Parameter**</span></span>|<span data-ttu-id="ea9f8-110">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="ea9f8-110">**Required**</span></span>|<span data-ttu-id="ea9f8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea9f8-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea9f8-112">**Где =**</span><span class="sxs-lookup"><span data-stu-id="ea9f8-112">**Where=**</span></span> <br/> |<span data-ttu-id="ea9f8-113">Нет</span><span class="sxs-lookup"><span data-stu-id="ea9f8-113">No</span></span>  <br/> |<span data-ttu-id="ea9f8-114">SQL предложение WHERE, которое ограничивает число записей в представлении.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="ea9f8-115">По умолчанию этот аргумент не задан.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="ea9f8-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="ea9f8-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="ea9f8-117">Нет</span><span class="sxs-lookup"><span data-stu-id="ea9f8-117">No</span></span>  <br/> |<span data-ttu-id="ea9f8-118">Строковое выражение, которое включает в себя имя поля или полей, по которому выполняется сортировка записей и необязательные ASC или DESC ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="ea9f8-119">По умолчанию этот аргумент не задан.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea9f8-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="ea9f8-120">Remarks</span></span>

<span data-ttu-id="ea9f8-121">При вызове действие **RequeryRecords** сортировки или фильтрации применяется пользователем снят.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="ea9f8-122">Аргумент *OrderBy* — это имя в поле или поля, в которых используется для сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="ea9f8-123">При использовании более одного имени поля, разделяйте имена запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="ea9f8-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="ea9f8-124">Если значение аргумента *OrderBy* , записи сортируются в порядке возрастания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="ea9f8-125">Чтобы отсортировать записи в убывающем порядке, введите DESC в конце выражения аргумента *OrderBy* .</span><span class="sxs-lookup"><span data-stu-id="ea9f8-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="ea9f8-126">Например для сортировки записей клиентов в порядке убывания имя контакта, задайте *OrderBy* аргумент «ContactName DESC».</span><span class="sxs-lookup"><span data-stu-id="ea9f8-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="ea9f8-127">Чтобы отсортировать имена, LastName по убыванию и FirstName по возрастанию, задайте *OrderBy* «Фамилия Desc, имя ASC».</span><span class="sxs-lookup"><span data-stu-id="ea9f8-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

