---
title: OpenVisualBasicModule Macro Action
TOCTitle: OpenVisualBasicModule Macro Action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9c57bb28de25ebc540c4e4eb3804a714969e2ac6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482805"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="f13ff-102">OpenVisualBasicModule Macro Action</span><span class="sxs-lookup"><span data-stu-id="f13ff-102">OpenVisualBasicModule Macro Action</span></span>


<span data-ttu-id="f13ff-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f13ff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f13ff-104">Действие **OpenVisualBasicModule** можно использовать для открытия указанного Visual Basic для приложений (VBA) модуля в указанной процедуры.</span><span class="sxs-lookup"><span data-stu-id="f13ff-104">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure.</span></span> <span data-ttu-id="f13ff-105">Это может быть процедуры Sub, Function или процедуру события.</span><span class="sxs-lookup"><span data-stu-id="f13ff-105">This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f13ff-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="f13ff-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="f13ff-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f13ff-108">Setting</span></span>

<span data-ttu-id="f13ff-109">Действие **OpenVisualBasicModule** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="f13ff-109">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f13ff-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="f13ff-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f13ff-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f13ff-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f13ff-112"><strong>Имя модуля</strong></span><span class="sxs-lookup"><span data-stu-id="f13ff-112"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f13ff-113">Имя модуля, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="f13ff-113">The name of the module you want to open.</span></span> <span data-ttu-id="f13ff-114">Этот аргумент можно оставить пустым чтобы поиск всех стандартных модулей в базе данных для процедуры и откройте модуль, соответствующие процедуры во.</span><span class="sxs-lookup"><span data-stu-id="f13ff-114">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="f13ff-115">Если макрос, содержащий действие <strong>OpenVisualBasicModule</strong> в базе данных библиотеки, Microsoft Access сначала выполняет поиск модуля с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="f13ff-115">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f13ff-116"><strong>Имя процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="f13ff-116"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f13ff-117">Имя процедуры, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="f13ff-117">The name of the procedure you want to open the module to.</span></span> <span data-ttu-id="f13ff-118">Если оставить этот аргумент пустым, будет открыт в разделе объявлений.</span><span class="sxs-lookup"><span data-stu-id="f13ff-118">If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="f13ff-119">Необходимо ввести допустимое имя аргумента <STRONG>Имя модуля</STRONG> или <STRONG>Имя процедуры</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="f13ff-119">You must enter a valid name in either the <STRONG>Module Name</STRONG> or <STRONG>Procedure Name</STRONG> argument.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="f13ff-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="f13ff-120">Remarks</span></span>

<span data-ttu-id="f13ff-121">Это действие можно использовать для открытия процедуру события, указав имя **Модуля** и аргумент **Имя процедуры** .</span><span class="sxs-lookup"><span data-stu-id="f13ff-121">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="f13ff-122">Например для открытия процедуру события **нажмите** кнопки в аргументе заказы формы, задайте имя **Модуля** **Form.Orders** и значение аргумента **Имя процедуры** **аргументе\_нажмите кнопку**.</span><span class="sxs-lookup"><span data-stu-id="f13ff-122">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="f13ff-123">Чтобы просмотреть процедуру в форму или отчет, форма или отчет необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="f13ff-123">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="f13ff-124">Аналогично для открытия процедуры в модуле класса, необходимо указать имя модуля, хотя модуль класса не нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="f13ff-124">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="f13ff-125">Чтобы открыть закрытый процедуру, модуль, содержащий его необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="f13ff-125">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="f13ff-126">Это действие имеет тот же эффект, как модуля в области переходов правой кнопкой мыши и выбрав пункт **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="f13ff-126">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**.</span></span> <span data-ttu-id="f13ff-127">Это действие также можно указать имя процедуры и для поиска стандартных модулях в базе данных для процедур.</span><span class="sxs-lookup"><span data-stu-id="f13ff-127">This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>


> [!TIP]
> <P><span data-ttu-id="f13ff-128">Можно выбрать модуль в области навигации и перетащите его в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="f13ff-128">You can select a module in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="f13ff-129">Это автоматически создает <STRONG>OpenVisualBasicModule</STRONG> действие, которое открывается в разделе описаний модуля.</span><span class="sxs-lookup"><span data-stu-id="f13ff-129">This automatically creates an <STRONG>OpenVisualBasicModule</STRONG> action that opens the module to the Declarations section.</span></span></P>



<span data-ttu-id="f13ff-130">Чтобы выполнить действие **OpenVisualBasicModule** в модуле VBA, используйте метод **ОткрытьМодуль** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="f13ff-130">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

