---
title: Набор форм, отчетов и свойств элемента управления
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480947"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="bc739-102">Набор форм, отчетов и свойств элемента управления</span><span class="sxs-lookup"><span data-stu-id="bc739-102">Set form, report, and control properties</span></span>

<span data-ttu-id="bc739-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc739-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bc739-104">Каждой формы, отчета, раздела и элемента управления имеются свойства, которые можно изменить, чтобы изменить внешний вид и характеристики этого элемента.</span><span class="sxs-lookup"><span data-stu-id="bc739-104">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item.</span></span> <span data-ttu-id="bc739-105">Просмотр и изменение свойств с помощью свойств, макрос или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bc739-105">You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="bc739-106">Настройка параметров</span><span class="sxs-lookup"><span data-stu-id="bc739-106">Set properties</span></span>

1. <span data-ttu-id="bc739-107">В режиме конструктора формы или в режиме конструктора отчета выберите элемент управления, раздел, форму или отчет, для которого требуется задать свойство.</span><span class="sxs-lookup"><span data-stu-id="bc739-107">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property.</span></span> <span data-ttu-id="bc739-108">Можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="bc739-108">You can select:</span></span>
    
   - <span data-ttu-id="bc739-109">Один или несколько элементов управления.</span><span class="sxs-lookup"><span data-stu-id="bc739-109">One or more controls.</span></span> <span data-ttu-id="bc739-110">Чтобы выбрать несколько элементов управления, нажмите и удерживайте клавишу SHIFT и щелкните элементы управления или перетащите указатель мыши на элементы управления, которые требуется выбрать.</span><span class="sxs-lookup"><span data-stu-id="bc739-110">To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="bc739-111">При выборе нескольких элементов управления в окне свойств отображаются только те свойства, общие для выделенных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="bc739-111">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="bc739-112">Один раздел.</span><span class="sxs-lookup"><span data-stu-id="bc739-112">One section.</span></span> <span data-ttu-id="bc739-113">Щелкните область выделения раздела раздела, который требуется выбрать.</span><span class="sxs-lookup"><span data-stu-id="bc739-113">Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="bc739-114">Вся форма или отчет.</span><span class="sxs-lookup"><span data-stu-id="bc739-114">The entire form or report.</span></span> <span data-ttu-id="bc739-115">Щелкните область выделения формы или область выделения отчета в левом верхнем углу форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="bc739-115">Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="bc739-116">Откройте окно свойств, щелкнув правой кнопкой мыши объект или раздел и выберите команду **Свойства** в контекстном меню или нажмите кнопку **Свойства** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="bc739-116">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="bc739-117">Выберите свойство, для которого требуется задать значение и затем выполните одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="bc739-117">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="bc739-118">В поле свойства введите соответствующее значение или выражение.</span><span class="sxs-lookup"><span data-stu-id="bc739-118">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="bc739-119">Если в диалоговом окне Свойства стрелки, щелкните стрелку и выберите значение в списке.</span><span class="sxs-lookup"><span data-stu-id="bc739-119">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="bc739-120">Если кнопка **Построить** отображается справа от поля свойства, щелкните его для отображения в построитель или для отображения диалогового окна со списком сборщиков систем.</span><span class="sxs-lookup"><span data-stu-id="bc739-120">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="bc739-121">К примеру можно использовать построитель программ, построитель макросов или построитель запросов для настройки некоторых свойств.</span><span class="sxs-lookup"><span data-stu-id="bc739-121">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="bc739-122">Советы </span><span class="sxs-lookup"><span data-stu-id="bc739-122">Tips</span></span>

- <span data-ttu-id="bc739-123">Microsoft Access поле **Показать** ввода и просмотр выражений или длинных значений.</span><span class="sxs-lookup"><span data-stu-id="bc739-123">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="bc739-124">Для отображения окна **инструмента** , щелкните поле свойства в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="bc739-124">To display the **Zoom** box, click a property box in the property sheet.</span></span> <span data-ttu-id="bc739-125">Нажмите клавиши SHIFT + F2 или щелкните правой кнопкой мыши и нажмите кнопку **Показать** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="bc739-125">Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="bc739-126">Свойства **ControlSource** для некоторых элементов управления, введя значение свойства непосредственно в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="bc739-126">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="bc739-127">Можно изменить параметры свойств по умолчанию для типа элемента управления, чтобы будущих элементов управления, создаваемых будут иметь значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc739-127">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="bc739-128">Значения свойств связанного элемента управления может не соответствовать соответствующие параметры в поле базовой таблицы или запроса, с которым связан элемент управления.</span><span class="sxs-lookup"><span data-stu-id="bc739-128">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="bc739-129">Если параметры не совпадают, параметры формы или отчета обычно имеют приоритет над таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="bc739-129">If the settings are different, the form or report settings typically override those in the table or query.</span></span> <span data-ttu-id="bc739-130">Дополнительные сведения о как свойства наследуются видеть связь свойств элементов управления со свойствами полей базы данных.</span><span class="sxs-lookup"><span data-stu-id="bc739-130">For more information about how properties are inherited, see How control properties relate to properties in their underlying fields.</span></span>

