---
title: SetProperty Macro Action (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Действие SetProperty можно использовать для набора свойства для управления представлением.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438031"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="1a5b1-103">SetProperty Macro Action (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="1a5b1-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="1a5b1-104">Действие **SetProperty можно использовать** для набора свойства для управления представлением.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1a5b1-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="1a5b1-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1a5b1-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="1a5b1-107">Setting</span></span>

<span data-ttu-id="1a5b1-108">Действие **SetProperty** имеет аргументы, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="1a5b1-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="1a5b1-109">**Action argument**</span></span>|<span data-ttu-id="1a5b1-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1a5b1-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1a5b1-111">_Имя элемента управления_</span><span class="sxs-lookup"><span data-stu-id="1a5b1-111">_Control Name_</span></span> <br/> |<span data-ttu-id="1a5b1-112">Введите имя поля или управления, для которого необходимо установить значение свойства.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="1a5b1-113">Оставьте этот аргумент пустым, чтобы установить свойство для представления.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="1a5b1-114">_Property_</span><span class="sxs-lookup"><span data-stu-id="1a5b1-114">_Property_</span></span> <br/> |<span data-ttu-id="1a5b1-115">Выберите свойство, которое необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-115">Select the property that you want to set.</span></span> <span data-ttu-id="1a5b1-116">Список  свойств, которые можно установить с помощью этого действия, см. в разделе Замечания в этой статье.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-116">See the **Remarks** section in this article for a list of the properties that can be set by using this action.</span></span>  <br/> |
| <span data-ttu-id="1a5b1-117">_Значение_</span><span class="sxs-lookup"><span data-stu-id="1a5b1-117">_Value_</span></span> <br/> |<span data-ttu-id="1a5b1-118">Введите значение, за которое должно быть установлено свойство.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-118">Type the value that the property is to be set to.</span></span> <span data-ttu-id="1a5b1-119">Для свойств, значения которых либо да, либо нет, используйте **-1** для да и **0** для No.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-119">For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a5b1-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a5b1-120">Remarks</span></span>

<span data-ttu-id="1a5b1-121">Вы можете использовать **действие SetProperty** для набора следующих свойств управления:</span><span class="sxs-lookup"><span data-stu-id="1a5b1-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="1a5b1-122">Подпись</span><span class="sxs-lookup"><span data-stu-id="1a5b1-122">Caption</span></span>
    
- <span data-ttu-id="1a5b1-123">Включено</span><span class="sxs-lookup"><span data-stu-id="1a5b1-123">Enabled</span></span>
    
- <span data-ttu-id="1a5b1-124">ForeColor</span><span class="sxs-lookup"><span data-stu-id="1a5b1-124">ForeColor</span></span>
    
- <span data-ttu-id="1a5b1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1a5b1-125">Value</span></span>
    
- <span data-ttu-id="1a5b1-126">Visible</span><span class="sxs-lookup"><span data-stu-id="1a5b1-126">Visible</span></span>
    
<span data-ttu-id="1a5b1-127">Если вы вводите недействительное значение для аргумента \*\* *Value* \*\* , ошибки не возникает, но Access может изменить свойство на другое, в зависимости от того, как он интерпретирует аргумент.</span><span class="sxs-lookup"><span data-stu-id="1a5b1-127">If you enter an invalid value for the \*\* *Value* \*\* argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

