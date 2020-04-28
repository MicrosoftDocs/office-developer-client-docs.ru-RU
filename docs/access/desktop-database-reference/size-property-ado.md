---
title: Свойство Size (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306932"
---
# <a name="size-property-ado"></a><span data-ttu-id="959b1-102">Свойство Size (ADO)</span><span class="sxs-lookup"><span data-stu-id="959b1-102">Size property (ADO)</span></span>


<span data-ttu-id="959b1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="959b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="959b1-104">Указывает максимальный размер объекта [параметра](parameter-object-ado.md) в байтах или символах.</span><span class="sxs-lookup"><span data-stu-id="959b1-104">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="959b1-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="959b1-105">Settings and return values</span></span>

<span data-ttu-id="959b1-106">Задает или возвращает значение **типа Long** , которое указывает максимальный размер значения в байтах или символах в объекте **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="959b1-106">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="959b1-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="959b1-107">Remarks</span></span>

<span data-ttu-id="959b1-108">Используйте свойство **size** для определения максимального размера значений, записываемых в свойство [value](value-property-ado.md) объекта **Parameter** или считанного из него.</span><span class="sxs-lookup"><span data-stu-id="959b1-108">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="959b1-109">Если указать тип данных переменной длины для объекта **Parameter** (например, любой **строковый** тип, например **адварчар**), необходимо задать свойство **size** объекта перед его добавлением в коллекцию [Parameters](parameters-collection-ado.md) ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="959b1-109">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="959b1-110">Если вы уже присоединяете объект **Parameter** к коллекции **Parameters** объекта [Command](command-object-ado.md) и изменяете его тип на тип данных переменной длины, необходимо задать свойство **size** объекта **Parameter** перед выполнением объекта **Command** ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="959b1-110">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="959b1-111">Если вы используете метод [Refresh](refresh-method-ado.md) для получения сведений о параметрах от поставщика и возвращает один или несколько объектов **параметров** типа данных переменной длины, ADO может выделить память для параметров на основе максимально возможного размера, что может привести к ошибке во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="959b1-111">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution.</span></span> <span data-ttu-id="959b1-112">Чтобы предотвратить возникновение ошибки, необходимо явно задать свойство **size** для этих параметров перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="959b1-112">To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="959b1-113">Свойство **size** доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="959b1-113">The **Size** property is read/write.</span></span>

