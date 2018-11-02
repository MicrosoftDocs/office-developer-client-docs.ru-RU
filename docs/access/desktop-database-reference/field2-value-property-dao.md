---
title: Свойство Field2.Value (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec1bdab14743a43bc4abda029e5f77ec1a8e6212
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925151"
---
# <a name="field2value-property-dao"></a><span data-ttu-id="5c838-102">Свойство Field2.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c838-102">Field2.Value property (DAO)</span></span>


<span data-ttu-id="5c838-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c838-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c838-104">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="5c838-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="5c838-105">Чтение и запись **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="5c838-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c838-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c838-106">Syntax</span></span>

<span data-ttu-id="5c838-107">*выражение* . Значение</span><span class="sxs-lookup"><span data-stu-id="5c838-107">*expression* .Value</span></span>

<span data-ttu-id="5c838-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="5c838-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c838-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c838-109">Remarks</span></span>

<span data-ttu-id="5c838-110">Параметр или возвращаемое значение имеет тип данных Variant, которое оценивается как значение соответствующего типа данных, указанный в свойстве **Тип** объекта.</span><span class="sxs-lookup"><span data-stu-id="5c838-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="5c838-111">Как правило свойство **Value** используется для извлечения и изменения данных в объектах **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5c838-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="5c838-112">Свойство **Value** является свойством по умолчанию **поле2**, **параметр**и **Свойства** объектов.</span><span class="sxs-lookup"><span data-stu-id="5c838-112">The **Value** property is the default property of the **Field2**, **Parameter**, and **Property** objects.</span></span> <span data-ttu-id="5c838-113">Таким образом можно задавать или возвращать значение одного из этих объектов, обратившись к ним напрямую вместо задания **значения** свойства.</span><span class="sxs-lookup"><span data-stu-id="5c838-113">Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="5c838-114">Попытка задать или получить **значение** свойства в недопустимом контексте (например, свойство **Value** объекта **поле2** в коллекции **полей** объекта **TableDef** ) будет отображено перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="5c838-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field2** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5c838-115">При чтении десятичные значения из базы данных Microsoft SQL Server, они будут иметь формат с помощью научное обозначение через рабочую область для Microsoft Access, но оно отображается как обычный десятичных значений с помощью технология ODBCDirect рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5c838-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>


