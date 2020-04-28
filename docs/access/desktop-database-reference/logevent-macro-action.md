---
title: Макрокоманда LogEvent
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4106e66074975f08a5058aafbfc0c6deac156277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289838"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="c5a02-102">Макрокоманда LogEvent</span><span class="sxs-lookup"><span data-stu-id="c5a02-102">LogEvent macro action</span></span>

<span data-ttu-id="c5a02-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5a02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5a02-104">Действие **ложевент** записывает сведения в системную таблицу **усисаппликатионлог** .</span><span class="sxs-lookup"><span data-stu-id="c5a02-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>

> [!NOTE]
> <span data-ttu-id="c5a02-105">Действие **ложевент** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="c5a02-105">The **LogEvent** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="c5a02-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="c5a02-106">Setting</span></span>

<span data-ttu-id="c5a02-107">Макрокоманда **ложевент** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="c5a02-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5a02-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="c5a02-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="c5a02-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c5a02-109">Required</span></span></p></th>
<th><p><span data-ttu-id="c5a02-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c5a02-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5a02-111"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="c5a02-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a02-112">Нет</span><span class="sxs-lookup"><span data-stu-id="c5a02-112">No</span></span></p></td>
<td><p><span data-ttu-id="c5a02-113">Строковое выражение, описывающее условие, которое необходимо заносить в журнал.</span><span class="sxs-lookup"><span data-stu-id="c5a02-113">A string expression that describes the condition that you want to log.</span></span> <span data-ttu-id="c5a02-114">Длина описания не может превышать 255 символов.</span><span class="sxs-lookup"><span data-stu-id="c5a02-114">The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="c5a02-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5a02-115">Remarks</span></span>

<span data-ttu-id="c5a02-116">Действие **ложевент** можно использовать для записи сведений о состоянии в системную таблицу **усисаппликатионлог** , которые не могут использовать действие **[раисиррор](raiseerror-macro-action.md)** для генерации ошибки.</span><span class="sxs-lookup"><span data-stu-id="c5a02-116">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error.</span></span> <span data-ttu-id="c5a02-117">Например, вы можете записать изменения в определенном поле или использовать элементы, записанные в **усисаппликатионлог** , чтобы помочь вам в отладке макроса.</span><span class="sxs-lookup"><span data-stu-id="c5a02-117">For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="c5a02-118">При использовании действия **ложевент** для записи в таблицу **Усисаппликатионлог** для столбца **Category** автоматически устанавливается значение **User**.</span><span class="sxs-lookup"><span data-stu-id="c5a02-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="c5a02-119">Чтобы просмотреть таблицу **усисаппликатионлог** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c5a02-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="c5a02-120">Откройте меню **файл** и выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c5a02-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="c5a02-121">В диалоговом окне **Параметры Access** перейдите на вкладку **Текущая база данных** .</span><span class="sxs-lookup"><span data-stu-id="c5a02-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="c5a02-122">В разделе **Навигация** щелкните **Параметры навигации**.</span><span class="sxs-lookup"><span data-stu-id="c5a02-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="c5a02-123">В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c5a02-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="c5a02-124">Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно **Параметры Access** .</span><span class="sxs-lookup"><span data-stu-id="c5a02-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

