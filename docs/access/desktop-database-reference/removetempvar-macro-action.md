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
# <a name="removetempvar-macro-action"></a><span data-ttu-id="b0b1f-102">Макрокоманда RemoveTempVar</span><span class="sxs-lookup"><span data-stu-id="b0b1f-102">RemoveTempVar macro action</span></span>


<span data-ttu-id="b0b1f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0b1f-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="b0b1f-104">С помощью **действия RemoveTempVar** можно удалить одну временную переменную, созданную с помощью **действия SetTempVar.**</span><span class="sxs-lookup"><span data-stu-id="b0b1f-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="b0b1f-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="b0b1f-105">Setting</span></span>

<span data-ttu-id="b0b1f-106">Действие **RemoveTempVar** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b1f-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b0b1f-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b0b1f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b0b1f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0b1f-109"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="b0b1f-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b1f-110">Введите имя временной переменной, которая необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b0b1f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0b1f-111">Remarks</span></span>

  - <span data-ttu-id="b0b1f-112">Одновременно можно определить до 255 временных переменных.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-112">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="b0b1f-113">Если не удалить временную переменную, она останется в памяти до закрытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-113">If you do not remove a temporary variable, it will remain in memory until you close the database.</span></span> <span data-ttu-id="b0b1f-114">Это хорошая практика, чтобы удалить временные переменные, когда вы закончите с их использованием.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-114">It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="b0b1f-115">При закрытии базы данных или проекта доступ автоматически удаляет все временные переменные.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="b0b1f-116">Если вы ошибались с именем удаляемой переменной, access не отображает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-116">If you misspell the name of the variable to be removed, Access does not display an error.</span></span> <span data-ttu-id="b0b1f-117">Переменная, которая необходимо удалить, останется в памяти до закрытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="b0b1f-117">The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="b0b1f-118">Если вы создали несколько временных переменных и хотите удалить их сразу, используйте действие **RemoveAllTempVars.**</span><span class="sxs-lookup"><span data-stu-id="b0b1f-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="b0b1f-119">Чтобы выполнить **действие RemoveTempVar** в модуле VBA, используйте метод **Remove** объекта **TempVars.**</span><span class="sxs-lookup"><span data-stu-id="b0b1f-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="b0b1f-120">Пример</span><span class="sxs-lookup"><span data-stu-id="b0b1f-120">Example</span></span>

<span data-ttu-id="b0b1f-121">На следующем макросе показано, как создать временную переменную, использовать ее в состоянии и поле сообщений, а затем удалить временную переменную с помощью действия **RemoveTempVar.**</span><span class="sxs-lookup"><span data-stu-id="b0b1f-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b1f-122">Условие</span><span class="sxs-lookup"><span data-stu-id="b0b1f-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="b0b1f-123">Action</span><span class="sxs-lookup"><span data-stu-id="b0b1f-123">Action</span></span></p></th>
<th><p><span data-ttu-id="b0b1f-124">Аргументы</span><span class="sxs-lookup"><span data-stu-id="b0b1f-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b0b1f-125"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="b0b1f-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b1f-126"><strong>Имя:</strong>Выражение<strong>MyVar:</strong>InputBox &quot; (Введите номер без нуля. &quot; )</span><span class="sxs-lookup"><span data-stu-id="b0b1f-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b1f-127">[TempVars]! [MyVar] &lt; &gt; 0</span><span class="sxs-lookup"><span data-stu-id="b0b1f-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="b0b1f-128"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b0b1f-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b1f-129"><strong>Сообщение</strong>: = &quot; Вы &quot; &amp; ввели [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Звуковой сигнал:</strong> <strong>YesType</strong>: <strong>Информация</strong></span><span class="sxs-lookup"><span data-stu-id="b0b1f-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b0b1f-130"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="b0b1f-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b1f-131"><strong>Имя:</strong>MyVar</span><span class="sxs-lookup"><span data-stu-id="b0b1f-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

