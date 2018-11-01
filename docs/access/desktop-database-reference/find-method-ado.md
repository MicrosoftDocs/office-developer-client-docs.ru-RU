---
title: Найти метод - ActiveX Data Objects (ADO)
TOCTitle: Find Method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929e4ac695ff65c3576f2ffb8ad1baf8ab1d1137
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870627"
---
# <a name="find-method-ado"></a><span data-ttu-id="24271-102">Найти метод (ADO)</span><span class="sxs-lookup"><span data-stu-id="24271-102">Find Method (ADO)</span></span>


<span data-ttu-id="24271-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24271-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="24271-104">Выполняет поиск [записей](recordset-object-ado.md) для строки, которая должна удовлетворять определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="24271-104">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria.</span></span> <span data-ttu-id="24271-105">Кроме того можно указать направление поиска, начальную строку и смещением от начала строки.</span><span class="sxs-lookup"><span data-stu-id="24271-105">Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</span></span> <span data-ttu-id="24271-106">Если соблюдаются условия, текущей позиции строки имеет значение обнаруженного записи; в противном случае положение задано значение end (или Пуск) **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="24271-106">If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="24271-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24271-107">Syntax</span></span>

<span data-ttu-id="24271-108">Поиск (*критерии*, *SkipRows*, *SearchDirection*, *запустите*)</span><span class="sxs-lookup"><span data-stu-id="24271-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="24271-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="24271-109">Parameters</span></span>

  - <span data-ttu-id="24271-110">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="24271-110">*Criteria*</span></span>

  - <span data-ttu-id="24271-111">**Строковое** значение, содержащее оператор, указав имя столбца, оператор сравнения и значение для использования в поиск.</span><span class="sxs-lookup"><span data-stu-id="24271-111">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>

  - <span data-ttu-id="24271-112">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="24271-112">*SkipRows*</span></span>

  - <span data-ttu-id="24271-113">Необязательные *.*</span><span class="sxs-lookup"><span data-stu-id="24271-113">Optional *.*</span></span> <span data-ttu-id="24271-114">**Длинное целое** значение, значение которого по умолчанию равно нулю, указывающее смещение из текущей строки или *запустите* закладку, чтобы начать поиск.</span><span class="sxs-lookup"><span data-stu-id="24271-114">A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search.</span></span> <span data-ttu-id="24271-115">По умолчанию поиск начнется в текущей строке.</span><span class="sxs-lookup"><span data-stu-id="24271-115">By default, the search will start on the current row.</span></span>

  - <span data-ttu-id="24271-116">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="24271-116">*SearchDirection*</span></span>

  - <span data-ttu-id="24271-117">Необязательные *.*</span><span class="sxs-lookup"><span data-stu-id="24271-117">Optional *.*</span></span> <span data-ttu-id="24271-118">[SearchDirectionEnum](searchdirectionenum.md) значение, указывающее, является ли начало поиска на текущей строке или следующей доступной строки в направление поиска.</span><span class="sxs-lookup"><span data-stu-id="24271-118">A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search.</span></span> <span data-ttu-id="24271-119">Если значение равно **adSearchForward**неуспешных поиска останавливается в конце **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="24271-119">An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**.</span></span> <span data-ttu-id="24271-120">Если значение равно **adSearchBackward**неуспешных поиска останавливается в начале **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="24271-120">An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>

  - <span data-ttu-id="24271-121">*Start*</span><span class="sxs-lookup"><span data-stu-id="24271-121">*Start*</span></span>

  - <span data-ttu-id="24271-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="24271-122">Optional.</span></span> <span data-ttu-id="24271-123">Закладка **Variant** , который работает как позицию для поиска.</span><span class="sxs-lookup"><span data-stu-id="24271-123">A **Variant** bookmark that functions as the starting position for the search.</span></span>

## <a name="remarks"></a><span data-ttu-id="24271-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="24271-124">Remarks</span></span>

<span data-ttu-id="24271-125">Может быть указано только имя одного столбца в *условия*.</span><span class="sxs-lookup"><span data-stu-id="24271-125">Only a single-column name may be specified in *criteria*.</span></span> <span data-ttu-id="24271-126">Этот метод не поддерживает поиска по нескольким столбцам.</span><span class="sxs-lookup"><span data-stu-id="24271-126">This method does not support multi-column searches.</span></span>

<span data-ttu-id="24271-127">Оператор сравнения в *условия* может быть "**\>**«(больше),»**\<**«(меньше), «=» (равно),»\>=» (больше или равно),"\<=» (меньше или равно), "\<\>" (не равно) или «как и» (подстановочные знаки).</span><span class="sxs-lookup"><span data-stu-id="24271-127">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="24271-128">Значение в *условия* может быть string, число с плавающей запятой или дата.</span><span class="sxs-lookup"><span data-stu-id="24271-128">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="24271-129">Строковые значения разделяются одинарные кавычки или "\#" (знак) помечает (, например «состояние = «Вашингтон»» или «состояние = \#WA\#«).</span><span class="sxs-lookup"><span data-stu-id="24271-129">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="24271-130">Значения дат разделяются "\#" (знак) помечает (, например «запустить\_Дата \> \#7/22/97\#«) и может содержать часов, минут и секунд, чтобы указать, метки времени, но не должен содержать миллисекундах или возникают ошибки .</span><span class="sxs-lookup"><span data-stu-id="24271-130">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="24271-131">Если оператор сравнения «как», строковое значение может содержать символ звездочки (\*) для поиска одного или нескольких экземпляров любой символ или подстроки.</span><span class="sxs-lookup"><span data-stu-id="24271-131">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring.</span></span> <span data-ttu-id="24271-132">Например «состояние как am\*"» соответствует Мэн и Массачусетского.</span><span class="sxs-lookup"><span data-stu-id="24271-132">For example, "state like 'M\*'" matches Maine and Massachusetts.</span></span> <span data-ttu-id="24271-133">Можно также использовать начальные и конечные звездочки поиск подстроки, содержащийся в значениях.</span><span class="sxs-lookup"><span data-stu-id="24271-133">You can also use leading and trailing asterisks to find a substring contained within the values.</span></span> <span data-ttu-id="24271-134">Например «состояние как "\*как\*"» соответствует Аляска, Arkansas и Массачусетского.</span><span class="sxs-lookup"><span data-stu-id="24271-134">For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="24271-135">Звездочки можно использовать только в конце строки условия, или друг с другом в начале и в конце строки критерии, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="24271-135">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above.</span></span> <span data-ttu-id="24271-136">Нельзя использовать в качестве начальных подстановочный знак звездочка ("\*str"), или встроенным ('s подстановочные знаки\*r ").</span><span class="sxs-lookup"><span data-stu-id="24271-136">You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r').</span></span> <span data-ttu-id="24271-137">Это приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="24271-137">This will cause an error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="24271-138">Если для текущей позиции строки не задано до вызова метода <STRONG>Найти</STRONG>, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="24271-138">An error will occur if a current row position is not set before calling <STRONG>Find</STRONG>.</span></span> <span data-ttu-id="24271-139">Любой метод, который задает положение строки, например <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, должен быть вызван до вызова метода <STRONG>поиска</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="24271-139">Any method that sets row position, such as <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, should be called before calling <STRONG>Find</STRONG>.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="24271-140">При вызове метода <STRONG>Поиск</STRONG> наборов записей и текущую позицию в наборе записей был создан последней записи или конца файла (EOF), вы не найдете все действия.</span><span class="sxs-lookup"><span data-stu-id="24271-140">If you call the <STRONG>Find</STRONG> method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything.</span></span> <span data-ttu-id="24271-141">Необходимо вызвать метод <STRONG>MoveFirst</STRONG> для установки текущей позиции/курсора в начало набора записей.</span><span class="sxs-lookup"><span data-stu-id="24271-141">You need to call the <STRONG>MoveFirst</STRONG> method to set the current position/cursor to the beginning of the recordset.</span></span></P>


