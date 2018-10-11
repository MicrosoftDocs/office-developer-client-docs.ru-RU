---
title: Диалоговое окно настраиваемых свойств элемента управления ActiveX
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481774"
---
# <a name="activex-controls-custom-properties-dialog-box"></a><span data-ttu-id="b99c9-102">Диалоговое окно настраиваемых свойств элемента управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b99c9-102">ActiveX Control's Custom Properties Dialog Box</span></span>

<span data-ttu-id="b99c9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b99c9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b99c9-104">При задании свойств элементов управления ActiveX, может требуются или предпочитаете использовать диалоговое окно настраиваемых свойств элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b99c9-104">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box.</span></span> <span data-ttu-id="b99c9-105">Это диалоговое окно настраиваемых свойств является альтернативой в списке свойств в окне свойств Microsoft Access для задания свойств элемента управления ActiveX в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="b99c9-105">This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="b99c9-106">Эти сведения применяется только к элементам управления ActiveX в среде базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b99c9-106">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>



## <a name="two-ways-to-set-properties"></a><span data-ttu-id="b99c9-107">Два способа настройки свойств</span><span class="sxs-lookup"><span data-stu-id="b99c9-107">Two Ways to Set Properties</span></span>

<span data-ttu-id="b99c9-108">Причина диалоговое окно настраиваемых свойств — укажите, что не все приложения, с помощью элементов управления ActiveX на листе свойств, как показано в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b99c9-108">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access.</span></span> <span data-ttu-id="b99c9-109">Диалоговое окно настраиваемых свойств предоставляет интерфейс для установки свойств ключевых элемента управления независимо от того, в интерфейсе размещения приложения.</span><span class="sxs-lookup"><span data-stu-id="b99c9-109">The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="b99c9-110">Для некоторых свойств элемента управления ActiveX можно выбрать один из этих двух местоположений для свойства:</span><span class="sxs-lookup"><span data-stu-id="b99c9-110">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

  - <span data-ttu-id="b99c9-111">Окно свойств Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b99c9-111">The Microsoft Access property sheet.</span></span>

  - <span data-ttu-id="b99c9-112">Диалоговое окно настраиваемых свойств элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b99c9-112">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="b99c9-113">В некоторых случаях диалоговое окно настраиваемых свойств — это единственный способ задания свойства в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="b99c9-113">In some cases, the custom properties dialog box is the only way to set a property in Design view.</span></span> <span data-ttu-id="b99c9-114">Это обычно ситуации, когда интерфейс, необходимый для задания свойства не работает в окне свойств Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b99c9-114">This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet.</span></span> <span data-ttu-id="b99c9-115">Например свойство **GridFont** для элемента управления календаря имеет число аргументов; нельзя установить более одного аргумента каждого свойства в окне свойств Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b99c9-115">For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="b99c9-116">Поиск диалоговое окно настраиваемых свойств</span><span class="sxs-lookup"><span data-stu-id="b99c9-116">Finding the Custom Properties Dialog Box</span></span>

<span data-ttu-id="b99c9-117">Не все элементы управления ActiveX предоставляют диалоговое окно настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="b99c9-117">Not all ActiveX controls provide a custom properties dialog box.</span></span> <span data-ttu-id="b99c9-118">Чтобы определить, попадают ли элемент управления предоставляет настраиваемого диалогового окна свойств, внешнего вида для **настраиваемого** свойства в окне свойств Microsoft Access для данного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b99c9-118">To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control.</span></span> <span data-ttu-id="b99c9-119">Если список свойств содержит имя **настраиваемого**, элемент управления предоставляет диалоговое окно настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="b99c9-119">If the list of properties contains the name **Custom**, then the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="b99c9-120">С помощью диалогового окна настраиваемых свойств</span><span class="sxs-lookup"><span data-stu-id="b99c9-120">Using the Custom Properties Dialog Box</span></span>

<span data-ttu-id="b99c9-121">После нажатия кнопки **настраиваемого** поля свойства в окне свойств Microsoft Access, нажмите кнопку **Построить** справа от поля свойства для отображения элемента управления настраиваемого свойства, часто представлена в виде диалоговое окно с вкладками.</span><span class="sxs-lookup"><span data-stu-id="b99c9-121">After you click the **Custom** property box in the Microsoft Access property sheet, click the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box.</span></span> <span data-ttu-id="b99c9-122">Перейдите на вкладку, которая содержит интерфейс для установки свойств, которые требуется установить.</span><span class="sxs-lookup"><span data-stu-id="b99c9-122">Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="b99c9-123">После внесения изменений на вкладке можно часто применить эти изменения немедленно, нажмите кнопку **Применить** (если они имеются).</span><span class="sxs-lookup"><span data-stu-id="b99c9-123">After you make changes on one tab, you can often apply those changes immediately by clicking the **Apply** button (if provided).</span></span> <span data-ttu-id="b99c9-124">Другие вкладки для настройки других свойств при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b99c9-124">You can click other tabs to set other properties as needed.</span></span> <span data-ttu-id="b99c9-125">Чтобы утвердить все изменения, внесенные в диалоговом окне настраиваемые свойства, нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="b99c9-125">To approve all changes made in the custom properties dialog box, click the **OK** button.</span></span> <span data-ttu-id="b99c9-126">Чтобы вернуться на страницу свойств Microsoft Access без изменения все параметры свойств, нажмите кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="b99c9-126">To return to the Microsoft Access property sheet without changing any property settings, click the **Cancel** button.</span></span>

<span data-ttu-id="b99c9-127">Можно также просмотреть диалоговое окно настраиваемых свойств, нажав кнопку команда **Свойства** элемента управления ActiveX в меню **Правка** команду **объект** (например, **Объект элемента управления календаря**) или, щелкнув этой же команды контекстное меню для элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b99c9-127">You can also view the custom properties dialog box by clicking the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by clicking this same subcommand on the shortcut menu for the ActiveX control.</span></span> <span data-ttu-id="b99c9-128">Кроме того некоторые свойства в окне свойств Microsoft Access для элемента управления ActiveX, как **GridFontColor** свойств элемента управления "Календарь", имеют **построения** кнопку справа от поля свойства.</span><span class="sxs-lookup"><span data-stu-id="b99c9-128">In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box.</span></span> <span data-ttu-id="b99c9-129">При нажатии кнопки **создания** , диалоговое окно настраиваемых свойств отображается с соответствующей вкладке (например, **цвета**).</span><span class="sxs-lookup"><span data-stu-id="b99c9-129">When you click the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

