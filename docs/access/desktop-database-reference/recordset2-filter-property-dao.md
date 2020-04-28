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
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="38d5a-102">Свойство Recordset2. Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="38d5a-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="38d5a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38d5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38d5a-104">Задает или возвращает значение, определяющее записи, включаемые в открытый впоследствии объект **Recordset** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="38d5a-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="38d5a-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="38d5a-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d5a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38d5a-106">Syntax</span></span>

<span data-ttu-id="38d5a-107">*выражение* .Filter</span><span class="sxs-lookup"><span data-stu-id="38d5a-107">*expression* .Filter</span></span>

<span data-ttu-id="38d5a-108">*Expression (выражение* ) Выражение, возвращающее объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="38d5a-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d5a-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="38d5a-109">Remarks</span></span>

<span data-ttu-id="38d5a-110">Параметр или возвращаемое значение является строковым типом данных, содержащим предложение WHERE оператора SQL без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="38d5a-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="38d5a-111">Используйте свойство **Filter**, чтобы применить фильтр к объекту **Recordset** типа динамический набор, статический набор или однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="38d5a-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="38d5a-112">Свойство **Filter** можно использовать для ограничения записей, возвращаемых из существующего объекта, если новый объект **Recordset** открыт на основе существующего объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="38d5a-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="38d5a-113">Используйте формат даты, принятый в США (месяц, день, год), при фильтрации полей, содержащих даты, даже если не используется версия ядра СУБД Microsoft Access для США (в этом случае необходимо вручную создать даты, сцепляя строки. Например: strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="38d5a-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="38d5a-114">В противном случае данные могут не отфильтроваться нужным образом.</span><span class="sxs-lookup"><span data-stu-id="38d5a-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="38d5a-115">Во многих случаях быстрее будет открыть новый объект **Recordset** с помощью оператора SQL, который включает предложение WHERE.</span><span class="sxs-lookup"><span data-stu-id="38d5a-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="38d5a-116">Если свойству присвоено значение строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия следующего объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="38d5a-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="38d5a-117">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="38d5a-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

