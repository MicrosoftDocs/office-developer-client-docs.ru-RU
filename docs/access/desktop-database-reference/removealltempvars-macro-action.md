---
title: Макрокоманда RemoveAllTempVars
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306799"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="bd2c3-102">Макрокоманда RemoveAllTempVars</span><span class="sxs-lookup"><span data-stu-id="bd2c3-102">RemoveAllTempVars macro action</span></span>


<span data-ttu-id="bd2c3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd2c3-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bd2c3-104">Вы можете использовать действие **Макрокоманда removealltempvars** , чтобы удалить все временные переменные, созданные с помощью действия **Макрокоманда SetTempVar** .</span><span class="sxs-lookup"><span data-stu-id="bd2c3-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="bd2c3-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="bd2c3-105">Setting</span></span>

<span data-ttu-id="bd2c3-106">Действие **Макрокоманда removealltempvars** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="bd2c3-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd2c3-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd2c3-107">Remarks</span></span>

  - <span data-ttu-id="bd2c3-108">Одновременно может быть определено до 255 временных переменных.</span><span class="sxs-lookup"><span data-stu-id="bd2c3-108">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="bd2c3-109">Если не удалить временную переменную, она останется в памяти до тех пор, пока не будет закрыта база данных или проект.</span><span class="sxs-lookup"><span data-stu-id="bd2c3-109">If you do not remove a temporary variable, it will remain in memory until you close the database or project.</span></span> <span data-ttu-id="bd2c3-110">Рекомендуется удалять временные переменные после завершения их использования.</span><span class="sxs-lookup"><span data-stu-id="bd2c3-110">It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="bd2c3-111">Access автоматически удаляет все временные переменные при закрытии базы данных или проекта.</span><span class="sxs-lookup"><span data-stu-id="bd2c3-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="bd2c3-112">Чтобы удалить одну временную переменную, используйте действие **Макрокоманда removetempvar** и задайте для аргумента имя удаляемой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="bd2c3-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="bd2c3-113">Чтобы выполнить действие **Макрокоманда removealltempvars** в модуле VBA, используйте метод **RemoveAll** объекта **TempVars** .</span><span class="sxs-lookup"><span data-stu-id="bd2c3-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="bd2c3-114">Пример</span><span class="sxs-lookup"><span data-stu-id="bd2c3-114">Example</span></span>

<span data-ttu-id="bd2c3-115">В следующем макросе показано, как создать временную переменную, использовать ее в условии и окне сообщения, а затем удалить временную переменную с помощью действия **Макрокоманда removealltempvars** .</span><span class="sxs-lookup"><span data-stu-id="bd2c3-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd2c3-116">Условие</span><span class="sxs-lookup"><span data-stu-id="bd2c3-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="bd2c3-117">Action</span><span class="sxs-lookup"><span data-stu-id="bd2c3-117">Action</span></span></p></th>
<th><p><span data-ttu-id="bd2c3-118">Аргументы</span><span class="sxs-lookup"><span data-stu-id="bd2c3-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="bd2c3-119"><strong>Макрокоманда SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="bd2c3-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="bd2c3-120"><strong>Name</strong>:<strong>выражение</strong>мивар: InputBox (&quot;введите ненулевое значение).&quot;</span><span class="sxs-lookup"><span data-stu-id="bd2c3-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd2c3-121">[TempVars]! [Мивар] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="bd2c3-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="bd2c3-122"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="bd2c3-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="bd2c3-123"><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [TempVars]! [Мивар] &amp; &quot;. &quot; <strong>Гудок</strong>: <strong>естипе</strong>: <strong>Information</strong></span><span class="sxs-lookup"><span data-stu-id="bd2c3-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="bd2c3-124"><strong>Макрокоманда removealltempvars</strong></span><span class="sxs-lookup"><span data-stu-id="bd2c3-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

