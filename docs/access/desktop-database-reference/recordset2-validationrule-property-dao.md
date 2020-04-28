---
title: Свойство Recordset2. ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7b146aa0278db278f3831bc0e00987d21e14b70a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307156"
---
# <a name="recordset2validationrule-property-dao"></a><span data-ttu-id="d29b8-102">Свойство Recordset2. ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="d29b8-102">Recordset2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="d29b8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d29b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d29b8-104">Задает или возвращает значение, которое проверяет данные в поле после его добавление или изменения в таблице (только для рабочих областей Microsoft Access). Чтение и запись, **String**.</span><span class="sxs-lookup"><span data-stu-id="d29b8-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d29b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d29b8-105">Syntax</span></span>

<span data-ttu-id="d29b8-106">*Expression* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="d29b8-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="d29b8-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d29b8-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d29b8-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="d29b8-108">Remarks</span></span>

<span data-ttu-id="d29b8-109">Параметры или возвращаемые значения — это **строка** , описывающая сравнение в форме предложения WHERE SQL без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="d29b8-109">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="d29b8-110">Для объекта, который еще не добавлен в коллекцию **Fields** , это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d29b8-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="d29b8-111">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="d29b8-111">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="d29b8-112">Если данные не являются допустимыми, возникает перехватываемая ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d29b8-112">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="d29b8-113">Возвращаемое сообщение об ошибке — это текст свойства **ValidationText** , если он указан, или текст выражения, указанного с помощью параметра **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="d29b8-113">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="d29b8-114">Для объекта **Recordset** использование свойства **ValidationRule** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d29b8-114">For a **Recordset** object, use of the **ValidationRule** property is read-only.</span></span> <span data-ttu-id="d29b8-115">Для объекта **tabledef** использование свойства **ValidationRule** зависит от состояния объекта **tabledef** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d29b8-115">For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d29b8-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="d29b8-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="d29b8-117">Применение</span><span class="sxs-lookup"><span data-stu-id="d29b8-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d29b8-118">Базовая таблица</span><span class="sxs-lookup"><span data-stu-id="d29b8-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="d29b8-119">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d29b8-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d29b8-120">Связанная таблица</span><span class="sxs-lookup"><span data-stu-id="d29b8-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="d29b8-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d29b8-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d29b8-122">Проверка поддерживается только для баз данных, использующих ядро СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d29b8-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="d29b8-123">Строковое выражение, заданное свойством **ValidationRule** объекта **field** , может ссылаться только на это **поле**.</span><span class="sxs-lookup"><span data-stu-id="d29b8-123">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="d29b8-124">Выражение не может ссылаться на пользовательские функции, статистические функции SQL или запросы.</span><span class="sxs-lookup"><span data-stu-id="d29b8-124">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="d29b8-125">Чтобы задать свойство **ValidationRule** объекта **поля** , если для его свойства **валидатеонсет** задано **значение true**, выражение должно успешно анализироваться (с именем поля в качестве подразумеваемого операнда) и оцениваться как **true**.</span><span class="sxs-lookup"><span data-stu-id="d29b8-125">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="d29b8-126">Если для свойства **валидатеонсет** задано **значение false**, то значение свойства **ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d29b8-126">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="d29b8-127">Свойство **ValidationRule** объекта **Recordset** или объекта **tabledef** может ссылаться на несколько полей в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="d29b8-127">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object.</span></span> <span data-ttu-id="d29b8-128">Ограничения, указанные ранее в этой статье для объекта **field** , применяются.</span><span class="sxs-lookup"><span data-stu-id="d29b8-128">The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="d29b8-129">Для объекта **Recordset** табличного типа свойство **ValidationRule** наследует значение свойства **ValidationRule** объекта **tabledef** , который используется для создания объекта **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="d29b8-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="d29b8-130">Если присвоить свойству строку, Объединенную со значением, не являющимся целым числом, а системные параметры указывают символ, отличный от U. S. Decimal, такой как запятая (например, стрруле = "Price &gt; " &amp; лнгприце, and лнгприце = 125, 50), то при попытке кода проверить какие-либо данные будет возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="d29b8-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="d29b8-131">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="d29b8-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>

