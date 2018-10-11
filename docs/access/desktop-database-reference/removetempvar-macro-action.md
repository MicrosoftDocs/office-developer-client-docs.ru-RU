---
title: RemoveTempVar Macro Action
TOCTitle: RemoveTempVar Macro Action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 61d03f23e0fbe04cae49670366f76c02e81d694a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481972"
---
# <a name="removetempvar-macro-action"></a><span data-ttu-id="4f86a-102">RemoveTempVar Macro Action</span><span class="sxs-lookup"><span data-stu-id="4f86a-102">RemoveTempVar Macro Action</span></span>


<span data-ttu-id="4f86a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f86a-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="4f86a-104">Действие **RemoveTempVar** можно использовать для удаления одного временную переменную, созданный с помощью действия **SetTempVar** .</span><span class="sxs-lookup"><span data-stu-id="4f86a-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="4f86a-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="4f86a-105">Setting</span></span>

<span data-ttu-id="4f86a-106">Действие **RemoveTempVar** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="4f86a-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f86a-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="4f86a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4f86a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4f86a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f86a-109"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="4f86a-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4f86a-110">Введите имя временную переменную, которые вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="4f86a-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4f86a-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f86a-111">Remarks</span></span>

  - <span data-ttu-id="4f86a-112">Может быть длиной до 255 временные переменные, определенные за один раз.</span><span class="sxs-lookup"><span data-stu-id="4f86a-112">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="4f86a-113">Если вы не удалите временную переменную, остается в памяти до закрытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="4f86a-113">If you do not remove a temporary variable, it will remain in memory until you close the database.</span></span> <span data-ttu-id="4f86a-114">Рекомендуется удалить временные переменные после завершения их использования.</span><span class="sxs-lookup"><span data-stu-id="4f86a-114">It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="4f86a-115">Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.</span><span class="sxs-lookup"><span data-stu-id="4f86a-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="4f86a-116">Если неправильно введено имя переменной удаляемых доступа не отображает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4f86a-116">If you misspell the name of the variable to be removed, Access does not display an error.</span></span> <span data-ttu-id="4f86a-117">Переменная, которую вы хотите удалить будет оставаться в памяти до закрытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="4f86a-117">The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="4f86a-118">Если были созданы более одного временную переменную, требуется одновременное удаление используйте действие **RemoveAllTempVars** .</span><span class="sxs-lookup"><span data-stu-id="4f86a-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="4f86a-119">Чтобы выполнить действие **RemoveTempVar** в модуле VBA, используйте метод **Remove** объекта **в TempVar** .</span><span class="sxs-lookup"><span data-stu-id="4f86a-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="4f86a-120">Пример</span><span class="sxs-lookup"><span data-stu-id="4f86a-120">Example</span></span>

<span data-ttu-id="4f86a-121">Следующий макрос показано, как создать временную переменную, используйте в окне сообщения и условия и затем удалить временную переменную с помощью действия **RemoveTempVar** .</span><span class="sxs-lookup"><span data-stu-id="4f86a-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f86a-122">Condition</span><span class="sxs-lookup"><span data-stu-id="4f86a-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="4f86a-123">Действие</span><span class="sxs-lookup"><span data-stu-id="4f86a-123">Action</span></span></p></th>
<th><p><span data-ttu-id="4f86a-124">Аргументы</span><span class="sxs-lookup"><span data-stu-id="4f86a-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="4f86a-125"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="4f86a-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="4f86a-126"><strong>Имя</strong>: MyVar<strong>выражение</strong>: InputBox (&quot;введите ненулевое число.&quot;)</span><span class="sxs-lookup"><span data-stu-id="4f86a-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f86a-127">[В TempVar]! [MyVar] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="4f86a-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="4f86a-128"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="4f86a-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="4f86a-129"><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [в TempVar]! [MyVar] &amp; &quot;. &quot; <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>сведения</strong></span><span class="sxs-lookup"><span data-stu-id="4f86a-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="4f86a-130"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="4f86a-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="4f86a-131"><strong>Имя</strong>: MyVar</span><span class="sxs-lookup"><span data-stu-id="4f86a-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

