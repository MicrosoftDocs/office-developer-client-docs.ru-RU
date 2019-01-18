---
title: Свойство Field.Value (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9b51bb4e08546531f95e3795074f90b5d94d4c7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722881"
---
# <a name="fieldvalue-property-dao"></a><span data-ttu-id="55d93-102">Свойство Field.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="55d93-102">Field.Value property (DAO)</span></span>


<span data-ttu-id="55d93-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55d93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55d93-104">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="55d93-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="55d93-105">Чтение и запись **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="55d93-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d93-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55d93-106">Syntax</span></span>

<span data-ttu-id="55d93-107">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="55d93-107">*expression* .Value</span></span>

<span data-ttu-id="55d93-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="55d93-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d93-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="55d93-109">Remarks</span></span>

<span data-ttu-id="55d93-110">Параметр или возвращаемое значение имеет тип данных Variant, которое оценивается как значение соответствующего типа данных, указанный в свойстве **Тип** объекта.</span><span class="sxs-lookup"><span data-stu-id="55d93-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="55d93-111">Как правило свойство **Value** используется для извлечения и изменения данных в объектах **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="55d93-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="55d93-112">Свойство **Value** является свойством по умолчанию \*\*, **параметр**и **Свойства** \*\*объектов.</span><span class="sxs-lookup"><span data-stu-id="55d93-112">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects.</span></span> <span data-ttu-id="55d93-113">Таким образом можно задавать или возвращать значение одного из этих объектов, обратившись к ним напрямую вместо задания **значения** свойства.</span><span class="sxs-lookup"><span data-stu-id="55d93-113">Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="55d93-114">Попытка установить или возвратить **значение** свойства в недопустимом контексте (например, свойство **Value** объекта **поля** в коллекцию **полей** объекта **TableDef** ) будет отображено перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="55d93-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <span data-ttu-id="55d93-115">При чтении десятичные значения из базы данных Microsoft SQL Server, они будут иметь формат с помощью научное обозначение через рабочую область для Microsoft Access, но оно отображается как обычный десятичных значений с помощью технология ODBCDirect рабочей области.</span><span class="sxs-lookup"><span data-stu-id="55d93-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


