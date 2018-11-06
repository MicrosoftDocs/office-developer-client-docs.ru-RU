---
title: Свойство Parameter.Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95086e811288bd70dce15a22319531b28a1ecd6c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996729"
---
# <a name="parametervalue-property-dao"></a><span data-ttu-id="827eb-102">Свойство Parameter.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="827eb-102">Parameter.Value property (DAO)</span></span>

<span data-ttu-id="827eb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="827eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="827eb-104">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="827eb-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="827eb-105">Чтение и запись **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="827eb-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="827eb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="827eb-106">Syntax</span></span>

<span data-ttu-id="827eb-107">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="827eb-107">*expression* .Value</span></span>

<span data-ttu-id="827eb-108">*выражение* Переменная, которая представляет собой объект- **параметр** .</span><span class="sxs-lookup"><span data-stu-id="827eb-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="827eb-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="827eb-109">Remarks</span></span>

<span data-ttu-id="827eb-110">Параметр или возвращаемое значение имеет тип данных Variant, которое оценивается как значение соответствующего типа данных, указанный в свойстве **Тип** объекта.</span><span class="sxs-lookup"><span data-stu-id="827eb-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="827eb-111">Как правило свойство **Value** используется для извлечения и изменения данных в объектах **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="827eb-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="827eb-112">Свойство **Value** является свойством по умолчанию \*\*, **параметр**и **Свойства** \*\*объектов.</span><span class="sxs-lookup"><span data-stu-id="827eb-112">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects.</span></span> <span data-ttu-id="827eb-113">Таким образом можно задавать или возвращать значение одного из этих объектов, обратившись к ним напрямую вместо задания **значения** свойства.</span><span class="sxs-lookup"><span data-stu-id="827eb-113">Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="827eb-114">Попытка установить или возвратить **значение** свойства в недопустимом контексте (например, свойство **Value** объекта **поля** в коллекцию **полей** объекта **TableDef** ) будет отображено перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="827eb-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="827eb-115">При чтении десятичные значения из базы данных Microsoft SQL Server, они будут иметь формат с помощью научное обозначение через рабочую область для Microsoft Access, но оно отображается как обычный десятичных значений с помощью технология ODBCDirect рабочей области.</span><span class="sxs-lookup"><span data-stu-id="827eb-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


