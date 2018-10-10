---
title: Size Property (ADO)
TOCTitle: Size Property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b690bd735f01e077b52c13c6c6e9b478234c1e8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482565"
---
# <a name="size-property-ado"></a><span data-ttu-id="9a245-102">Size Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="9a245-102">Size Property (ADO)</span></span>


<span data-ttu-id="9a245-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a245-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9a245-104">Указывает максимальный размер в байтах или символов объекта [параметров](parameter-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="9a245-104">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9a245-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9a245-105">Settings and Return Values</span></span>

<span data-ttu-id="9a245-106">Задает или возвращает значение типа **Long** , которое указывает максимальный размер в байтах или символов значение в объект **параметра** .</span><span class="sxs-lookup"><span data-stu-id="9a245-106">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a245-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a245-107">Remarks</span></span>

<span data-ttu-id="9a245-108">Используйте свойство **размер** для определения максимального размера для записи значений или чтение из свойства [Value](value-property-ado.md) объекта **параметров** .</span><span class="sxs-lookup"><span data-stu-id="9a245-108">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="9a245-109">Если указан тип данных переменной длины для **параметра** объекта (например, все **строки** типа, например **adVarChar**), необходимо задать свойство **размер** объекта перед добавлением в коллекцию [параметров](parameters-collection-ado.md) ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9a245-109">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="9a245-110">Если объект **параметра** уже добавлены коллекции **параметров** объекта [команды](command-object-ado.md) и измените его тип в тип данных переменной длины, необходимо задать свойство **Size** объект **параметра** перед выполнение **команды** объекта; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9a245-110">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="9a245-111">Если использовать метод [Refresh](refresh-method-ado.md) для получения сведений о параметрах от поставщика, и он возвращает тип данных переменной длины один или несколько объектов **параметров** , ADO может выделить память для параметров, основанных на их максимальный размер потенциальных, которое может использовать возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9a245-111">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution.</span></span> <span data-ttu-id="9a245-112">Чтобы предотвратить ошибки, необходимо явно присвойте свойству **размер** для этих параметров перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="9a245-112">To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="9a245-113">Свойство **Size** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="9a245-113">The **Size** property is read/write.</span></span>

