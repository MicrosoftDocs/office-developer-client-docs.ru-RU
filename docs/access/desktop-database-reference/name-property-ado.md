---
title: Свойство Name (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288667"
---
# <a name="name-property-ado"></a><span data-ttu-id="e48bb-102">Свойство Name (ADO)</span><span class="sxs-lookup"><span data-stu-id="e48bb-102">Name property (ADO)</span></span>


<span data-ttu-id="e48bb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e48bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e48bb-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e48bb-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e48bb-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="e48bb-105">Settings and return values</span></span>

<span data-ttu-id="e48bb-106">Задает или возвращает значение **String,** которое указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e48bb-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e48bb-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="e48bb-107">Remarks</span></span>

<span data-ttu-id="e48bb-108">Используйте свойство **Name,** чтобы назначить имя или получить имя объекта **Command,** **Property,** **Field** или **Parameter.**</span><span class="sxs-lookup"><span data-stu-id="e48bb-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="e48bb-109">Значение — чтение или записи на **объекте Command** и только чтение на **объекте Property.**</span><span class="sxs-lookup"><span data-stu-id="e48bb-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="e48bb-110">Для объекта **Field** **имя** обычно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e48bb-110">For a **Field** object, **Name** is normally read-only.</span></span> <span data-ttu-id="e48bb-111">Однако для новых  объектов [](value-property-ado.md) **Field,** которые были [](fields-collection-ado.md) добавлены в  коллекцию Полей записи, имя  считывалось или записывалось только после того, как было задано свойство Value для поля и поставщик данных успешно добавил новое поле, позвонив методу [Update](update-method-ado.md) коллекции [](record-object-ado.md) **Fields.**</span><span class="sxs-lookup"><span data-stu-id="e48bb-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="e48bb-112">Для **объектов Parameter,** которые еще не примыкают к коллекции [Параметры,](parameters-collection-ado.md) свойство **Name** читается или записи.</span><span class="sxs-lookup"><span data-stu-id="e48bb-112">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write.</span></span> <span data-ttu-id="e48bb-113">Для объектов **параметра и** всех остальных объектов свойство **Name** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e48bb-113">For appended **Parameter** objects and all other objects, the **Name** property is read-only.</span></span> <span data-ttu-id="e48bb-114">Имена не должны быть уникальными в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e48bb-114">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="e48bb-115">Свойство **Name** объекта можно получить по порядковой ссылке, после чего можно обратиться к объекту напрямую по имени.</span><span class="sxs-lookup"><span data-stu-id="e48bb-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="e48bb-116">Например, если rstMain.Properties (20). Имя дает updatability , вы можете впоследствии ссылаться на это свойство как уступает updatability , вы можете впоследствии ссылаться на это свойство как rstMain.Properties ("Updatability") .</span><span class="sxs-lookup"><span data-stu-id="e48bb-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

