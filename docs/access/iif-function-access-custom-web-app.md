---
title: Функция IIf (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Проверяет, будет ли условие соблюдено и возвращает одно значение, если значение TRUE, от друга в том случае, если оно равно FALSE.
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806933"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="a4497-103">Функция IIf (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="a4497-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="a4497-104">Проверяет, будет ли условие соблюдено и возвращает одно значение, если значение TRUE, от друга в том случае, если оно равно FALSE.</span><span class="sxs-lookup"><span data-stu-id="a4497-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a4497-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a4497-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a4497-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="a4497-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a4497-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4497-107">Syntax</span></span>

<span data-ttu-id="a4497-108">**IIf** (*Условие*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="a4497-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="a4497-109">Функция **IIf** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a4497-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a4497-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="a4497-110">**Argument name**</span></span>|<span data-ttu-id="a4497-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a4497-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a4497-112">*Условие*</span><span class="sxs-lookup"><span data-stu-id="a4497-112">*Condition*</span></span>  <br/> |<span data-ttu-id="a4497-113">Выражение, которое требуется вычислить.</span><span class="sxs-lookup"><span data-stu-id="a4497-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a4497-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="a4497-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="a4497-115">Значение или выражение, возвращаемое, если *условие* равно True.</span><span class="sxs-lookup"><span data-stu-id="a4497-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="a4497-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="a4497-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="a4497-117">Значение или выражение, возвращаемое, если *условие* равно False.</span><span class="sxs-lookup"><span data-stu-id="a4497-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="a4497-118">Пример</span><span class="sxs-lookup"><span data-stu-id="a4497-118">Example</span></span>

<span data-ttu-id="a4497-119">Следующее выражение можно использовать для отображения полного имени пользователя которых таблицы содержит полей FirstName, LastName и MiddleInitial.</span><span class="sxs-lookup"><span data-stu-id="a4497-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="a4497-120">Если MiddleInitial поле не заполнено, чтобы отобразить полное имя объединяются только поля имя и Фамилия.</span><span class="sxs-lookup"><span data-stu-id="a4497-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


