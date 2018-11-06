---
title: Макрокоманда OpenVisualBasicModule
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 274ec88483066b4e8dd4032501ecfcc6a662b134
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998142"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="754c7-102">Макрокоманда OpenVisualBasicModule</span><span class="sxs-lookup"><span data-stu-id="754c7-102">OpenVisualBasicModule macro action</span></span>

<span data-ttu-id="754c7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="754c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="754c7-104">Действие **OpenVisualBasicModule** можно использовать для открытия указанного Visual Basic для приложений (VBA) модуля в указанной процедуры.</span><span class="sxs-lookup"><span data-stu-id="754c7-104">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure.</span></span> <span data-ttu-id="754c7-105">Это может быть процедуры Sub, Function или процедуру события.</span><span class="sxs-lookup"><span data-stu-id="754c7-105">This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="754c7-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="754c7-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="754c7-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="754c7-107">Setting</span></span>

<span data-ttu-id="754c7-108">Действие **OpenVisualBasicModule** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="754c7-108">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="754c7-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="754c7-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="754c7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="754c7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="754c7-111"><strong>Имя модуля</strong></span><span class="sxs-lookup"><span data-stu-id="754c7-111"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="754c7-112">Имя модуля, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="754c7-112">The name of the module you want to open.</span></span> <span data-ttu-id="754c7-113">Этот аргумент можно оставить пустым чтобы поиск всех стандартных модулей в базе данных для процедуры и откройте модуль, соответствующие процедуры во.</span><span class="sxs-lookup"><span data-stu-id="754c7-113">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="754c7-114">Если макрос, содержащий действие <strong>OpenVisualBasicModule</strong> в базе данных библиотеки, Microsoft Access сначала выполняет поиск модуля с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="754c7-114">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754c7-115"><strong>Имя процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="754c7-115"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="754c7-116">Имя процедуры, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="754c7-116">The name of the procedure you want to open the module to.</span></span> <span data-ttu-id="754c7-117">Если оставить этот аргумент пустым, будет открыт в разделе объявлений.</span><span class="sxs-lookup"><span data-stu-id="754c7-117">If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="754c7-118">Необходимо ввести допустимое имя аргумента **Имя модуля** или **Имя процедуры** .</span><span class="sxs-lookup"><span data-stu-id="754c7-118">You must enter a valid name in either the **Module Name** or **Procedure Name** argument.</span></span>


## <a name="remarks"></a><span data-ttu-id="754c7-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="754c7-119">Remarks</span></span>

<span data-ttu-id="754c7-120">Это действие можно использовать для открытия процедуру события, указав имя **Модуля** и аргумент **Имя процедуры** .</span><span class="sxs-lookup"><span data-stu-id="754c7-120">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="754c7-121">Например для открытия процедуру события **нажмите** кнопки в аргументе заказы формы, задайте имя **Модуля** **Form.Orders** и значение аргумента **Имя процедуры** **аргументе\_нажмите кнопку**.</span><span class="sxs-lookup"><span data-stu-id="754c7-121">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="754c7-122">Чтобы просмотреть процедуру в форму или отчет, форма или отчет необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="754c7-122">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="754c7-123">Аналогично для открытия процедуры в модуле класса, необходимо указать имя модуля, хотя модуль класса не нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="754c7-123">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="754c7-124">Чтобы открыть закрытый процедуру, модуль, содержащий его необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="754c7-124">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="754c7-125">Это действие имеет тот же эффект, как модуля в области переходов правой кнопкой мыши и выбрав пункт **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="754c7-125">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**.</span></span> <span data-ttu-id="754c7-126">Это действие также можно указать имя процедуры и для поиска стандартных модулях в базе данных для процедур.</span><span class="sxs-lookup"><span data-stu-id="754c7-126">This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>

> [!TIP]
> <span data-ttu-id="754c7-127">Можно выбрать модуль в области навигации и перетащите его в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="754c7-127">You can select a module in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="754c7-128">Это автоматически создает **OpenVisualBasicModule** действие, которое открывается в разделе описаний модуля.</span><span class="sxs-lookup"><span data-stu-id="754c7-128">This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.</span></span>

<span data-ttu-id="754c7-129">Чтобы выполнить действие **OpenVisualBasicModule** в модуле VBA, используйте метод **ОткрытьМодуль** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="754c7-129">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

