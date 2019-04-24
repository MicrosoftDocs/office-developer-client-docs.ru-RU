---
title: Свойство field2. Value (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4324917fcabd768a9527b11fceadbfc2dc9ef2b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292631"
---
# <a name="field2value-property-dao"></a><span data-ttu-id="c2bb6-102">Свойство field2. Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2bb6-102">Field2.Value property (DAO)</span></span>


<span data-ttu-id="c2bb6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2bb6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2bb6-104">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="c2bb6-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="c2bb6-105">Для чтения и записи, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="c2bb6-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2bb6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2bb6-106">Syntax</span></span>

<span data-ttu-id="c2bb6-107">*Expression* . Оно</span><span class="sxs-lookup"><span data-stu-id="c2bb6-107">*expression* .Value</span></span>

<span data-ttu-id="c2bb6-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="c2bb6-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2bb6-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2bb6-109">Remarks</span></span>

<span data-ttu-id="c2bb6-110">Параметр или возвращаемое значение — это тип данных Variant, который оценивается как значение, соответствующее типу данных, как указано в свойстве **Type** объекта.</span><span class="sxs-lookup"><span data-stu-id="c2bb6-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="c2bb6-111">Как правило, свойство **value** используется для извлечения и изменения данных в объектах **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c2bb6-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="c2bb6-112">Свойство **value** является свойством по умолчанию для объектов **field2**, **Parameter**и **Property** .</span><span class="sxs-lookup"><span data-stu-id="c2bb6-112">The **Value** property is the default property of the **Field2**, **Parameter**, and **Property** objects.</span></span> <span data-ttu-id="c2bb6-113">Таким образом, вы можете задать или вернуть значение одного из этих объектов, обратившись к ним напрямую вместо того, чтобы указывать свойство **value** .</span><span class="sxs-lookup"><span data-stu-id="c2bb6-113">Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="c2bb6-114">Попытка задать или вернуть свойство **value** в неприемлемом контексте (например, свойство **value** объекта **field2** в коллекции **Fields** объекта **tabledef** ) приведет к ошибке перехвата.</span><span class="sxs-lookup"><span data-stu-id="c2bb6-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field2** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <span data-ttu-id="c2bb6-115">При чтении десятичных значений из базы данных Microsoft SQL Server они будут отформатированы с использованием экспоненциальной нотации в рабочей области Microsoft Access, но будут отображаться как обычные десятичные значения в рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="c2bb6-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


