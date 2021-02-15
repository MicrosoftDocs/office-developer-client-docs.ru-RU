---
title: Макрокоманда SetProperty
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314576"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="2f206-102">Макрокоманда SetProperty</span><span class="sxs-lookup"><span data-stu-id="2f206-102">SetProperty macro action</span></span>

<span data-ttu-id="2f206-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f206-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f206-104">С помощью действия **SetProperty можно** установить свойство для управления в форме или отчете.</span><span class="sxs-lookup"><span data-stu-id="2f206-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="2f206-105">Setting</span><span class="sxs-lookup"><span data-stu-id="2f206-105">Setting</span></span>

<span data-ttu-id="2f206-106">Действие **SetProperty** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2f206-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f206-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="2f206-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2f206-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2f206-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f206-109">Контрольное имя</span><span class="sxs-lookup"><span data-stu-id="2f206-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="2f206-110">Введите имя поля или управления, для которого необходимо установить значение свойства.</span><span class="sxs-lookup"><span data-stu-id="2f206-110">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="2f206-111">Используйте только имя, а не полный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="2f206-111">Use only the control name, not the full syntax.</span></span> <span data-ttu-id="2f206-112">Оставьте этот аргумент пустым, чтобы установить свойство для текущей формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="2f206-112">Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f206-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="2f206-113">Property</span></span></p></td>
<td><p><span data-ttu-id="2f206-114">Выберите свойство, которое нужно установить.</span><span class="sxs-lookup"><span data-stu-id="2f206-114">Select the property that you want to set.</span></span> <span data-ttu-id="2f206-115">Список <strong>свойств,</strong> которые можно настроить с помощью этого действия, см. в разделе "Примечаний" этой статьи.</span><span class="sxs-lookup"><span data-stu-id="2f206-115">See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f206-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2f206-116">Value</span></span></p></td>
<td><p><span data-ttu-id="2f206-117">Введите значение, которое должно быть установлено для свойства.</span><span class="sxs-lookup"><span data-stu-id="2f206-117">Type the value that the property is to be set to.</span></span> <span data-ttu-id="2f206-118">Для свойств со значениями "Да" или "Нет" используйте <strong>-1</strong> для "Да" и <strong>0</strong> для "Нет".</span><span class="sxs-lookup"><span data-stu-id="2f206-118">For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2f206-119">Заметки</span><span class="sxs-lookup"><span data-stu-id="2f206-119">Remarks</span></span>

- <span data-ttu-id="2f206-120">С помощью действия **SetProperty** можно настроить следующие свойства управления: **Enabled,** **Visible,** **Locked,** **Left,** **Top,** **Width,** **Height,** **Fore Color,** **Back Color** или **Caption**.</span><span class="sxs-lookup"><span data-stu-id="2f206-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="2f206-121">Если ввести недопустимое значение для аргумента ***Value,*** ошибка не возникает, но Access может изменить свойство на другое значение в зависимости от того, как он интерпретирует аргумент.</span><span class="sxs-lookup"><span data-stu-id="2f206-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="2f206-122">Действие **SetProperty** в отдельном макросе можно использовать только в том случае, если перед ним установлено действие, которое выбирает форму или отчет, содержащий объект управления, для которого задается свойство.</span><span class="sxs-lookup"><span data-stu-id="2f206-122">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property.</span></span> <span data-ttu-id="2f206-123">Если форма или отчет не открыты, вы можете открыть и выбрать действие **OpenForm** или **OpenReport.**</span><span class="sxs-lookup"><span data-stu-id="2f206-123">If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it.</span></span> <span data-ttu-id="2f206-124">Если форма или отчет уже открыты, вы можете выбрать ее с помощью действия **SelectObject.**</span><span class="sxs-lookup"><span data-stu-id="2f206-124">If the form or report is already open, you can use the **SelectObject** action to select it.</span></span> <span data-ttu-id="2f206-125">Затем можно использовать действие **SetProperty,** чтобы установить свойство.</span><span class="sxs-lookup"><span data-stu-id="2f206-125">You can then use the **SetProperty** action to set the property.</span></span> <span data-ttu-id="2f206-126">Выбор объекта не требуется, если вы используете действие **SetProperty** в макросе, внедренном в элемент управления в той же форме или отчете, что и элемент управления, для которого вы устанавливаете свойство.</span><span class="sxs-lookup"><span data-stu-id="2f206-126">Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="2f206-127">Чтобы запустить действие **SetProperty** в модуле VBA, используйте метод **SetProperty** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="2f206-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="2f206-128">Пример</span><span class="sxs-lookup"><span data-stu-id="2f206-128">Example</span></span>

<span data-ttu-id="2f206-129">В следующем примере показано, как использовать действие SetProperty для перестройки видимости текстового окна **MyTextBox.**</span><span class="sxs-lookup"><span data-stu-id="2f206-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="2f206-130">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2f206-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
