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
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288282"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="84b67-102">Макрокоманда OpenVisualBasicModule</span><span class="sxs-lookup"><span data-stu-id="84b67-102">OpenVisualBasicModule macro action</span></span>

<span data-ttu-id="84b67-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84b67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84b67-104">Вы можете использовать действие **Макрокоманда openvisualbasicmodule** , чтобы открыть указанный модуль Visual Basic для приложений (VBA) в указанной процедуре.</span><span class="sxs-lookup"><span data-stu-id="84b67-104">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure.</span></span> <span data-ttu-id="84b67-105">Это может быть процедура Sub, Function или процедура обработки события.</span><span class="sxs-lookup"><span data-stu-id="84b67-105">This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="84b67-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="84b67-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="84b67-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="84b67-107">Setting</span></span>

<span data-ttu-id="84b67-108">Макрокоманда **Макрокоманда openvisualbasicmodule** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="84b67-108">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84b67-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="84b67-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="84b67-110">Описание</span><span class="sxs-lookup"><span data-stu-id="84b67-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84b67-111"><strong>Имя модуля</strong></span><span class="sxs-lookup"><span data-stu-id="84b67-111"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="84b67-112">Имя модуля, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="84b67-112">The name of the module you want to open.</span></span> <span data-ttu-id="84b67-113">Если требуется выполнить поиск по всем стандартным модулям в базе данных для процедуры и открыть соответствующий модуль в этой процедуре, можно оставить этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="84b67-113">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="84b67-114">При запуске макроса, содержащего действие <strong>Макрокоманда openvisualbasicmodule</strong> , в библиотечной базе данных Microsoft Access сначала ищет модуль с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="84b67-114">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84b67-115"><strong>Имя процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="84b67-115"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="84b67-116">Имя процедуры, в которую нужно открыть модуль.</span><span class="sxs-lookup"><span data-stu-id="84b67-116">The name of the procedure you want to open the module to.</span></span> <span data-ttu-id="84b67-117">Если оставить этот аргумент пустым, модуль откроется в разделе "объявления".</span><span class="sxs-lookup"><span data-stu-id="84b67-117">If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="84b67-118">Необходимо ввести допустимое имя в аргументе **имя модуля** или **имя процедуры** .</span><span class="sxs-lookup"><span data-stu-id="84b67-118">You must enter a valid name in either the **Module Name** or **Procedure Name** argument.</span></span>


## <a name="remarks"></a><span data-ttu-id="84b67-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="84b67-119">Remarks</span></span>

<span data-ttu-id="84b67-120">С помощью этого действия можно открыть процедуру обработки события, указав аргумент **имени модуля** и аргумент **имени процедуры** .</span><span class="sxs-lookup"><span data-stu-id="84b67-120">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="84b67-121">Например, чтобы открыть процедуру обработки события **Click** кнопки принтинвоице в формах Orders, задайте для аргумента **имя модуля** значение **Form. Orders** и присвойте аргументу **имя процедуры** значение **принтинвоице\_нажмите кнопку**.</span><span class="sxs-lookup"><span data-stu-id="84b67-121">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="84b67-122">Чтобы просмотреть процедуру обработки события для формы или отчета, необходимо открыть форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="84b67-122">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="84b67-123">Аналогично, чтобы открыть процедуру в модуле класса, необходимо указать имя модуля, несмотря на то что модуль класса не обязательно должен быть открыт.</span><span class="sxs-lookup"><span data-stu-id="84b67-123">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="84b67-124">Чтобы открыть частную процедуру, необходимо открыть модуль, содержащий его.</span><span class="sxs-lookup"><span data-stu-id="84b67-124">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="84b67-125">Это действие аналогично щелчку правой кнопкой мыши модуля в области навигации и нажатию кнопки **режим конструктора**.</span><span class="sxs-lookup"><span data-stu-id="84b67-125">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**.</span></span> <span data-ttu-id="84b67-126">Это действие также позволяет указать имя процедуры и выполнить поиск процедур в стандартных модулях базы данных.</span><span class="sxs-lookup"><span data-stu-id="84b67-126">This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>

> [!TIP]
> <span data-ttu-id="84b67-127">Вы можете выбрать модуль в области навигации и перетащить его в строку макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="84b67-127">You can select a module in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="84b67-128">При этом автоматически создается действие **Макрокоманда openvisualbasicmodule** , которое открывает модуль в разделе "объявления".</span><span class="sxs-lookup"><span data-stu-id="84b67-128">This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.</span></span>

<span data-ttu-id="84b67-129">Чтобы выполнить действие **Макрокоманда openvisualbasicmodule** в модуле VBA, используйте метод **опенмодуле** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="84b67-129">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

