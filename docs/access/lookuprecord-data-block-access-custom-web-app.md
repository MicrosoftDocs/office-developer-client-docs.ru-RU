---
title: Блок данных LookupRecord (Пользовательский доступ к веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Блок данных LookupRecord выполняет набор действий на определенной записи.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434363"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="a37c5-103">Блок данных LookupRecord (Пользовательский доступ к веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="a37c5-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="a37c5-104">Блок **данных LookupRecord** выполняет набор действий на определенной записи.</span><span class="sxs-lookup"><span data-stu-id="a37c5-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a37c5-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a37c5-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a37c5-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="a37c5-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a37c5-107">Блок **данных LookupRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="a37c5-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="a37c5-108">Setting</span><span class="sxs-lookup"><span data-stu-id="a37c5-108">Setting</span></span>

<span data-ttu-id="a37c5-109">Действие **SetField** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a37c5-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="a37c5-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="a37c5-110">**Argument**</span></span>|<span data-ttu-id="a37c5-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a37c5-111">**Required**</span></span>|<span data-ttu-id="a37c5-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a37c5-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a37c5-113">_В_</span><span class="sxs-lookup"><span data-stu-id="a37c5-113">_In_</span></span> <br/> |<span data-ttu-id="a37c5-114">Да</span><span class="sxs-lookup"><span data-stu-id="a37c5-114">Yes</span></span>  <br/> |<span data-ttu-id="a37c5-115">Строка, определяемая для работы записи.</span><span class="sxs-lookup"><span data-stu-id="a37c5-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="a37c5-116">Аргумент *In* может содержать имя таблицы, выбранный запрос или SQL.</span><span class="sxs-lookup"><span data-stu-id="a37c5-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="a37c5-117">_Где состояние_</span><span class="sxs-lookup"><span data-stu-id="a37c5-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="a37c5-118">Нет</span><span class="sxs-lookup"><span data-stu-id="a37c5-118">No</span></span>  <br/> |<span data-ttu-id="a37c5-119">Строковая экспрессия, используемая для ограничения диапазона данных, на которых выполняется блок данных **LookupRecord.**</span><span class="sxs-lookup"><span data-stu-id="a37c5-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="a37c5-120">Например, критерии часто эквивалентны пункту WHERE в SQL, без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="a37c5-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="a37c5-121">Если не указаны критерии, блок **данных LookupRecord** работает на всем домене, указанном аргументом *In.*</span><span class="sxs-lookup"><span data-stu-id="a37c5-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="a37c5-122">Любое поле, включенное в критерии, также должно быть полем  *в In*  .</span><span class="sxs-lookup"><span data-stu-id="a37c5-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="a37c5-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="a37c5-123">_Alias_</span></span> <br/> |<span data-ttu-id="a37c5-124">Нет</span><span class="sxs-lookup"><span data-stu-id="a37c5-124">No</span></span>  <br/> |<span data-ttu-id="a37c5-125">Строка, которая предоставляет альтернативное имя для записи, указанной аргументом *In.*</span><span class="sxs-lookup"><span data-stu-id="a37c5-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="a37c5-126">Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки.</span><span class="sxs-lookup"><span data-stu-id="a37c5-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="a37c5-127">Если  *псевдоним не*  указан, в качестве псевдонима будет использоваться таблица или имя запроса.</span><span class="sxs-lookup"><span data-stu-id="a37c5-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a37c5-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="a37c5-128">Remarks</span></span>

<span data-ttu-id="a37c5-129">Если критерии, указанные аргументами In  *и*  *Where Condition,*  задают несколько записей, блок данных **LookupRecord** будет работать только на первой записи.</span><span class="sxs-lookup"><span data-stu-id="a37c5-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="a37c5-130">Если запись не удовлетворяет положение *"Где* состояние" или "In" не содержит записей, **то LookupRecord** создает пустую запись, в которой все поля содержат значение **Null.** </span><span class="sxs-lookup"><span data-stu-id="a37c5-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

