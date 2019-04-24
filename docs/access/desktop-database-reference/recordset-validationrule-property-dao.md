---
title: Свойство Recordset. ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: c9250c13-18fe-1ff7-7846-7872c49a1e3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823208(v=office.15)
ms:contentKeyID: 48547671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e73d81cd890930952835ca6529cc3bfb455e6c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307506"
---
# <a name="recordsetvalidationrule-property-dao"></a><span data-ttu-id="60bea-102">Свойство Recordset. ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="60bea-102">Recordset.ValidationRule property (DAO)</span></span>

<span data-ttu-id="60bea-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60bea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60bea-104">Задает или возвращает значение, которое проверяет данные в поле после его добавление или изменения в таблице (только для рабочих областей Microsoft Access). Чтение и запись, **String**.</span><span class="sxs-lookup"><span data-stu-id="60bea-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="60bea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60bea-105">Syntax</span></span>

<span data-ttu-id="60bea-106">*Expression* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="60bea-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="60bea-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="60bea-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="60bea-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="60bea-108">Remarks</span></span>

<span data-ttu-id="60bea-109">Параметры или возвращаемые значения — это **строка** , описывающая сравнение в форме предложения WHERE SQL без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="60bea-109">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="60bea-110">Для объекта, который еще не добавлен в коллекцию **Fields** , это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="60bea-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="60bea-111">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="60bea-111">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="60bea-112">Если данные не являются допустимыми, возникает перехватываемая ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="60bea-112">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="60bea-113">Возвращаемое сообщение об ошибке — это текст свойства **ValidationText** , если он указан, или текст выражения, указанного с помощью параметра **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="60bea-113">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="60bea-114">Для объекта **Recordset** использование свойства **ValidationRule** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="60bea-114">For a **Recordset** object, use of the **ValidationRule** property is read-only.</span></span> <span data-ttu-id="60bea-115">Для объекта **tabledef** использование свойства **ValidationRule** зависит от состояния объекта **tabledef** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="60bea-115">For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60bea-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="60bea-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="60bea-117">Использование</span><span class="sxs-lookup"><span data-stu-id="60bea-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60bea-118">Базовая таблица</span><span class="sxs-lookup"><span data-stu-id="60bea-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="60bea-119">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="60bea-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60bea-120">Связанная таблица</span><span class="sxs-lookup"><span data-stu-id="60bea-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="60bea-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60bea-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60bea-122">Проверка поддерживается только для баз данных, использующих ядро СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="60bea-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="60bea-123">Строковое выражение, заданное свойством **ValidationRule** объекта **field** , может ссылаться только на это **поле**.</span><span class="sxs-lookup"><span data-stu-id="60bea-123">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="60bea-124">Выражение не может ссылаться на пользовательские функции, статистические функции SQL или запросы.</span><span class="sxs-lookup"><span data-stu-id="60bea-124">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="60bea-125">Чтобы задать свойство **ValidationRule** объекта **поля** , если для его свойства **валидатеонсет** задано **значение true**, выражение должно успешно анализироваться (с именем поля в качестве подразумеваемОго операнда) и оцениваться как **true**.</span><span class="sxs-lookup"><span data-stu-id="60bea-125">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="60bea-126">Если для свойства **валидатеонсет** задано **значение false**, то значение свойства **ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="60bea-126">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="60bea-127">Свойство **ValidationRule** объекта **Recordset** или объекта **tabledef** может ссылаться на несколько полей в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="60bea-127">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object.</span></span> <span data-ttu-id="60bea-128">Ограничения, указанные ранее в этой статье для объекта **field** , применяются.</span><span class="sxs-lookup"><span data-stu-id="60bea-128">The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="60bea-129">Для объекта **Recordset** табличного типа свойство **ValidationRule** наследует значение свойства **ValidationRule** объекта **tabledef** , который используется для создания объекта **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="60bea-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="60bea-130">Если присвоить свойству строку, Объединенную со значением, не являющимся целым числом, а системные параметры указывают символ, отличный от U. S. Decimal, такой как запятая (например, стрруле = "Price &gt; " &amp; лнгприце и лнгприце = 125, 50), то ошибка будет возникать при код пытается проверить какие бы то ни было данные.</span><span class="sxs-lookup"><span data-stu-id="60bea-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="60bea-131">Это вызвано тем, что во время сцепления число преобразуется в строку с использованием десятичного знака системы, а Microsoft Access SQL принимает только десятичные знаки США.</span><span class="sxs-lookup"><span data-stu-id="60bea-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>
