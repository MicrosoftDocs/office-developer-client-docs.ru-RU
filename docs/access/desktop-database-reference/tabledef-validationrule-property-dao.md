---
title: Свойство TableDef. ValidationRule (DAO)
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
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="8bfba-102">Свойство TableDef. ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="8bfba-102">TableDef.ValidationRule property (DAO)</span></span>

<span data-ttu-id="8bfba-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bfba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8bfba-104">Задает или возвращает значение, которое проверяет данные в поле после его добавление или изменения в таблице (только для рабочих областей Microsoft Access). Чтение и запись, **String**.</span><span class="sxs-lookup"><span data-stu-id="8bfba-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bfba-105">Syntax</span></span>

<span data-ttu-id="8bfba-106">*Expression* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="8bfba-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="8bfba-107">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8bfba-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bfba-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bfba-108">Remarks</span></span>

<span data-ttu-id="8bfba-109">Параметры или возвращаемые значения — это **строка** , описывающая сравнение в форме предложения WHERE SQL без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="8bfba-109">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="8bfba-110">Для объекта, который еще не добавлен в коллекцию **Fields** , это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8bfba-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="8bfba-111">Свойство **ValidationRule** определяет, содержит ли поле допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="8bfba-111">The **ValidationRule** property determines whether or not a field contains valid data.</span></span> <span data-ttu-id="8bfba-112">Если данные не являются допустимыми, возникает перехватываемая ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="8bfba-112">If the data is not valid, a trappable run-time error occurs.</span></span> <span data-ttu-id="8bfba-113">Возвращаемое сообщение об ошибке — это текст свойства **ValidationText** , если он указан, или текст выражения, указанного с помощью параметра **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="8bfba-113">The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="8bfba-114">Проверка поддерживается только для баз данных, использующих ядро СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8bfba-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="8bfba-115">Строковое выражение, заданное свойством **ValidationRule** объекта **field** , может ссылаться только на это **поле**.</span><span class="sxs-lookup"><span data-stu-id="8bfba-115">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**.</span></span> <span data-ttu-id="8bfba-116">Выражение не может ссылаться на пользовательские функции, статистические функции SQL или запросы.</span><span class="sxs-lookup"><span data-stu-id="8bfba-116">The expression can't refer to user-defined functions, SQL aggregate functions, or queries.</span></span> <span data-ttu-id="8bfba-117">Чтобы задать свойство **ValidationRule** объекта **поля** , если для его свойства **валидатеонсет** задано **значение true**, выражение должно успешно анализироваться (с именем поля в качестве подразумеваемОго операнда) и оцениваться как **true**.</span><span class="sxs-lookup"><span data-stu-id="8bfba-117">To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**.</span></span> <span data-ttu-id="8bfba-118">Если для свойства **валидатеонсет** задано **значение false**, то значение свойства **ValidationRule** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8bfba-118">If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="8bfba-119">Свойство **ValidationRule** объекта **Recordset** или объекта **tabledef** может ссылаться на несколько полей в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="8bfba-119">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object.</span></span> <span data-ttu-id="8bfba-120">Ограничения, указанные ранее в этой статье для объекта **field** , применяются.</span><span class="sxs-lookup"><span data-stu-id="8bfba-120">The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="8bfba-121">Для объекта **tabledef** на основе связанной таблицы свойство **ValidationRule** наследует значение свойства **ValidationRule** базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="8bfba-121">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table.</span></span> <span data-ttu-id="8bfba-122">Если базовая таблица не поддерживает проверку, значением этого свойства является строка нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="8bfba-122">If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>

> [!NOTE]
> <span data-ttu-id="8bfba-123">Если присвоить свойству строку, Объединенную со значением, не являющимся целым числом, а системные параметры указывают символ, отличный от U. S. Decimal, такой как запятая (например, стрруле = "Price &gt; " &amp; лнгприце и лнгприце = 125, 50), то ошибка будет возникать при код пытается проверить какие бы то ни было данные.</span><span class="sxs-lookup"><span data-stu-id="8bfba-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="8bfba-124">Это вызвано тем, что во время сцепления число преобразуется в строку с использованием десятичного знака системы, а Microsoft Access SQL принимает только десятичные знаки США.</span><span class="sxs-lookup"><span data-stu-id="8bfba-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>
