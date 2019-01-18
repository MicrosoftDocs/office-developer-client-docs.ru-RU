---
title: Установка свойств форм, отчетов и элементов управления
TOCTitle: Set form, report, and control properties
description: Каждой формы, отчета, раздела и элемента управления имеются свойства, которые можно изменить, чтобы изменить внешний вид и характеристики этого элемента в Access 2013.
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701692"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="14ccc-103">Установка свойств форм, отчетов и элементов управления</span><span class="sxs-lookup"><span data-stu-id="14ccc-103">Set form, report, and control properties</span></span>

<span data-ttu-id="14ccc-104">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14ccc-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14ccc-105">Каждой формы, отчета, раздела и элемента управления имеются свойства, которые можно изменить, чтобы изменить внешний вид и характеристики этого элемента.</span><span class="sxs-lookup"><span data-stu-id="14ccc-105">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item.</span></span> <span data-ttu-id="14ccc-106">Просмотр и изменение свойств с помощью свойств, макрос или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="14ccc-106">You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="14ccc-107">Настройка параметров</span><span class="sxs-lookup"><span data-stu-id="14ccc-107">Set properties</span></span>

1. <span data-ttu-id="14ccc-108">В режиме конструктора формы или в режиме конструктора отчета выберите элемент управления, раздел, форму или отчет, для которого требуется задать свойство.</span><span class="sxs-lookup"><span data-stu-id="14ccc-108">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property.</span></span> <span data-ttu-id="14ccc-109">Можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="14ccc-109">You can select:</span></span>
    
   - <span data-ttu-id="14ccc-110">Один или несколько элементов управления.</span><span class="sxs-lookup"><span data-stu-id="14ccc-110">One or more controls.</span></span> <span data-ttu-id="14ccc-111">Чтобы выбрать несколько элементов управления, нажмите и удерживайте клавишу SHIFT и выберите элементы управления или перетащите указатель мыши на элементы управления, которые требуется выбрать.</span><span class="sxs-lookup"><span data-stu-id="14ccc-111">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="14ccc-112">При выборе нескольких элементов управления в окне свойств отображаются только те свойства, общие для выделенных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="14ccc-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="14ccc-113">Один раздел.</span><span class="sxs-lookup"><span data-stu-id="14ccc-113">One section.</span></span> <span data-ttu-id="14ccc-114">Выберите область выделения раздела раздела, который требуется выбрать.</span><span class="sxs-lookup"><span data-stu-id="14ccc-114">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="14ccc-115">Вся форма или отчет.</span><span class="sxs-lookup"><span data-stu-id="14ccc-115">The entire form or report.</span></span> <span data-ttu-id="14ccc-116">Выберите область выделения формы или область выделения отчета в левом верхнем углу форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="14ccc-116">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="14ccc-117">Откройте окно свойств, щелкнув правой кнопкой мыши объект или раздел, а затем выберите **Свойства** в контекстном меню или с помощью **Свойства** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="14ccc-117">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="14ccc-118">Выберите свойство, для которого требуется задать значение и затем выполните одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="14ccc-118">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="14ccc-119">В поле свойства введите соответствующее значение или выражение.</span><span class="sxs-lookup"><span data-stu-id="14ccc-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="14ccc-120">Если в диалоговом окне Свойства стрелки, выберите стрелку и выберите значение в списке.</span><span class="sxs-lookup"><span data-stu-id="14ccc-120">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="14ccc-121">Если кнопка **Построить** отображается справа от поля свойства, выберите его для отображения в построитель или для отображения диалогового окна со списком сборщиков систем.</span><span class="sxs-lookup"><span data-stu-id="14ccc-121">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="14ccc-122">К примеру можно использовать построитель программ, построитель макросов или построитель запросов для настройки некоторых свойств.</span><span class="sxs-lookup"><span data-stu-id="14ccc-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="14ccc-123">Советы </span><span class="sxs-lookup"><span data-stu-id="14ccc-123">Tips</span></span>

- <span data-ttu-id="14ccc-124">Microsoft Access поле **Показать** ввода и просмотр выражений или длинных значений.</span><span class="sxs-lookup"><span data-stu-id="14ccc-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="14ccc-125">Для отображения окна **инструмента** , выберите поле свойства в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="14ccc-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="14ccc-126">Нажмите клавиши SHIFT + F2 или щелкните правой кнопкой мыши и выберите пункт **Показать** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="14ccc-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="14ccc-127">Свойства **ControlSource** для некоторых элементов управления, введя значение свойства непосредственно в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="14ccc-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="14ccc-128">Можно изменить параметры свойств по умолчанию для типа элемента управления, чтобы будущих элементов управления, создаваемых будут иметь значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14ccc-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="14ccc-129">Значения свойств связанного элемента управления может не соответствовать соответствующие параметры в поле базовой таблицы или запроса, с которым связан элемент управления.</span><span class="sxs-lookup"><span data-stu-id="14ccc-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="14ccc-130">Если параметры не совпадают, параметры формы или отчета обычно имеют приоритет над таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="14ccc-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

