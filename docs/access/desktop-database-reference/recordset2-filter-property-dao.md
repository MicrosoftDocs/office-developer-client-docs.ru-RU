---
title: Свойство Recordset2. Filter (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307331"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="2a653-102">Свойство Recordset2. Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a653-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="2a653-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a653-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a653-104">Задает или возвращает значение, определяющее записи, включаемые в открытом впоследствии объект **Recordset** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2a653-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2a653-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="2a653-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a653-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a653-106">Syntax</span></span>

<span data-ttu-id="2a653-107">*Expression* . Фишинг</span><span class="sxs-lookup"><span data-stu-id="2a653-107">*expression* .Filter</span></span>

<span data-ttu-id="2a653-108">*Expression (выражение* ) Выражение, возвращающее объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="2a653-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a653-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a653-109">Remarks</span></span>

<span data-ttu-id="2a653-110">Параметр или возвращаемое значение — это строковый тип данных, который содержит предложение WHERE оператора SQL без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="2a653-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="2a653-111">Используйте свойство **Filter** для применения фильтра к объекту Recordset с типом "динамический **набор** ", "моментальный снимок" или "перенаправление только вперед".</span><span class="sxs-lookup"><span data-stu-id="2a653-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="2a653-112">С помощью свойства **Filter** можно ограничить записи, возвращенные из существующего объекта, при открытии нового объекта **Recordset** на основе существующего объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2a653-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="2a653-113">Используйте формат даты США (month-day-year) при фильтрации полей, содержащих даты, даже если не используется американский вариант ядра СУБД Microsoft Access (в этом случае необходимо собрать какие-либо даты, например, Стрмонс _Амп_ "-" _ Амп_ Стрдай _Амп_ "-" _Амп_ Стреар).</span><span class="sxs-lookup"><span data-stu-id="2a653-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="2a653-114">В противном случае данные могут быть отфильтрованы не так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="2a653-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="2a653-115">Во многих случаях быстрее открыть новый объект **Recordset** с помощью оператора SQL, включающего предложение WHERE.</span><span class="sxs-lookup"><span data-stu-id="2a653-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="2a653-116">Если присвоить свойству строку, Объединенную со значением, не являющимся целым числом, а системные параметры указывают символ, отличный от U. S. Decimal, такой как запятая (например, Стрфилтер = "PRICE \> " _амп_ Лнгприце и лнгприце = 125, 50), возникает ошибка при попытке Откройте следующий **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="2a653-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="2a653-117">Это вызвано тем, что во время сцепления число преобразуется в строку с использованием десятичного знака системы, а Microsoft Access SQL принимает только десятичные знаки США.</span><span class="sxs-lookup"><span data-stu-id="2a653-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

