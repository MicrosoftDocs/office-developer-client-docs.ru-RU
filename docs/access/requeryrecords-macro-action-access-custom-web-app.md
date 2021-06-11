---
title: RequeryRecords Macro Action (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Вы можете использовать действие RequeryRecords для обновления, сортировки и фильтрации данных в активном представлении путем повторного представления источника представления.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439249"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="4b0ed-103">RequeryRecords Macro Action (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="4b0ed-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="4b0ed-104">Вы можете использовать действие **RequeryRecords** для обновления, сортировки и фильтрации данных в активном представлении путем повторного представления источника представления.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4b0ed-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="4b0ed-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="4b0ed-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="4b0ed-107">Setting</span></span>

<span data-ttu-id="4b0ed-108">Действие **RequeryRecords имеет** следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="4b0ed-109">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="4b0ed-109">**Parameter**</span></span>|<span data-ttu-id="4b0ed-110">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4b0ed-110">**Required**</span></span>|<span data-ttu-id="4b0ed-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b0ed-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b0ed-112">**Where=**</span><span class="sxs-lookup"><span data-stu-id="4b0ed-112">**Where=**</span></span> <br/> |<span data-ttu-id="4b0ed-113">Нет</span><span class="sxs-lookup"><span data-stu-id="4b0ed-113">No</span></span>  <br/> |<span data-ttu-id="4b0ed-114">Пункт SQL WHERE, ограничивающий записи в представлении.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="4b0ed-115">По умолчанию этот аргумент является пустым.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="4b0ed-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="4b0ed-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="4b0ed-117">Нет</span><span class="sxs-lookup"><span data-stu-id="4b0ed-117">No</span></span>  <br/> |<span data-ttu-id="4b0ed-118">Строковая фраза, включаемая имя поля или полей для сортировки записей, а также необязательные ключевые слова ASC или DESC.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="4b0ed-119">По умолчанию этот аргумент является пустым.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b0ed-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="4b0ed-120">Remarks</span></span>

<span data-ttu-id="4b0ed-121">Любая сортировка или фильтрация, применяемая пользователем, очищается при наложении действия **RequeryRecords.**</span><span class="sxs-lookup"><span data-stu-id="4b0ed-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="4b0ed-122">Аргумент  *OrderBy*  — это имя поля или полей, на которых необходимо сортировать записи.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="4b0ed-123">При использовании более чем одного имени поля разделять имена с запятой (,).</span><span class="sxs-lookup"><span data-stu-id="4b0ed-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="4b0ed-124">При наборе  *аргумента OrderBy*  записи сортироваться по умолчанию в порядке восходящей.</span><span class="sxs-lookup"><span data-stu-id="4b0ed-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="4b0ed-125">Чтобы сортировать записи в порядке убывления, введите DESC в конце выражения *аргумента OrderBy.*</span><span class="sxs-lookup"><span data-stu-id="4b0ed-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="4b0ed-126">Например, чтобы сортировать записи клиентов в порядке убывания по имени контакта, установите аргумент  *OrderBy*  на "ContactName DESC".</span><span class="sxs-lookup"><span data-stu-id="4b0ed-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="4b0ed-127">Чтобы сортировать имена по убыванию LastName и по возрастанию FirstName, установите аргумент  *OrderBy*  на "LastName DESC, FirstName ASC".</span><span class="sxs-lookup"><span data-stu-id="4b0ed-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

