---
title: Макрокоманда RemoveTempVar
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5051cfd74f2a745ee430f2ed8a20445d2f9965f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306757"
---
# <a name="removetempvar-macro-action"></a><span data-ttu-id="69b41-102">Макрокоманда RemoveTempVar</span><span class="sxs-lookup"><span data-stu-id="69b41-102">RemoveTempVar macro action</span></span>


<span data-ttu-id="69b41-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69b41-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="69b41-104">Вы можете использовать действие **Макрокоманда removetempvar** для удаления одной временной переменной, созданной с помощью действия **Макрокоманда SetTempVar** .</span><span class="sxs-lookup"><span data-stu-id="69b41-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="69b41-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="69b41-105">Setting</span></span>

<span data-ttu-id="69b41-106">Действие **Макрокоманда removetempvar** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="69b41-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69b41-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="69b41-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="69b41-108">Описание</span><span class="sxs-lookup"><span data-stu-id="69b41-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69b41-109"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="69b41-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="69b41-110">Введите имя временной переменной, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="69b41-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="69b41-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="69b41-111">Remarks</span></span>

  - <span data-ttu-id="69b41-112">Одновременно может быть определено до 255 временных переменных.</span><span class="sxs-lookup"><span data-stu-id="69b41-112">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="69b41-113">Если не удалить временную переменную, она останется в памяти до тех пор, пока не будет закрыта база данных.</span><span class="sxs-lookup"><span data-stu-id="69b41-113">If you do not remove a temporary variable, it will remain in memory until you close the database.</span></span> <span data-ttu-id="69b41-114">Рекомендуется удалять временные переменные после завершения их использования.</span><span class="sxs-lookup"><span data-stu-id="69b41-114">It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="69b41-115">Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.</span><span class="sxs-lookup"><span data-stu-id="69b41-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="69b41-116">Если вы неправильно задаете имя удаляемой переменной, Access не отобразит сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="69b41-116">If you misspell the name of the variable to be removed, Access does not display an error.</span></span> <span data-ttu-id="69b41-117">Переменная, которую вы хотите удалить, остается в памяти до закрытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="69b41-117">The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="69b41-118">Если вы создали более одной временной переменной и хотите удалить их все сразу, используйте действие **Макрокоманда removealltempvars** .</span><span class="sxs-lookup"><span data-stu-id="69b41-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="69b41-119">Чтобы выполнить действие **Макрокоманда removetempvar** в модуле VBA, используйте метод **Remove** объекта **TempVars** .</span><span class="sxs-lookup"><span data-stu-id="69b41-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="69b41-120">Пример</span><span class="sxs-lookup"><span data-stu-id="69b41-120">Example</span></span>

<span data-ttu-id="69b41-121">В следующем макросе показано, как создать временную переменную, использовать ее в условии и окне сообщения, а затем удалить временную переменную с помощью действия **Макрокоманда removetempvar** .</span><span class="sxs-lookup"><span data-stu-id="69b41-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69b41-122">Условие</span><span class="sxs-lookup"><span data-stu-id="69b41-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="69b41-123">Action</span><span class="sxs-lookup"><span data-stu-id="69b41-123">Action</span></span></p></th>
<th><p><span data-ttu-id="69b41-124">Аргументы</span><span class="sxs-lookup"><span data-stu-id="69b41-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="69b41-125"><strong>Макрокоманда SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="69b41-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="69b41-126"><strong>Name</strong>:<strong>выражение</strong>мивар: InputBox (&quot;введите ненулевое значение).&quot;</span><span class="sxs-lookup"><span data-stu-id="69b41-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69b41-127">[TempVars]! [Мивар] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="69b41-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="69b41-128"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="69b41-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="69b41-129"><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [TempVars]! [Мивар] &amp; &quot;. &quot; <strong>Гудок</strong>: <strong>естипе</strong>: <strong>Information</strong></span><span class="sxs-lookup"><span data-stu-id="69b41-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="69b41-130"><strong>Макрокоманда removetempvar</strong></span><span class="sxs-lookup"><span data-stu-id="69b41-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="69b41-131"><strong>Name</strong>: мивар</span><span class="sxs-lookup"><span data-stu-id="69b41-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

