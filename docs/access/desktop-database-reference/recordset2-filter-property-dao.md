---
title: Recordset2.Filter Property (DAO)
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
ms.openlocfilehash: ba5b43f6b0012e45c3cb4af662454ef76eab9194
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482569"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="f98b8-102">Recordset2.Filter Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f98b8-102">Recordset2.Filter Property (DAO)</span></span>


<span data-ttu-id="f98b8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f98b8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f98b8-104">Задает или возвращает значение, определяющее записей, включенных в последующем открытого объекта **набора записей** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f98b8-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="f98b8-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="f98b8-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98b8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f98b8-106">Syntax</span></span>

<span data-ttu-id="f98b8-107">*выражение* . Фильтр</span><span class="sxs-lookup"><span data-stu-id="f98b8-107">*expression* .Filter</span></span>

<span data-ttu-id="f98b8-108">*выражение* Выражение, возвращающее объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="f98b8-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f98b8-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="f98b8-109">Remarks</span></span>

<span data-ttu-id="f98b8-110">Параметр или возвращаемое значение имеет тип данных String, содержащий предложение WHERE инструкции SQL без зарезервированные слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="f98b8-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="f98b8-111">Используйте свойство **фильтра** для применения фильтра к динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип.</span><span class="sxs-lookup"><span data-stu-id="f98b8-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="f98b8-112">Свойство **фильтра** для ограничения записей, возвращенных из существующего объекта при открытии нового объекта **набора записей** на основе существующего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f98b8-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="f98b8-113">Использовать формат даты США (месяц день года) при фильтрации полей с датами, даже в том случае, если вы не используете США версия ядра базы данных Microsoft Access (в этом случае необходимо собрать все даты с объединения строк, например, strMonth & «-» & strDay & «-» & strYear).</span><span class="sxs-lookup"><span data-stu-id="f98b8-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="f98b8-114">В противном случае данные могут фильтрация не должным образом.</span><span class="sxs-lookup"><span data-stu-id="f98b8-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="f98b8-115">Во многих случаях это быстрее, чтобы открыть новый объект **набора записей** с помощью инструкции SQL, которая включает в себя предложение WHERE.</span><span class="sxs-lookup"><span data-stu-id="f98b8-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="f98b8-116">Если свойству присвоено значение string, объединяется с не – целое значение и системных параметров укажите десятичных знаков например запятыми (, например strFilter = «PRICE \> "& lngPrice и lngPrice = 125,50), возникает ошибка при попытке Откройте следующий **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f98b8-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="f98b8-117">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="f98b8-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

