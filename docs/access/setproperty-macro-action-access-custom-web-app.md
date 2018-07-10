---
title: Действия макроса SetProperty (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Действия SetProperty можно использовать для задания свойства для элемента управления в представлении.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807106"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="c75d8-103">Действия макроса SetProperty (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="c75d8-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="c75d8-104">Действия **SetProperty** можно использовать для задания свойства для элемента управления в представлении.</span><span class="sxs-lookup"><span data-stu-id="c75d8-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c75d8-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c75d8-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="c75d8-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="c75d8-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="c75d8-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="c75d8-107">Setting</span></span>

<span data-ttu-id="c75d8-108">Действия **SetProperty** содержит аргументы, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c75d8-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="c75d8-109">**Аргумент действия**</span><span class="sxs-lookup"><span data-stu-id="c75d8-109">**Action argument**</span></span>|<span data-ttu-id="c75d8-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c75d8-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c75d8-111">_Имя элемента управления_</span><span class="sxs-lookup"><span data-stu-id="c75d8-111">_Control Name_</span></span> <br/> |<span data-ttu-id="c75d8-112">Введите имя в поле или элемент управления, для которого требуется задать значение свойства.</span><span class="sxs-lookup"><span data-stu-id="c75d8-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="c75d8-113">Оставьте данный аргумент пустым, чтобы задать свойства для представления.</span><span class="sxs-lookup"><span data-stu-id="c75d8-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="c75d8-114">_Свойство_</span><span class="sxs-lookup"><span data-stu-id="c75d8-114">_Property_</span></span> <br/> |<span data-ttu-id="c75d8-115">Выберите свойство, которое требуется установить.</span><span class="sxs-lookup"><span data-stu-id="c75d8-115">Select the property that you want to set.</span></span> <span data-ttu-id="c75d8-116">**В этой статье представлен список свойств, которые можно настроить с помощью этого действия см.**</span><span class="sxs-lookup"><span data-stu-id="c75d8-116">See the **Remarks** section in this article for a list of the properties that can be set by using this action.</span></span>  <br/> |
| <span data-ttu-id="c75d8-117">_Значение_</span><span class="sxs-lookup"><span data-stu-id="c75d8-117">_Value_</span></span> <br/> |<span data-ttu-id="c75d8-118">Введите значение, является ли данное свойство должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="c75d8-118">Type the value that the property is to be set to.</span></span> <span data-ttu-id="c75d8-119">Для свойства, значения которых являются Да или нет, используйте **значение -1** для Да и **0** для нет.</span><span class="sxs-lookup"><span data-stu-id="c75d8-119">For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c75d8-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="c75d8-120">Remarks</span></span>

<span data-ttu-id="c75d8-121">Действия **SetProperty** можно использовать для настройки следующих свойств элемента управления:</span><span class="sxs-lookup"><span data-stu-id="c75d8-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="c75d8-122">Caption</span><span class="sxs-lookup"><span data-stu-id="c75d8-122">Caption</span></span>
    
- <span data-ttu-id="c75d8-123">Включена</span><span class="sxs-lookup"><span data-stu-id="c75d8-123">Enabled</span></span>
    
- <span data-ttu-id="c75d8-124">Цвет текста</span><span class="sxs-lookup"><span data-stu-id="c75d8-124">ForeColor</span></span>
    
- <span data-ttu-id="c75d8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c75d8-125">Value</span></span>
    
- <span data-ttu-id="c75d8-126">Visible</span><span class="sxs-lookup"><span data-stu-id="c75d8-126">Visible</span></span>
    
<span data-ttu-id="c75d8-127">Если ввести недопустимое значение ** *значение* ** аргумент, ошибка не происходит, но доступа могут измените свойство на разные значения, в зависимости от того, как оно интерпретирует аргумента.</span><span class="sxs-lookup"><span data-stu-id="c75d8-127">If you enter an invalid value for the ** *Value* ** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

