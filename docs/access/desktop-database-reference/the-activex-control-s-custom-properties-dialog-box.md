---
title: Диалоговое окно настраиваемых свойств элемента ActiveX
TOCTitle: ActiveX control custom properties dialog box
description: Это диалоговое окно настраиваемого свойства предоставляет альтернативу списку свойств на листе свойств Microsoft Access для ActiveX свойств управления в представлении конструктора.
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4574abc86e6eacd38721e601d26c8b8fbf0a0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314107"
---
# <a name="activex-control-custom-properties-dialog-box"></a><span data-ttu-id="c2c52-103">Диалоговое окно настраиваемых свойств элемента ActiveX</span><span class="sxs-lookup"><span data-stu-id="c2c52-103">ActiveX control custom properties dialog box</span></span>

<span data-ttu-id="c2c52-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2c52-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2c52-105">При настройке свойств ActiveX может потребоваться или использовать диалоговое окно настраиваемого свойства этого управления.</span><span class="sxs-lookup"><span data-stu-id="c2c52-105">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box.</span></span> <span data-ttu-id="c2c52-106">Это диалоговое окно настраиваемого свойства предоставляет альтернативу списку свойств на листе свойств Microsoft Access для ActiveX свойств управления в представлении конструктора.</span><span class="sxs-lookup"><span data-stu-id="c2c52-106">This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="c2c52-107">Эти сведения применимы только к ActiveX в среде базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c2c52-107">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>

## <a name="two-ways-to-set-properties"></a><span data-ttu-id="c2c52-108">Два способа установить свойства</span><span class="sxs-lookup"><span data-stu-id="c2c52-108">Two ways to set properties</span></span>

<span data-ttu-id="c2c52-109">Причина в диалоговом окне настраиваемого свойства заключается в том, что не все приложения, ActiveX элементы управления, предоставляют таблицу свойств, похожую на таблицу в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c2c52-109">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access.</span></span> <span data-ttu-id="c2c52-110">Диалоговое окно настраиваемого свойства предоставляет интерфейс для настройки свойств управления ключами независимо от интерфейса, предоставленного приложением размещения.</span><span class="sxs-lookup"><span data-stu-id="c2c52-110">The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="c2c52-111">Для некоторых ActiveX свойств управления можно выбрать один из этих двух расположений, чтобы установить свойство:</span><span class="sxs-lookup"><span data-stu-id="c2c52-111">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

- <span data-ttu-id="c2c52-112">Таблица свойств Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c2c52-112">The Microsoft Access property sheet.</span></span>
- <span data-ttu-id="c2c52-113">Диалоговое ActiveX настраиваемые свойства этого управления.</span><span class="sxs-lookup"><span data-stu-id="c2c52-113">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="c2c52-114">В некоторых случаях единственным способом настройки свойства в представлении конструктора является диалоговое окно настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="c2c52-114">In some cases, the custom properties dialog box is the only way to set a property in Design view.</span></span> <span data-ttu-id="c2c52-115">Обычно это происходит, когда интерфейс, необходимый для набора свойства, не работает в листе свойств Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c2c52-115">This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet.</span></span> <span data-ttu-id="c2c52-116">Например, свойство **GridFont** для управления "Календарь" имеет несколько аргументов; На листе свойств Microsoft Access нельзя установить более одного аргумента для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="c2c52-116">For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="c2c52-117">Диалоговое окно поиска настраиваемого свойства</span><span class="sxs-lookup"><span data-stu-id="c2c52-117">Finding the custom properties dialog box</span></span>

<span data-ttu-id="c2c52-118">Не все ActiveX предоставляют диалоговое окно настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="c2c52-118">Not all ActiveX controls provide a custom properties dialog box.</span></span> <span data-ttu-id="c2c52-119">Чтобы узнать, предоставляет ли этот пользовательский диалоговое окно свойств, наберите свойство **Custom** на листе свойств Microsoft Access для этого управления.</span><span class="sxs-lookup"><span data-stu-id="c2c52-119">To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control.</span></span> <span data-ttu-id="c2c52-120">Если список свойств содержит имя **Custom,** то в этом диалоговом окне управления будут настраиваемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c2c52-120">If the list of properties contains the name **Custom**, the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="c2c52-121">Диалоговое окно "Использование настраиваемого свойства"</span><span class="sxs-lookup"><span data-stu-id="c2c52-121">Using the custom properties dialog box</span></span>

<span data-ttu-id="c2c52-122">После выбора  настраиваемого окна свойств на листе  свойств Microsoft Access выберите кнопку "Построение" справа от окна свойств, чтобы отобразить диалоговое окно настраиваемого свойства этого управления, часто отображаемого как диалоговое окно с вкладками.</span><span class="sxs-lookup"><span data-stu-id="c2c52-122">After you choose the **Custom** property box in the Microsoft Access property sheet, choose the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box.</span></span> <span data-ttu-id="c2c52-123">Выберите вкладку с интерфейсом для настройки свойств, которые необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="c2c52-123">Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="c2c52-124">После внесения изменений на одной вкладке часто можно сразу применить эти изменения, нажатием кнопки **"Применить"** (если она есть).</span><span class="sxs-lookup"><span data-stu-id="c2c52-124">After you make changes on one tab, you can often apply those changes immediately by choosing the **Apply** button (if provided).</span></span> <span data-ttu-id="c2c52-125">Вы можете выбрать другие вкладки, чтобы при необходимости настроить другие свойства.</span><span class="sxs-lookup"><span data-stu-id="c2c52-125">You can choose other tabs to set other properties as needed.</span></span> <span data-ttu-id="c2c52-126">Чтобы утвердить все изменения, внесенные в диалоговом окне настраиваемого свойства, выберите кнопку **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="c2c52-126">To approve all changes made in the custom properties dialog box, choose the **OK** button.</span></span> <span data-ttu-id="c2c52-127">Чтобы вернуться на таблицу свойств Microsoft Access без изменения параметров свойств, выберите кнопку **"Отмена".**</span><span class="sxs-lookup"><span data-stu-id="c2c52-127">To return to the Microsoft Access property sheet without changing any property settings, choose the **Cancel** button.</span></span>

<span data-ttu-id="c2c52-128">Вы также можете просмотреть диалоговое окно настраиваемого свойства, выбрав подкоманда  **"Свойства"** команды "Объект управления ActiveX" (например, "Объект управления календарем") в меню "Правка" или выбрав этот же подкоманда в ярлыке для ActiveX управления. </span><span class="sxs-lookup"><span data-stu-id="c2c52-128">You can also view the custom properties dialog box by choosing the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by choosing this same subcommand on the shortcut menu for the ActiveX control.</span></span> <span data-ttu-id="c2c52-129">Кроме того, некоторые свойства на листе свойств Microsoft Access для ActiveX, такие как **свойство GridFontColor** этого объекта, имеют кнопку "Построение" справа от окна свойств. </span><span class="sxs-lookup"><span data-stu-id="c2c52-129">In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box.</span></span> <span data-ttu-id="c2c52-130">При **нажатии** кнопки "Построение" отображается диалоговое окно настраиваемого свойства с соответствующей вкладками (например, **"Цвета").**</span><span class="sxs-lookup"><span data-stu-id="c2c52-130">When you choose the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

