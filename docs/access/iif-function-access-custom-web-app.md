---
title: Функция IIf (Доступ к настраиваемой веб-приложении)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Проверяет, выполнены ли условия, и возвращает одно значение, если значение TRUE другого, если оно FALSE.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439081"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="6aa6a-103">Функция IIf (Доступ к настраиваемой веб-приложении)</span><span class="sxs-lookup"><span data-stu-id="6aa6a-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="6aa6a-104">Проверяет, выполнены ли условия, и возвращает одно значение, если значение TRUE другого, если оно FALSE.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6aa6a-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="6aa6a-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6aa6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6aa6a-107">Syntax</span></span>

<span data-ttu-id="6aa6a-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="6aa6a-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="6aa6a-109">Функция **IIf** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6aa6a-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="6aa6a-110">**Argument name**</span></span>|<span data-ttu-id="6aa6a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6aa6a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6aa6a-112">*Condition*</span><span class="sxs-lookup"><span data-stu-id="6aa6a-112">*Condition*</span></span>  <br/> |<span data-ttu-id="6aa6a-113">Выражение, которое необходимо оценить.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="6aa6a-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="6aa6a-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="6aa6a-115">Значение или выражение возвращается,  *если условие*  true.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="6aa6a-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="6aa6a-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="6aa6a-117">Значение или выражение, возвращаемое,  *если условие*  является ложным.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="6aa6a-118">Пример</span><span class="sxs-lookup"><span data-stu-id="6aa6a-118">Example</span></span>

<span data-ttu-id="6aa6a-119">Следующее выражение можно использовать для отображения полного имени человека, в котором таблица содержит поля FirstName, MiddleInitial и LastName.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="6aa6a-120">Если поле MiddleInitial пусто, для отображения полного имени объединяются только поля FirstName и LastName.</span><span class="sxs-lookup"><span data-stu-id="6aa6a-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


