---
title: Действия макроса RemoveAllTempVars
TOCTitle: RemoveAllTempVars Macro Action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 49b92f90fb26ea1f7ad5f0878a7479267b35bdaf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870795"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="0b501-102">Действия макроса RemoveAllTempVars</span><span class="sxs-lookup"><span data-stu-id="0b501-102">RemoveAllTempVars Macro Action</span></span>


<span data-ttu-id="0b501-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b501-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0b501-104">Чтобы удалить все временные переменные, которые созданы с помощью действия **SetTempVar** можно использовать действие **RemoveAllTempVars** .</span><span class="sxs-lookup"><span data-stu-id="0b501-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="0b501-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="0b501-105">Setting</span></span>

<span data-ttu-id="0b501-106">Действие **RemoveAllTempVars** не имеет каких-либо аргументов.</span><span class="sxs-lookup"><span data-stu-id="0b501-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b501-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="0b501-107">Remarks</span></span>

  - <span data-ttu-id="0b501-108">Может быть длиной до 255 временные переменные, определенные за один раз.</span><span class="sxs-lookup"><span data-stu-id="0b501-108">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="0b501-109">Если вы не удалите временную переменную, остается в памяти до закрытия базы данных или проекта.</span><span class="sxs-lookup"><span data-stu-id="0b501-109">If you do not remove a temporary variable, it will remain in memory until you close the database or project.</span></span> <span data-ttu-id="0b501-110">Рекомендуется удалить временные переменные после завершения их использования.</span><span class="sxs-lookup"><span data-stu-id="0b501-110">It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="0b501-111">Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.</span><span class="sxs-lookup"><span data-stu-id="0b501-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="0b501-112">Чтобы удалить одного временную переменную, используйте действие **RemoveTempVar** и установите аргумента имя временную переменную, которые вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="0b501-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="0b501-113">Чтобы выполнить действие **RemoveAllTempVars** в модуле VBA, используйте метод **RemoveAll** объекта **в TempVar** .</span><span class="sxs-lookup"><span data-stu-id="0b501-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="0b501-114">Пример</span><span class="sxs-lookup"><span data-stu-id="0b501-114">Example</span></span>

<span data-ttu-id="0b501-115">Следующий макрос показано, как создать временную переменную, используйте в окне сообщения и условия и затем удалить временную переменную с помощью действия **RemoveAllTempVars** .</span><span class="sxs-lookup"><span data-stu-id="0b501-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b501-116">Condition</span><span class="sxs-lookup"><span data-stu-id="0b501-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="0b501-117">Действие</span><span class="sxs-lookup"><span data-stu-id="0b501-117">Action</span></span></p></th>
<th><p><span data-ttu-id="0b501-118">Аргументы</span><span class="sxs-lookup"><span data-stu-id="0b501-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0b501-119"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="0b501-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="0b501-120"><strong>Имя</strong>: MyVar<strong>выражение</strong>: InputBox (&quot;введите ненулевое число.&quot;)</span><span class="sxs-lookup"><span data-stu-id="0b501-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b501-121">[В TempVar]! [MyVar] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="0b501-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="0b501-122"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="0b501-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="0b501-123"><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [в TempVar]! [MyVar] &amp; &quot;. &quot; <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>сведения</strong></span><span class="sxs-lookup"><span data-stu-id="0b501-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0b501-124"><strong>RemoveAllTempVars</strong></span><span class="sxs-lookup"><span data-stu-id="0b501-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

