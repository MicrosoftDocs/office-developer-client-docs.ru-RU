---
title: Блок данных ДляКаждойЗаписи (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Блок данных ДляКаждойЗаписи повторяет набор инструкций для каждой записи в домене.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806967"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="1577b-103">Блок данных ДляКаждойЗаписи (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="1577b-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="1577b-104">Блок данных **ДляКаждойЗаписи** повторяет набор инструкций для каждой записи в домене.</span><span class="sxs-lookup"><span data-stu-id="1577b-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1577b-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1577b-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="1577b-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="1577b-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1577b-107">Блок данных **ДляКаждойЗаписи** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="1577b-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1577b-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="1577b-108">Setting</span></span>

<span data-ttu-id="1577b-109">Действие **ДляКаждойЗаписи** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1577b-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="1577b-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="1577b-110">**Argument name**</span></span>|<span data-ttu-id="1577b-111">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="1577b-111">**Required**</span></span>|<span data-ttu-id="1577b-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1577b-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1577b-113">**В**</span><span class="sxs-lookup"><span data-stu-id="1577b-113">**In**</span></span> <br/> |<span data-ttu-id="1577b-114">Да</span><span class="sxs-lookup"><span data-stu-id="1577b-114">Yes</span></span>  <br/> |<span data-ttu-id="1577b-115">Строка, идентифицирующая домена записей для работы с.</span><span class="sxs-lookup"><span data-stu-id="1577b-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="1577b-116">Аргумент *в* может содержать имя таблицы, запроса или инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="1577b-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="1577b-117">**Примечание**: указанный домен не может включать данные, хранящиеся в связанной таблице или источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="1577b-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="1577b-118">**Условие отбора**</span><span class="sxs-lookup"><span data-stu-id="1577b-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="1577b-119">Нет</span><span class="sxs-lookup"><span data-stu-id="1577b-119">No</span></span>  <br/> |<span data-ttu-id="1577b-120">Строковое выражение, используемое для ограничения диапазона данных, на котором блок данных **ДляКаждойЗаписи** выполняется.</span><span class="sxs-lookup"><span data-stu-id="1577b-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="1577b-121">К примеру, критерии эквивалентен часто предложение WHERE в выражении SQL без слова ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="1577b-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="1577b-122">Если критерии опускаются, блок данных **ДляКаждойЗаписи** действует на весь домен, указанный в аргументе *в* .</span><span class="sxs-lookup"><span data-stu-id="1577b-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="1577b-123">Поля, который включен в условия также должны входить в *в* поле.</span><span class="sxs-lookup"><span data-stu-id="1577b-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="1577b-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="1577b-124">**Alias**</span></span> <br/> |<span data-ttu-id="1577b-125">Нет</span><span class="sxs-lookup"><span data-stu-id="1577b-125">No</span></span>  <br/> |<span data-ttu-id="1577b-126">Строка, которая предоставляет альтернативное имя для домена, указанный в аргументе *в* .</span><span class="sxs-lookup"><span data-stu-id="1577b-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="1577b-127">Позволяет сократить имя таблицы для последующих ссылок избежать возможных неоднозначных ссылок.</span><span class="sxs-lookup"><span data-stu-id="1577b-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="1577b-128">Если *псевдоним* не указан, будут использовать имя таблицы или запроса в качестве псевдоним.</span><span class="sxs-lookup"><span data-stu-id="1577b-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1577b-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="1577b-129">Remarks</span></span>

<span data-ttu-id="1577b-130">Действие **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** используется для выхода из блока **ДляКаждойЗаписи** данных немедленно.</span><span class="sxs-lookup"><span data-stu-id="1577b-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

