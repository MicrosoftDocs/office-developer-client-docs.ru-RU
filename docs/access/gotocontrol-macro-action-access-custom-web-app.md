---
title: Макрокоманда GoToControl (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Макрокоманда GoToControl позволяет переместить фокус на указанный элемент управления в текущей записи открытого представления.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806945"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="fe6fd-103">Макрокоманда GoToControl (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="fe6fd-103">GoToControl Macro Action (Access 2013 custom web app)</span></span>

<span data-ttu-id="fe6fd-104">Макрокоманда **GoToControl** позволяет переместить фокус на указанный элемент управления в текущей записи открытого представления.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="fe6fd-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="fe6fd-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-RU/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-RU/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="fe6fd-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="fe6fd-107">Setting</span></span>

<span data-ttu-id="fe6fd-108">Макрокоманда **GoToControl** имеет указанный ниже аргумент.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="fe6fd-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="fe6fd-109">**Action argument**</span></span>|<span data-ttu-id="fe6fd-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe6fd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe6fd-111">**Имя элемента управления**</span><span class="sxs-lookup"><span data-stu-id="fe6fd-111">**Control Name**</span></span> <br/> |<span data-ttu-id="fe6fd-112">Имя поля или элемента управления, куда необходимо переместить фокус.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="fe6fd-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe6fd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe6fd-114">Remarks</span></span>

<span data-ttu-id="fe6fd-115">Эта макрокоманда позволяет переместить фокус на определенное поле или на другой элемент управления.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="fe6fd-116">Кроме того, можно использовать эту макрокоманду для навигации в форме в соответствии с определенными условиями.</span><span class="sxs-lookup"><span data-stu-id="fe6fd-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="fe6fd-117">Например, если пользователь введет "Нет" в элементе управления "Брак" формы медицинского страхования, фокус может сразу автоматически переместиться на элемент управления, следующий за элементом управления "Имя партнера".</span><span class="sxs-lookup"><span data-stu-id="fe6fd-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

