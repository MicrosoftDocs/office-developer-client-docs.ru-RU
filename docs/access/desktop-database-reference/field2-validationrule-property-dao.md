---
title: Свойство Field2.ValidationRule (DAO)
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
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="5cf2d-102">Свойство Field2.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="5cf2d-102">Field2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="5cf2d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cf2d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cf2d-104">Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5cf2d-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5cf2d-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf2d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cf2d-106">Syntax</span></span>

<span data-ttu-id="5cf2d-107">*выражения* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="5cf2d-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="5cf2d-108">*выражение* Выражение, возвращаемая **объекту Field2.**</span><span class="sxs-lookup"><span data-stu-id="5cf2d-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf2d-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="5cf2d-109">Remarks</span></span>

<span data-ttu-id="5cf2d-110">Параметры или значения возврата — это строка, описываемая сравнение в виде оговорки SQL WHERE без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="5cf2d-111">Для объекта, еще не примыкаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство является чтением и написанием.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="5cf2d-112">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-112">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="5cf2d-113">Если данные не являются допустимыми, возникает ловкая ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-113">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="5cf2d-114">Возвращенное сообщение об ошибке — это текст свойства **ValidationText,** если указано, или текст выражения, указанного **в ValidationRule.**</span><span class="sxs-lookup"><span data-stu-id="5cf2d-114">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="5cf2d-115">Для объекта **Field2** использование свойства **ValidationRule** зависит от объекта,  который содержит коллекцию Полей, к которой примыкает объект **Field2.**</span><span class="sxs-lookup"><span data-stu-id="5cf2d-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cf2d-116">Объект, приданный</span><span class="sxs-lookup"><span data-stu-id="5cf2d-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="5cf2d-117">Usage</span><span class="sxs-lookup"><span data-stu-id="5cf2d-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cf2d-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="5cf2d-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="5cf2d-119">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5cf2d-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cf2d-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="5cf2d-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="5cf2d-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5cf2d-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cf2d-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="5cf2d-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="5cf2d-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5cf2d-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cf2d-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="5cf2d-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="5cf2d-125">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5cf2d-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cf2d-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="5cf2d-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="5cf2d-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5cf2d-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cf2d-128">Проверка поддерживается только для баз данных, которые используют двигатель базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="5cf2d-129">Выражение строки, указанное **свойством ValidationRule** объекта **Field2,** может ссылаться только на **это Поле2.**</span><span class="sxs-lookup"><span data-stu-id="5cf2d-129">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**.</span></span> <span data-ttu-id="5cf2d-130">Выражение не может ссылаться на определенные пользователем функции, SQL совокупные функции или запросы.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-130">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="5cf2d-131">Чтобы установить свойство **ValidationRule** объекта **Field2** при его параметре **ValidOnSet** **True,** выражение должно успешно разузнать (с именем поля в качестве подразумеваемого операнда) и оценить до **True**.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-131">To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="5cf2d-132">Если параметр **свойства ValidateOnSet** является **false,** параметр **ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-132">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="5cf2d-133">Если задайте свойство строке, сопутствуемой неинтегрированному значению, а параметры системы укажите не-США. десятичных символов, таких как запятая (например, strRule = &gt; "PRICE" &amp; lngPrice и lngPrice = 125,50), ошибка приведет, когда код пытается проверить любые данные.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="5cf2d-134">Это потому, что во время конкатепации номер будет преобразован в строку с помощью десятичных символов вашей системы по умолчанию, а двигатель базы данных Microsoft Access SQL принимает только десятичных символов США.</span><span class="sxs-lookup"><span data-stu-id="5cf2d-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


