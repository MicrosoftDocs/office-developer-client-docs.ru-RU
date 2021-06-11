---
title: Функция Concat (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Возвращает строку, которая является результатом объединения двух или более значений строки.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423274"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="cd12b-103">Функция Concat (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="cd12b-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="cd12b-104">Возвращает строку, которая является результатом объединения двух или более значений строки.</span><span class="sxs-lookup"><span data-stu-id="cd12b-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cd12b-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cd12b-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="cd12b-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="cd12b-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cd12b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd12b-107">Syntax</span></span>

<span data-ttu-id="cd12b-108">**Concat** (*Value1*, *Value2*, ... [*ValueN*])</span><span class="sxs-lookup"><span data-stu-id="cd12b-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="cd12b-109">Функция **Concat** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="cd12b-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="cd12b-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="cd12b-110">**Argument Name**</span></span>|<span data-ttu-id="cd12b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cd12b-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd12b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cd12b-112">Value</span></span>  <br/> |<span data-ttu-id="cd12b-113">Значение строки, примыкает к другим значениям.</span><span class="sxs-lookup"><span data-stu-id="cd12b-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd12b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd12b-114">Remarks</span></span>

<span data-ttu-id="cd12b-115">**Concat** принимает переменную строку аргументов и соедает их в одну строку.</span><span class="sxs-lookup"><span data-stu-id="cd12b-115">**Concat** takes a variable number of string arguments and concatenates them into a single string.</span></span> <span data-ttu-id="cd12b-116">Требуется минимум два аргумента строки; в противном случае будет поднята ошибка.</span><span class="sxs-lookup"><span data-stu-id="cd12b-116">A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="cd12b-117">Все аргументы неявно преобразуются в типы данных строки и затем согласуются.</span><span class="sxs-lookup"><span data-stu-id="cd12b-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="cd12b-118">Пример</span><span class="sxs-lookup"><span data-stu-id="cd12b-118">Example</span></span>

<span data-ttu-id="cd12b-119">Следующее выражение можно использовать для отображения полного имени человека, в котором таблица содержит поля FirstName, MiddleInitial и LastName.</span><span class="sxs-lookup"><span data-stu-id="cd12b-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="cd12b-120">Если поле MiddleInitial пусто, для отображения полного имени объединяются только поля FirstName и LastName.</span><span class="sxs-lookup"><span data-stu-id="cd12b-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


