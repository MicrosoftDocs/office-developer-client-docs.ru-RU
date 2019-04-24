---
title: Функция Concat (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Возвращает строку, которая является результатом объединения двух или более строковых значений.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282294"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="13c03-103">Функция Concat (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="13c03-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="13c03-104">Возвращает строку, которая является результатом объединения двух или более строковых значений.</span><span class="sxs-lookup"><span data-stu-id="13c03-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="13c03-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="13c03-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="13c03-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="13c03-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13c03-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13c03-107">Syntax</span></span>

<span data-ttu-id="13c03-108">**Concat** (*Значение1*, *Значение2*,... [*Валуен*])</span><span class="sxs-lookup"><span data-stu-id="13c03-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="13c03-109">Функция **concat** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="13c03-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="13c03-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="13c03-110">**Argument Name**</span></span>|<span data-ttu-id="13c03-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13c03-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13c03-112">Значение</span><span class="sxs-lookup"><span data-stu-id="13c03-112">Value</span></span>  <br/> |<span data-ttu-id="13c03-113">Строковое значение для сцепления с другими значениями.</span><span class="sxs-lookup"><span data-stu-id="13c03-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13c03-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="13c03-114">Remarks</span></span>

<span data-ttu-id="13c03-115">**Сцепление** принимает переменное число строковых аргументов и объединяет их в одну строку.</span><span class="sxs-lookup"><span data-stu-id="13c03-115">**Concat** takes a variable number of string arguments and concatenates them into a single string.</span></span> <span data-ttu-id="13c03-116">Необходимо указать не менее двух строковых аргументов; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="13c03-116">A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="13c03-117">Все аргументы неявно преобразуются в типы данных String, а затем сцепляются.</span><span class="sxs-lookup"><span data-stu-id="13c03-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="13c03-118">Пример</span><span class="sxs-lookup"><span data-stu-id="13c03-118">Example</span></span>

<span data-ttu-id="13c03-119">Следующее выражение можно использовать для отображения полного имени пользователя, где в таблице содержатся поля FirstName, Миддлеинитиал и LastName.</span><span class="sxs-lookup"><span data-stu-id="13c03-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="13c03-120">Если поле Миддлеинитиал не заполнено, только поля FirstName и LastName будут объединены для отображения полного имени.</span><span class="sxs-lookup"><span data-stu-id="13c03-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


