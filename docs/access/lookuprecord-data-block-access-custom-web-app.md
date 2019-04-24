---
title: Блок данных LookupRecord (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Блок данных LookupRecord выполняет набор действий с определенной записью.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304272"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="b3251-103">Блок данных LookupRecord (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="b3251-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="b3251-104">Блок данных **LookupRecord** выполняет набор действий с определенной записью.</span><span class="sxs-lookup"><span data-stu-id="b3251-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b3251-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b3251-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="b3251-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="b3251-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b3251-107">Блок данных **LookupRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="b3251-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="b3251-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b3251-108">Setting</span></span>

<span data-ttu-id="b3251-109">Макрокоманда **SetField** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b3251-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="b3251-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="b3251-110">**Argument**</span></span>|<span data-ttu-id="b3251-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b3251-111">**Required**</span></span>|<span data-ttu-id="b3251-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3251-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b3251-113">_Возврата_</span><span class="sxs-lookup"><span data-stu-id="b3251-113">_In_</span></span> <br/> |<span data-ttu-id="b3251-114">Да</span><span class="sxs-lookup"><span data-stu-id="b3251-114">Yes</span></span>  <br/> |<span data-ttu-id="b3251-115">Строка, определяющая запись, с которой выполняется работа.</span><span class="sxs-lookup"><span data-stu-id="b3251-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="b3251-116">Аргумент *in* может содержать имя таблицы, запрос на выборку или инструкцию SQL.</span><span class="sxs-lookup"><span data-stu-id="b3251-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="b3251-117">_Условие отбора_</span><span class="sxs-lookup"><span data-stu-id="b3251-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="b3251-118">Нет</span><span class="sxs-lookup"><span data-stu-id="b3251-118">No</span></span>  <br/> |<span data-ttu-id="b3251-119">Строковое выражение, используемое для ограничения диапазона данных, в котором выполняется блок данных **LookupRecord** .</span><span class="sxs-lookup"><span data-stu-id="b3251-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="b3251-120">Например, критерии часто эквивалентны предложению WHERE в выражении SQL без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="b3251-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="b3251-121">Если аргумент условия_отбора опущен, блок данных **LookupRecord** работает на всем домене, указанном аргументом *in* .</span><span class="sxs-lookup"><span data-stu-id="b3251-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="b3251-122">Все поля, включенные в критерии, также должны быть полями в \*\* .</span><span class="sxs-lookup"><span data-stu-id="b3251-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="b3251-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="b3251-123">_Alias_</span></span> <br/> |<span data-ttu-id="b3251-124">Нет</span><span class="sxs-lookup"><span data-stu-id="b3251-124">No</span></span>  <br/> |<span data-ttu-id="b3251-125">Строка, предоставляющая альтернативное имя для записи, заданной аргументом *in* .</span><span class="sxs-lookup"><span data-stu-id="b3251-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="b3251-126">Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки.</span><span class="sxs-lookup"><span data-stu-id="b3251-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="b3251-127">Если параметр *Alias* не указан, имя таблицы или запроса будет использоваться в качестве псевдонима.</span><span class="sxs-lookup"><span data-stu-id="b3251-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3251-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3251-128">Remarks</span></span>

<span data-ttu-id="b3251-129">Если условие, заданное в аргументах *условия* *in* и WHERE, указывает более одной записи, блок данных **LookupRecord** будет работать только с первой записью.</span><span class="sxs-lookup"><span data-stu-id="b3251-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="b3251-130">Если ни одна *из* записей не удовлетворяет *условию WHERE* или не содержит записей, то **LookupRecord** создает пустую запись, в которой все поля содержат значение **null** .</span><span class="sxs-lookup"><span data-stu-id="b3251-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

