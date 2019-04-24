---
title: Свойство field2. ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292652"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="ebd4d-102">Свойство field2. ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="ebd4d-102">Field2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="ebd4d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebd4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebd4d-104">Задает или возвращает значение, которое проверяет данные в поле по мере их изменения или добавления в таблицу (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ebd4d-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="ebd4d-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd4d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebd4d-106">Syntax</span></span>

<span data-ttu-id="ebd4d-107">*Expression* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="ebd4d-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="ebd4d-108">*Expression (выражение* ) Выражение, возвращающее объект **field2** .</span><span class="sxs-lookup"><span data-stu-id="ebd4d-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd4d-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="ebd4d-109">Remarks</span></span>

<span data-ttu-id="ebd4d-110">Параметры или возвращаемые значения — это строка, описывающая сравнение в форме предложения WHERE SQL без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="ebd4d-111">Для объекта, который еще не добавлен в коллекцию **[Fields](fields-collection-dao.md)** , это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="ebd4d-112">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-112">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="ebd4d-113">Если данные не являются допустимыми, возникает перехватываемая ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-113">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="ebd4d-114">Возвращаемое сообщение об ошибке — это текст свойства **ValidationText** , если он указан, или текст выражения, указанного с помощью параметра **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-114">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="ebd4d-115">Для объекта **field2** использование свойства **ValidationRule** зависит от объекта, содержащего коллекцию Fields, к которой \*\*\*\* добавляется объект **field2** .</span><span class="sxs-lookup"><span data-stu-id="ebd4d-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ebd4d-116">Объект, добавленный в</span><span class="sxs-lookup"><span data-stu-id="ebd4d-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="ebd4d-117">Использование</span><span class="sxs-lookup"><span data-stu-id="ebd4d-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebd4d-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="ebd4d-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="ebd4d-119">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ebd4d-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebd4d-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="ebd4d-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ebd4d-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ebd4d-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebd4d-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="ebd4d-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="ebd4d-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ebd4d-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebd4d-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="ebd4d-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="ebd4d-125">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ebd4d-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebd4d-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="ebd4d-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ebd4d-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ebd4d-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ebd4d-128">Проверка поддерживается только для баз данных, использующих ядро СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="ebd4d-129">Строковое выражение, заданное свойством **ValidationRule** объекта **field2** , может ссылаться только на этот **field2**.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-129">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**.</span></span> <span data-ttu-id="ebd4d-130">Выражение не может ссылаться на пользовательские функции, статистические функции SQL или запросы.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-130">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="ebd4d-131">Чтобы задать свойство **ValidationRule** объекта **field2** , если его свойство **валидатеонсет** имеет **значение true**, выражение должно успешно анализироваться (с именем поля в качестве подразумеваемОго операнда) и оцениваться как **true**.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-131">To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="ebd4d-132">Если для свойства **валидатеонсет** задано **значение false**, то значение свойства **ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-132">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="ebd4d-133">Если присвоить свойству строку, Объединенную со значением, не являющимся целым числом, а системные параметры указывают символ, отличный от U. S. Decimal, такой как запятая (например, стрруле = "Price &gt; " &amp; лнгприце и лнгприце = 125, 50), то ошибка будет возникать при код пытается проверить какие бы то ни было данные.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="ebd4d-134">Это вызвано тем, что во время сцепления число преобразуется в строку с использованием десятичного знака системы, а SQL ядра СУБД Microsoft Access принимает только десятичные знаки США.</span><span class="sxs-lookup"><span data-stu-id="ebd4d-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


