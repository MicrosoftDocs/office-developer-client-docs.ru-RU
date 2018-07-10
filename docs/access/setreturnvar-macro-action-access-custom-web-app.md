---
title: Действия макроса SetReturnVar (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Действие SetReturnVar создает возвращаемое переменной и устанавливает для определенного значения.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807135"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="4746f-103">Действия макроса SetReturnVar (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="4746f-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="4746f-104">Действие **SetReturnVar** создает возвращаемое переменной и устанавливает для определенного значения.</span><span class="sxs-lookup"><span data-stu-id="4746f-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4746f-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4746f-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="4746f-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="4746f-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4746f-107">**SetReturnVar** действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="4746f-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="4746f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4746f-108">Setting</span></span>

<span data-ttu-id="4746f-109">Действие **SetReturnVar** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="4746f-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="4746f-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="4746f-110">**Argument name**</span></span>|<span data-ttu-id="4746f-111">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="4746f-111">**Required**</span></span>|<span data-ttu-id="4746f-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4746f-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4746f-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="4746f-113">_Name_</span></span> <br/> |<span data-ttu-id="4746f-114">Да</span><span class="sxs-lookup"><span data-stu-id="4746f-114">Yes</span></span>  <br/> |<span data-ttu-id="4746f-115">Строка, задающая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="4746f-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="4746f-116">_Выражение_</span><span class="sxs-lookup"><span data-stu-id="4746f-116">_Expression_</span></span> <br/> |<span data-ttu-id="4746f-117">Да</span><span class="sxs-lookup"><span data-stu-id="4746f-117">Yes</span></span>  <br/> |<span data-ttu-id="4746f-118">Выражение, которое будет использоваться для задания значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="4746f-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="4746f-119">Перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="4746f-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="4746f-120">Можно нажмите кнопку **Построить** для задания аргумента с помощью **Построителя выражений** .</span><span class="sxs-lookup"><span data-stu-id="4746f-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4746f-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="4746f-121">Remarks</span></span>

<span data-ttu-id="4746f-122">Действие **SetReturnVar** используется для создания **ReturnVar**, которая является переменной, которая может использоваться макросы, которые могут вызывать макрос данных с помощью **ЗапускМакросаДанных** .</span><span class="sxs-lookup"><span data-stu-id="4746f-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="4746f-123">После создания **ReturnVar** с **SetReturnVar** действие вызова макроса можно использовать в выражении.</span><span class="sxs-lookup"><span data-stu-id="4746f-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="4746f-124">Например при создании **ReturnVar** с именем **UpdateSuccess**, можно использовать переменную, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="4746f-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="4746f-125">Действие **SetReturnVar** можно использовать только в именованных макросов данных.</span><span class="sxs-lookup"><span data-stu-id="4746f-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="4746f-126">Он недоступен в макросах данных, подключенные к события макрос данных.</span><span class="sxs-lookup"><span data-stu-id="4746f-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

