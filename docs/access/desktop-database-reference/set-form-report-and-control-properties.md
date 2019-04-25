---
title: Настройка свойств форм, отчетов и элементов управления
TOCTitle: Set form, report, and control properties
description: Каждая форма, отчет, раздел и элемент управления содержит параметры свойств, которые можно настроить для изменения оформления или поведения определенного элемента в Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308738"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="667d3-103">Настройка свойств форм, отчетов и элементов управления</span><span class="sxs-lookup"><span data-stu-id="667d3-103">Set form, report, and control properties</span></span>

<span data-ttu-id="667d3-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="667d3-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="667d3-105">Каждая форма, отчет, раздел и элемент управления содержит параметры свойств, которые можно настроить для изменения оформления или поведения определенного элемента.</span><span class="sxs-lookup"><span data-stu-id="667d3-105">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item.</span></span> <span data-ttu-id="667d3-106">Просматривать и изменять свойства можно с помощью страницы свойств, макроса или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="667d3-106">You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="667d3-107">Настройка свойств</span><span class="sxs-lookup"><span data-stu-id="667d3-107">Set properties</span></span>

1. <span data-ttu-id="667d3-108">В режиме конструктора формы или конструктора отчетов выберите элемент управления, раздел, форму или отчет, для которого нужно настроить свойство.</span><span class="sxs-lookup"><span data-stu-id="667d3-108">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property.</span></span> <span data-ttu-id="667d3-109">Можно выбрать:</span><span class="sxs-lookup"><span data-stu-id="667d3-109">You can select from:</span></span>
    
   - <span data-ttu-id="667d3-110">Один или несколько элементов управления.</span><span class="sxs-lookup"><span data-stu-id="667d3-110">One or more additional controls of your choice.</span></span> <span data-ttu-id="667d3-111">Чтобы выбрать несколько элементов управления, выбирайте их, удерживая нажатой клавишу SHIFT, или перетаскивайте указатель мыши по элементам управления, которые нужно выбрать.</span><span class="sxs-lookup"><span data-stu-id="667d3-111">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="667d3-112">Если выбрано несколько элементов управления, страница свойств отобразит только те свойства, которые совпадают у выбранных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="667d3-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="667d3-113">Один раздел.</span><span class="sxs-lookup"><span data-stu-id="667d3-113">One section only</span></span> <span data-ttu-id="667d3-114">Щелкните область выделения того раздела, который нужно выбрать.</span><span class="sxs-lookup"><span data-stu-id="667d3-114">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="667d3-115">Всю форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="667d3-115">The entire form or report.</span></span> <span data-ttu-id="667d3-116">Щелкните область выделения формы или отчета в верхнем левом углу формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="667d3-116">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="667d3-117">Откройте страницу свойств, щелкнув правой кнопкой мыши объект или раздел и выбрав пункт **Свойства** в контекстном меню или нажав **Свойства** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="667d3-117">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="667d3-118">Выберите свойство, для которого нужно задать значение, и выполните одно из указанных ниже действий:</span><span class="sxs-lookup"><span data-stu-id="667d3-118">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="667d3-119">В поле свойства введите соответствующий параметр или выражение.</span><span class="sxs-lookup"><span data-stu-id="667d3-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="667d3-120">Если поле свойства содержит стрелку, щелкните ее и выберите значение в списке.</span><span class="sxs-lookup"><span data-stu-id="667d3-120">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="667d3-121">Если справа от поля свойства отображается кнопка **Построитель**, нажмите ее, чтобы открыть построитель или отобразить диалоговое окно, предоставляющее возможность выбора построителя.</span><span class="sxs-lookup"><span data-stu-id="667d3-121">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="667d3-122">Например, можно использовать построитель кода, макросов или запросов, чтобы настроить некоторые свойства.</span><span class="sxs-lookup"><span data-stu-id="667d3-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="667d3-123">Советы </span><span class="sxs-lookup"><span data-stu-id="667d3-123">Tips</span></span>

- <span data-ttu-id="667d3-124">В Microsoft Access предусмотрено поле **Масштаб** для ввода и просмотра выражений или других длинных параметров свойств.</span><span class="sxs-lookup"><span data-stu-id="667d3-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="667d3-125">Чтобы отобразить поле **Масштаб** выберите поле свойства на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="667d3-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="667d3-126">Нажмите клавиши SHIFT+F2 или щелкните правой кнопкой мыши и выберите в контекстном меню пункт **Масштаб**.</span><span class="sxs-lookup"><span data-stu-id="667d3-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="667d3-127">Для некоторых элементов управления можно задать свойство **ControlSource** путем ввода параметра свойства в самом элементе управления.</span><span class="sxs-lookup"><span data-stu-id="667d3-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="667d3-128">Вы можете изменить параметры свойства по умолчанию для типа элемента управления, чтобы создаваемые в будущем элементы управления содержали новые параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="667d3-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="667d3-129">Параметры свойства связанного элемента управления могут не совпадать с соответствующими параметрами в поле в базовой таблицы или запроса, с которым связан элемент управления.</span><span class="sxs-lookup"><span data-stu-id="667d3-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="667d3-130">Если параметры отличаются, параметры формы или отчета обычно переопределяют параметры таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="667d3-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

