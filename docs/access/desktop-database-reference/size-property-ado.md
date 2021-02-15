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
# <a name="size-property-ado"></a><span data-ttu-id="5fcd4-102">Свойство Size (ADO)</span><span class="sxs-lookup"><span data-stu-id="5fcd4-102">Size property (ADO)</span></span>


<span data-ttu-id="5fcd4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fcd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5fcd4-104">Указывает максимальный размер объекта [Parameter](parameter-object-ado.md) (в ветвях или символах).</span><span class="sxs-lookup"><span data-stu-id="5fcd4-104">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5fcd4-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5fcd4-105">Settings and return values</span></span>

<span data-ttu-id="5fcd4-106">Задает или возвращает **длинное** значение, которое указывает максимальный размер значения в параметров (в ветвях или **символах).**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-106">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fcd4-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="5fcd4-107">Remarks</span></span>

<span data-ttu-id="5fcd4-108">Используйте свойство **Size,** чтобы определить максимальный размер значений, в которые записано или прочитано свойство [Value](value-property-ado.md) объекта **Parameter.**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-108">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="5fcd4-109">При указании типа данных переменной длины для объекта **Parameter** (например, любого типа **String,** например **adVarChar),** необходимо задать свойство **Size** объекта перед его приложением в коллекцию [Parameters;](parameters-collection-ado.md) в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-109">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="5fcd4-110">Если вы уже применили объект **Parameter** к коллекции **Parameters** объекта [Command](command-object-ado.md) и измените его тип на тип данных переменной длины, перед выполнением объекта **Command** необходимо установить свойство Size объекта **Parameter;**  в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-110">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="5fcd4-111">Если метод [Refresh](refresh-method-ado.md) используется для получения сведений о параметрах от поставщика и  возвращает один или несколько объектов parameter типа данных переменной длины, ADO может выделить память для параметров в зависимости от их максимального потенциального размера, что может привести к ошибке во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-111">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution.</span></span> <span data-ttu-id="5fcd4-112">Чтобы избежать ошибки, перед выполнением команды необходимо явно установить свойство **Size** для этих параметров.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-112">To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="5fcd4-113">Свойство **Size** имеет свойство read/write.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-113">The **Size** property is read/write.</span></span>

