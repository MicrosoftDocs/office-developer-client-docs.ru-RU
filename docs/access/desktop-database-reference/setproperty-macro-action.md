---
title: Действия SetProperty макроса
TOCTitle: SetProperty Macro Action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ac0cb0fe608ad5f3e15ae72346eac30628ba3dfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887385"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="fab61-102">Действия SetProperty макроса</span><span class="sxs-lookup"><span data-stu-id="fab61-102">SetProperty Macro Action</span></span>

<span data-ttu-id="fab61-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fab61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fab61-104">Действия **SetProperty** можно использовать для задания свойства для элемента управления в форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="fab61-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="fab61-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="fab61-105">Setting</span></span>

<span data-ttu-id="fab61-106">Действия **SetProperty** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="fab61-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fab61-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="fab61-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fab61-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fab61-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fab61-109">Контрольное имя</span><span class="sxs-lookup"><span data-stu-id="fab61-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="fab61-110">Введите имя в поле или элемент управления, для которого требуется задать значение свойства.</span><span class="sxs-lookup"><span data-stu-id="fab61-110">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="fab61-111">Используйте только имя элемента управления, но не полный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="fab61-111">Use only the control name, not the full syntax.</span></span> <span data-ttu-id="fab61-112">Оставьте данный аргумент пустым, чтобы задать свойства для текущей формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="fab61-112">Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fab61-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="fab61-113">Property</span></span></p></td>
<td><p><span data-ttu-id="fab61-114">Выберите свойство, которое требуется установить.</span><span class="sxs-lookup"><span data-stu-id="fab61-114">Select the property that you want to set.</span></span> <span data-ttu-id="fab61-115"><strong>В этой статье представлен список свойств, которые можно настроить с помощью этого действия см.</strong></span><span class="sxs-lookup"><span data-stu-id="fab61-115">See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fab61-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fab61-116">Value</span></span></p></td>
<td><p><span data-ttu-id="fab61-117">Введите значение, является ли данное свойство должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="fab61-117">Type the value that the property is to be set to.</span></span> <span data-ttu-id="fab61-118">Для свойства, значения которых являются Да или нет, используйте <strong>значение -1</strong> для Да и <strong>0</strong> для нет.</span><span class="sxs-lookup"><span data-stu-id="fab61-118">For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fab61-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="fab61-119">Remarks</span></span>

- <span data-ttu-id="fab61-120">Действия **SetProperty** можно использовать для настройки следующих свойств элемента управления: **включено**, **Visible**, **блокируется**, **слева**, **в начало**, **Ширина**, **Высота**, **цвет текста**, **Цвет фона**, или **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="fab61-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="fab61-121">При вводе недопустимое значение аргумента ***значение*** ошибок нет, но доступа могут изменить свойство разные значения, в зависимости от того, как оно интерпретирует аргумент.</span><span class="sxs-lookup"><span data-stu-id="fab61-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="fab61-122">Действие **SetProperty** в изолированном макрос можно использовать только в том случае, если вы поставьте перед ним действие, которое выбирает форму или отчет, содержащий элемент управления, для которого задаются свойства.</span><span class="sxs-lookup"><span data-stu-id="fab61-122">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property.</span></span> <span data-ttu-id="fab61-123">Если форма или отчет не открыт, можно использовать действие **ОткрытьФорму** или **ОткрытьОтчет** открыть и затем выберите ее.</span><span class="sxs-lookup"><span data-stu-id="fab61-123">If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it.</span></span> <span data-ttu-id="fab61-124">Если форма или отчет уже открыт, чтобы выбрать его можно использовать **ВыделитьОбъект** .</span><span class="sxs-lookup"><span data-stu-id="fab61-124">If the form or report is already open, you can use the **SelectObject** action to select it.</span></span> <span data-ttu-id="fab61-125">Затем можно использовать действие **SetProperty** для свойства.</span><span class="sxs-lookup"><span data-stu-id="fab61-125">You can then use the **SetProperty** action to set the property.</span></span> <span data-ttu-id="fab61-126">Выберите объект не является обязательным, если вы используете действие **SetProperty** в макросе, который встроен в элемент управления на одну форму или отчет в качестве элемента управления, для которого задаются свойства.</span><span class="sxs-lookup"><span data-stu-id="fab61-126">Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="fab61-127">Чтобы выполнить действия **SetProperty** в модуле VBA, используйте метод **SetProperty** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="fab61-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="fab61-128">Пример</span><span class="sxs-lookup"><span data-stu-id="fab61-128">Example</span></span>

<span data-ttu-id="fab61-129">Следующий пример демонстрирует действие SetProperty используется для включения и отключения видимости **MyTextBox** текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="fab61-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="fab61-130">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="fab61-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
