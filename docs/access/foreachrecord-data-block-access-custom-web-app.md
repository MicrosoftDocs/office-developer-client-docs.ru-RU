---
title: Блок данных ДляКаждойЗаписи (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Блок данных ДляКаждойЗаписи повторяет набор операторов для каждой записи в домене.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428237"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="ae29b-103">Блок данных ДляКаждойЗаписи (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="ae29b-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="ae29b-104">Блок данных **ДляКаждойЗаписи** повторяет набор операторов для каждой записи в домене.</span><span class="sxs-lookup"><span data-stu-id="ae29b-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ae29b-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ae29b-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="ae29b-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="ae29b-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ae29b-107">Блок данных **ДляКаждойЗаписи** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="ae29b-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ae29b-108">Setting</span><span class="sxs-lookup"><span data-stu-id="ae29b-108">Setting</span></span>

<span data-ttu-id="ae29b-109">Макрокоманда **ДляКаждойЗаписи** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="ae29b-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="ae29b-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="ae29b-110">**Argument name**</span></span>|<span data-ttu-id="ae29b-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ae29b-111">**Required**</span></span>|<span data-ttu-id="ae29b-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ae29b-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae29b-113">**Возврата**</span><span class="sxs-lookup"><span data-stu-id="ae29b-113">**In**</span></span> <br/> |<span data-ttu-id="ae29b-114">Да</span><span class="sxs-lookup"><span data-stu-id="ae29b-114">Yes</span></span>  <br/> |<span data-ttu-id="ae29b-115">Строка, определяющая домен записей, с которыми выполняется работа.</span><span class="sxs-lookup"><span data-stu-id="ae29b-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="ae29b-116">Аргумент *in* может содержать имя таблицы, запрос на выборку или инструкцию SQL.</span><span class="sxs-lookup"><span data-stu-id="ae29b-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="ae29b-117">**Note**: указанный домен не может содержать данные, хранящиеся в связанной таблице или источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="ae29b-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="ae29b-118">**Условие отбора**</span><span class="sxs-lookup"><span data-stu-id="ae29b-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="ae29b-119">Нет</span><span class="sxs-lookup"><span data-stu-id="ae29b-119">No</span></span>  <br/> |<span data-ttu-id="ae29b-120">Строковое выражение, используемое для ограничения диапазона данных, в котором выполняется блок данных блока **ДляКаждойЗаписи** .</span><span class="sxs-lookup"><span data-stu-id="ae29b-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="ae29b-121">Например, критерии часто эквивалентны предложению WHERE в выражении SQL без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="ae29b-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="ae29b-122">Если критерии опущены, блок данных **ДляКаждойЗаписи** работает на всем домене, указанном аргументом *in* .</span><span class="sxs-lookup"><span data-stu-id="ae29b-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="ae29b-123">Все поля, включенные в критерии, также должны быть полями в \*\* .</span><span class="sxs-lookup"><span data-stu-id="ae29b-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="ae29b-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="ae29b-124">**Alias**</span></span> <br/> |<span data-ttu-id="ae29b-125">Нет</span><span class="sxs-lookup"><span data-stu-id="ae29b-125">No</span></span>  <br/> |<span data-ttu-id="ae29b-126">Строка, предоставляющая альтернативное имя для домена, указанного аргументом *in* .</span><span class="sxs-lookup"><span data-stu-id="ae29b-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="ae29b-127">Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки.</span><span class="sxs-lookup"><span data-stu-id="ae29b-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="ae29b-128">Если параметр *Alias* не указан, имя таблицы или запроса будет использоваться в качестве псевдонима.</span><span class="sxs-lookup"><span data-stu-id="ae29b-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae29b-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae29b-129">Remarks</span></span>

<span data-ttu-id="ae29b-130">Используйте действие **[екситфореачрекорд](exitforeachrecord-macro-action-access-custom-web-app.md)** для немедленного выхода из блока данных **ДляКаждойЗаписи** .</span><span class="sxs-lookup"><span data-stu-id="ae29b-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

