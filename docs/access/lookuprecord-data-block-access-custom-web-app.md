---
title: Блок данных макрокомандой НайтиЗапись, после (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Блок данных макрокомандой НайтиЗапись, после выполняет набор действий в конкретной записи.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806991"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="c8d5f-103">Блок данных макрокомандой НайтиЗапись, после (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="c8d5f-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="c8d5f-104">Блок данных **макрокомандой НайтиЗапись, после** выполняет набор действий в конкретной записи.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c8d5f-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="c8d5f-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c8d5f-107">Блок данных **макрокомандой НайтиЗапись, после** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="c8d5f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="c8d5f-108">Setting</span></span>

<span data-ttu-id="c8d5f-109">Действие **SetField** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="c8d5f-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="c8d5f-110">**Argument**</span></span>|<span data-ttu-id="c8d5f-111">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="c8d5f-111">**Required**</span></span>|<span data-ttu-id="c8d5f-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8d5f-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c8d5f-113">_В_</span><span class="sxs-lookup"><span data-stu-id="c8d5f-113">_In_</span></span> <br/> |<span data-ttu-id="c8d5f-114">Да</span><span class="sxs-lookup"><span data-stu-id="c8d5f-114">Yes</span></span>  <br/> |<span data-ttu-id="c8d5f-115">Строка, идентифицирующая запись для работы.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="c8d5f-116">Аргумент *в* может содержать имя таблицы, запроса или инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="c8d5f-117">_Условие отбора_</span><span class="sxs-lookup"><span data-stu-id="c8d5f-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="c8d5f-118">Нет</span><span class="sxs-lookup"><span data-stu-id="c8d5f-118">No</span></span>  <br/> |<span data-ttu-id="c8d5f-119">Строковое выражение, используемое для ограничения диапазона данных, на котором блок данных **макрокомандой НайтиЗапись, после** выполнения.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="c8d5f-120">К примеру, критерии эквивалентен часто предложение WHERE в выражении SQL без слова ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="c8d5f-121">Если критерии опущен, блок данных **макрокомандой НайтиЗапись, после** действует на весь домен, указанный в аргументе *в* .</span><span class="sxs-lookup"><span data-stu-id="c8d5f-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="c8d5f-122">Поля, который включен в условия также должны входить в *в* поле.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="c8d5f-123">_Псевдоним_</span><span class="sxs-lookup"><span data-stu-id="c8d5f-123">_Alias_</span></span> <br/> |<span data-ttu-id="c8d5f-124">Нет</span><span class="sxs-lookup"><span data-stu-id="c8d5f-124">No</span></span>  <br/> |<span data-ttu-id="c8d5f-125">Строка, которая предоставляет альтернативное имя для записи, указанный в аргументе *в* .</span><span class="sxs-lookup"><span data-stu-id="c8d5f-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="c8d5f-126">Позволяет сократить имя таблицы для последующих ссылок избежать возможных неоднозначных ссылок.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="c8d5f-127">Если *псевдоним* не указан, будут использовать имя таблицы или запроса в качестве псевдоним.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8d5f-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="c8d5f-128">Remarks</span></span>

<span data-ttu-id="c8d5f-129">Если условиям, указанным *в* и *Где условие* аргументы указывает более одной записи, затем **макрокомандой НайтиЗапись, после** блока данных будет работать только первой записи.</span><span class="sxs-lookup"><span data-stu-id="c8d5f-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="c8d5f-130">Если *Условие* или, если *в* содержит записи не соответствует ни одна запись, **макрокомандой НайтиЗапись, после** создает пустую запись, в которой все поля содержат значение **Null** .</span><span class="sxs-lookup"><span data-stu-id="c8d5f-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

