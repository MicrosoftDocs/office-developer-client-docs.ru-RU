---
title: Property.Value Property (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cac6d4d1715599a71c082ebc988d3f07d76da2b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888056"
---
# <a name="propertyvalue-property-dao"></a><span data-ttu-id="9027c-102">Property.Value Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9027c-102">Property.Value Property (DAO)</span></span>


<span data-ttu-id="9027c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9027c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9027c-104">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="9027c-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="9027c-105">Чтение и запись **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="9027c-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9027c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9027c-106">Syntax</span></span>

<span data-ttu-id="9027c-107">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="9027c-107">*expression* .Value</span></span>

<span data-ttu-id="9027c-108">*выражение* Переменная, которая представляет собой объект- **свойство** .</span><span class="sxs-lookup"><span data-stu-id="9027c-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9027c-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="9027c-109">Remarks</span></span>

<span data-ttu-id="9027c-110">Параметр или возвращаемое значение имеет тип данных Variant, которое оценивается как значение соответствующего типа данных, указанный в свойстве **Тип** объекта.</span><span class="sxs-lookup"><span data-stu-id="9027c-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="9027c-111">Как правило свойство **Value** используется для извлечения и изменения данных в объектах **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9027c-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="9027c-112">Свойство **Value** является свойством по умолчанию \*\*, **параметр**и **Свойства** \*\*объектов.</span><span class="sxs-lookup"><span data-stu-id="9027c-112">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects.</span></span> <span data-ttu-id="9027c-113">Таким образом можно задавать или возвращать значение одного из этих объектов, обратившись к ним напрямую вместо задания **значения** свойства.</span><span class="sxs-lookup"><span data-stu-id="9027c-113">Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="9027c-114">Попытка установить или возвратить **значение** свойства в недопустимом контексте (например, свойство **Value** объекта **поля** в коллекцию **полей** объекта **TableDef** ) будет отображено перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="9027c-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9027c-115">При чтении десятичные значения из базы данных Microsoft SQL Server, они будут иметь формат с помощью научное обозначение через рабочую область для Microsoft Access, но оно отображается как обычный десятичных значений с помощью технология ODBCDirect рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9027c-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>


