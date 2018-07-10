---
title: Функция объединить (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Возвращает строку, которая является результат объединения двух или нескольких строковых значений.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806925"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="01e67-103">Функция объединить (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="01e67-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="01e67-104">Возвращает строку, которая является результат объединения двух или нескольких строковых значений.</span><span class="sxs-lookup"><span data-stu-id="01e67-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="01e67-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="01e67-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="01e67-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="01e67-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="01e67-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01e67-107">Syntax</span></span>

<span data-ttu-id="01e67-108">**Объединить** (*Значение1*, *значение2*... [*ValueN*])</span><span class="sxs-lookup"><span data-stu-id="01e67-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="01e67-109">Функция **Объединить** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="01e67-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="01e67-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="01e67-110">**Argument Name**</span></span>|<span data-ttu-id="01e67-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01e67-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01e67-112">Значение</span><span class="sxs-lookup"><span data-stu-id="01e67-112">Value</span></span>  <br/> |<span data-ttu-id="01e67-113">Строковое значение для объединения в другие значения.</span><span class="sxs-lookup"><span data-stu-id="01e67-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01e67-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="01e67-114">Remarks</span></span>

<span data-ttu-id="01e67-115">**Объединить** с переменным числом строковые аргументы и объединяет их в одну строку.</span><span class="sxs-lookup"><span data-stu-id="01e67-115">**Concat** takes a variable number of string arguments and concatenates them into a single string.</span></span> <span data-ttu-id="01e67-116">Не менее двух строковые аргументы являются обязательными; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="01e67-116">A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="01e67-117">Все аргументы неявно преобразуются в строковых данных и затем объединяется.</span><span class="sxs-lookup"><span data-stu-id="01e67-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="01e67-118">Пример</span><span class="sxs-lookup"><span data-stu-id="01e67-118">Example</span></span>

<span data-ttu-id="01e67-119">Следующее выражение можно использовать для отображения полного имени пользователя которых таблицы содержит полей FirstName, LastName и MiddleInitial.</span><span class="sxs-lookup"><span data-stu-id="01e67-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="01e67-120">Если MiddleInitial поле не заполнено, чтобы отобразить полное имя объединяются только поля имя и Фамилия.</span><span class="sxs-lookup"><span data-stu-id="01e67-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


