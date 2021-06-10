---
title: Свойство TableDef.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44329a4cc320e9adcc0612629bcc3fdcd179a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314884"
---
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="fe5b9-102">Свойство TableDef.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe5b9-102">TableDef.ValidationRule property (DAO)</span></span>

<span data-ttu-id="fe5b9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe5b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe5b9-104">Задает или возвращает значение, которое проверяет данные в поле после его добавление или изменения в таблице (только для рабочих областей Microsoft Access). Чтение и запись, **String**.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe5b9-105">Syntax</span></span>

<span data-ttu-id="fe5b9-106">*выражения* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="fe5b9-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="fe5b9-107">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5b9-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe5b9-108">Remarks</span></span>

<span data-ttu-id="fe5b9-109">Параметры или значения возврата  — это строка, описываемая сравнение в виде оговорки SQL WHERE без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-109">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="fe5b9-110">Для объекта, еще не примыкаемого к коллекции **Fields,** это свойство является чтением и написанием.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="fe5b9-111">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-111">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="fe5b9-112">Если данные не являются допустимыми, возникает ловкая ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-112">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="fe5b9-113">Возвращенное сообщение об ошибке — это текст свойства **ValidationText,** если указано, или текст выражения, указанного **в ValidationRule.**</span><span class="sxs-lookup"><span data-stu-id="fe5b9-113">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="fe5b9-114">Проверка поддерживается только для баз данных, которые используют двигатель базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="fe5b9-115">Выражение строки, указанное **свойством ValidationRule** объекта **Field,** может ссылаться только на **это поле.**</span><span class="sxs-lookup"><span data-stu-id="fe5b9-115">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="fe5b9-116">Выражение не может ссылаться на определенные пользователем функции, SQL совокупные функции или запросы.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-116">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="fe5b9-117">Чтобы установить свойство **ValidationRule** объекта Field, когда параметр **свойства ValidateOnSet** является **True,** выражение должно успешно разузнать (с именем поля в качестве подразумеваемого операнда) и оценить его до **True**. </span><span class="sxs-lookup"><span data-stu-id="fe5b9-117">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="fe5b9-118">Если параметр **свойства ValidateOnSet** является **false,** параметр **ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-118">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="fe5b9-119">Свойство **ValidationRule** объекта **Recordset** или **TableDef** может ссылаться на несколько полей в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-119">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object.</span></span> <span data-ttu-id="fe5b9-120">Ограничения, отмеченные ранее в этом разделе для объекта **Field,** применяются.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-120">The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="fe5b9-121">Для объекта **TableDef** на основе связанной таблицы свойство **ValidationRule** наследует параметр **свойства ValidationRule** базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-121">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table.</span></span> <span data-ttu-id="fe5b9-122">Если базовая таблица не поддерживает проверку, значение этого свойства — строка нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="fe5b9-122">If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>

> [!NOTE]
> <span data-ttu-id="fe5b9-123">Если задайте свойство строке, сопутствуемой неинтегрированному значению, а параметры системы укажите не-США. десятичных символов, таких как запятая (например, strRule = &gt; "PRICE" &amp; lngPrice и lngPrice = 125,50), ошибка приведет, когда код пытается проверить любые данные.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="fe5b9-124">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="fe5b9-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>
